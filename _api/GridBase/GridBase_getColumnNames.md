---
layout: apipost
title: getColumnNames
part: Objects
objectname: GridBase
directiontype: Function
permalink: /api/GridBase/getColumnNames/
---


#### Description

> 그리드에 설정되어 있는 컬럼 이름들을 가져온다.  

#### Syntax

> function getColumnNames(columnsOnly)  

#### Parameters

> **columnsOnly**  
> Type: Boolean  
> Default: false  
> true면 컬럼 그룹들을 포함한 모든 컬럼들의 이름을 가져온다.   

#### Return value

> Type: array of string  
> 컬럼 이름 배열.  

#### Example

<pre class="prettyprint">
var columnNames = grid.getColumnNames(false);
</pre>





