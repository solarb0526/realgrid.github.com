---
layout: faqpost
title:  특정 row만 Editable 하도록 하는 방법
date:   2015-05-13 00:00:00
categories: faq
part: RealGrid
directiontype: 
tags:
    - row
    - editable
---

# Q.

특정 row만 Editable 하도록 하는 방법

---
***

# A.

Checkbox를 이용한 Row단위 Editable을 설정 방법을 알려드리겠습니다.  

Current 가 이동 하였을때 콜백 되는 함수   

> grid.onCurrentChanged(grid, newIndex)

CheckBox를 Check 하였을때 콜백 되는 함수  

> grid.onItemChecked(grid, itemIndex, checked)


CheckBox를 전체 Check 하였을때 콜백되는 함수  

> grid.onItemAllChecked(grid, checked) 

를 이용해서 구현해 보았습니다 아래 예제를 참조해 주세요.

<pre class="prettyprint">
grid.onItemChecked = function(grid, itemIndex, checked){
    editableControl(checked, grid);
}

grid.onItemAllChecked = function(grid, checked){
    editableControl(checked, grid);
}

grid.onCurrentChanged = function(grid, newIndex){
    var check = grid.isCheckedItem(newIndex.itemIndex);
    editableControl(check, grid);
}

function editableControl(check, grid){
    var index = grid.getCurrent();
    var column = grid.columnByField(index.fieldName);
    if(check){
         // column field name = a
        if(index.fieldName == 'a'){
            grid.setColumnProperty(column, "editable", true);
        }else{
            grid.setColumnProperty(column, "editable", false);
        }
    }else{
        grid.setColumnProperty(column, "editable", false);
    }
}
</pre>
