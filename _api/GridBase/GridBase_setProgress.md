---
layout: apipost
title: setProgress
part: Objects
objectname: GridBase
directiontype: Function
permalink: /api/GridBase/setProgress/
jsonly: true
---


#### Description

> 프로그래스 창을 설정한다.

#### Syntax

> function setProgress(min, max, position, message)

#### Parameters

>**min**  
>Type: Number   
>프로그래스바의 시작값   

>**max**  
>Type: Number   
>프로그래스바의 끝값    

>**position**  
>Type: Number   
>프로그래스바의 위치값  

>**message**  
>Type: String  
>프로그래스바에 표시되는 메시지  

#### Return value

> None.

#### Example

<pre class="prettyprint">
    grdMain.showProgress();

    $.ajax({
        type: "GET",
        url: "http://" + location.host + "/Demo/GetCustomOrders?__date__=" + new Date().getTime(),
        dataType: "json",
        success: function (data) {
            grdMain.closeProgress();
            provider.fillJsonData(data, {
                start: 1,
                count : 10
            });
            var count = provider.getRowCount();
            $("#loadResult").css("color", "green").text(parseInt(count).toLocaleString() + " rows loaded.").show();
            grdMain.setFocus();
        },
        error: function (xhr, status, error) {
            var err = xhr + ', ' + status + ', ' + error;
            console.log("Load failed: " + err);
            $("#loadResult").css("color", "red").text("Load failed: " + err).show();
        },
        complete: function (data) {
            grdMain.closeProgress();
        },
        xhr: function () {
            var xhr = new window.XMLHttpRequest();
            //Download progress
            xhr.addEventListener("progress", function (evt) {
                if (evt.lengthComputable) {
                    if (evt.loaded > evt.total / 2) {
                        grdMain.setProgress(0, evt.total, evt.loaded, "Loading...");
                    } else {
                        grdMain.setProgress(0, evt.total, evt.loaded);
                    }
                }
            }, false);
            return xhr;
        }
    });</pre>

