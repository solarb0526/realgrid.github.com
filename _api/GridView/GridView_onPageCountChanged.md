---
layout: apipost
title: onPageCountChanged
part: Objects
objectname: GridView
directiontype: Callback
permalink: /api/GridView/onPageCountChanged/
---


#### Description

> 그리드가 [Paging](/api/features/Paging/) 상태일 때, 다른 페이지로 이동한 후 호출된다.

#### Syntax

> function onPageCountChanged(grid, pageCount)

#### Arguments

> **grid**  
> Type: [GridView](/api/GridView/)  
> GridView 컨트롤

> **pageCount**  
> Type: number  
> 변경된 페이지의 수.  

#### Return

> None.

#### Example

<pre class="prettyprint">
    grid.onPageCountChanged =  function (grid, pageCount) {
        alert("onPageCountChanged:" + pageCount);
    }
</pre>
