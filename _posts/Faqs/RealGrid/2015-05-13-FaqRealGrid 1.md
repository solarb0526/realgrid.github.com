---
layout: faqpost
title:  dropDown리스트가 동적으로 앞의 값에 따라서 변경되는 방법이 있나요?
date:   2015-05-13 00:00:00
categories: faq
part: RealGrid
directiontype: 
tags:
    - dropdown
---

# Q.

dropDown리스트가 동적으로 앞의 값에 따라서 변경되는 방법이 있나요?

---
***

# A.

예전에 자체 프로젝트에 사용했던 소스로 설명 드리겠습니다.

<pre class="prettyprint">
/**
 * 먼저 setLookups로 id(lookupTree를 사용할 컬럼에 지정), levels(선행조건 갯수+ 자신 컬럼 갯수를
 * 지정),key(실제 data값),values(그리드에 보여지는 값)을 설정합니다. type1은 teamcode컬럼의 lookupTree에
 * 사용되고 type2는 empcode컬럼의 lookupTree에 사용합니다.
 */
 
function setLookups(grid) {
              
        grid.setLookups([{
               id: "type1",
               levels: 2,
               keys: [],
               values: []
        }, {
               id: "type2",
               levels: 3,
               keys: [],
               values: []
        }]);
}
 
/**
 * code컬럼은 values, labels를 지정한 dropDown 컬럼으로 설정합니다.
 */
 
function setColumns(grid) {
        var values1 =[], labels1=[];
       
        var columns = [{
              header : {text : "영업부서"},
               fieldName : "code",
               lookupDisplay : true,
               values: values1,
               labels: labels1,
               editor : {
                       type : "dropDown"
               }
        }, {
            	 header : {text : "영업팀"},
               fieldName : "teamCode",
               lookupDisplay : true,
               lookupSourceId : "type1",
               lookupKeyFields : ["code", "teamCode"],
               editor : {
                       type : "dropDown"
               }
        }, {
                 header : {text : "영업사원"},
               fieldName : "empCode",
               lookupDisplay : true,
               lookupSourceId : "type2",
               lookupKeyFields : ["code", "teamCode", "empCode"],
               editor : {
                       type : "dropDown"
               }
        }];
 
        $.post("/realgrid/product/dptCode.do",function(json){
               $.each(json,function(k,v){
                       values1.push(v.code);
                       labels1.push(v.name);
               });
        grid.setColumns(columns);
        };
}
 


/**
 * 본 예제는 Cell의 데이타가 변경되었을때 발생하는 이벤트 함수 GridView.onCellEdited를 사용하엿습니다.
 */
function onCellEditedMenu(grid, itemIndex,  dataRow, field){
        var fieldIndexCode = dataProvider.getFieldIndex("code");
        var fieldIndexTeamCode = dataProvider.getFieldIndex("teamCode");
        // 영업팀
        // onCellEdited 가 발생한 필드가 첫번째 컬럼일때 두번째에 lookupTree를 생성합니다.
        if (field == fieldIndexCode){
               var searchType1 = grid.getValue(itemIndex, fieldIndexCode);
               var fieldIndexTeamCode = dataProvider.getFieldIndex("teamCode");
               var fieldIndexEmpCode = dataProvider.getFieldIndex("empCode");
 
               var ajaxData = "&searchType1="+searchType1+"&searchType2=";
              
               // data를 db에서 가져온후
               $.post("/realgrid/product/teamCode.do",ajaxData,function(json){
                       $.each(json, function(k,v){
                              // existsLookupData 함수를 이용해서 해당값이 없으면
                              if (!grdMain.existsLookupData("type1", [searchType1, v.teamCode])) {
                                      // type1 에 fillLookupData 이용해서 트리 값을 채워줍니다.
                                      grid.fillLookupData("type1",{"rows" :  [[searchType1, v.teamCode, v.teamName]]});
                              };
                       });
               });
        };
       
        // 영업사원
        // 아래는 2두번째 lookupTree 생성 방법입니다.
        if(field == fieldIndexTeamCode){
               var searchType1 = grid.getValue(itemIndex, fieldIndexCode);
               var searchType2 = grid.getValue(itemIndex, fieldIndexTeamCode);
               var fieldIndexEmpCode = dataProvider.getFieldIndex("empCode");
 
               var ajaxData = "&searchType1="+searchType1+"&searchType2="+searchType2;
              
               $.post("/realgrid/product/empCode.do",ajaxData,function(json){
                       $.each(json, function(k,v){
                              if (!grdMain.existsLookupData("type2", [searchType1, searchType2, v.empCode])) {
                                     grid.fillLookupData("type2", { "rows" :  [[searchType1, searchType2, v.empCode, v.empName]]});
                              };
                       });
               });
        };
}
</pre>
