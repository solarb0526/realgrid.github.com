---
layout: apipost
title: onFilteringChanged
part: Objects
objectname: GridBase
directiontype: Callback
permalink: /api/GridBase/onFilteringChanged/
---


#### Description

> 컬럼에 필터들이 설정되어 있고, 그 필터의 상태가 변경될 경우 호출된다.  

#### Syntax

> function onFilteringChanged(grid)  

#### Arguments

> **grid**  
> Type: [GridBase](/api/GridBase/)  
> GridBase 컨트롤  

#### Return

None.

#### Example

<pre class="prettyprint">
    grid.onFilteringChanged = function (grid){
	    alert("필터가 변경됨");
	}
</pre>

