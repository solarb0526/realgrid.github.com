---
layout: apipost
title: onRowGroupPanelClicked
part: Objects
objectname: GridBase
directiontype: Callback
permalink: /api/GridBase/onRowGroupPanelClicked/
jsonly: true
---


#### Description

> 사용자가 마우스로 RowGroupPanel을 클릭했을 때 호출된다.  

#### Syntax

> function onRowGroupPanelClicked (grid, column)  

#### Arguments

> **grid**  
> Type: [GridBase](/api/GridBase/)  
> GridBase 컨트롤  

> **column**  
> Type: object  
> [DataColumn](/api/types/DataColumn/)과 같은 구조의 object.  

#### Return

> None.  

#### Example

<pre class="prettyprint">
    grid.onRowGroupPanelClicked =  function (grid, column) {
        console.log("onRowGroupPanelClicked : " + "(" + column.name + ")")
    };
</pre>

