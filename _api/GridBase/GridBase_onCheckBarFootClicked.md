---
layout: apipost
title: onCheckBarFootClicked
part: Objects
objectname: GridBase
directiontype: Callback
permalink: /api/GridBase/onCheckBarFootClicked/
jsonly: true
---


#### Description

> 사용자가 마우스로 CheckBarFoot셀을 클릭했을 때 호출된다.  

#### Syntax

> function onCheckBarFootClicked (grid)  

#### Arguments

> **grid**  
> Type: [GridBase](/api/GridBase/)  
> GridBase 컨트롤  

#### Return

> None.  

#### Example

<pre class="prettyprint">
    grid.onCheckBarFootClicked =  function (grid) {
        console.log("onCheckBarFootClicked");
    };
</pre>

