---
layout: apipost
title: getColumnFilters
part: Objects
objectname: GridBase
directiontype: Function
permalink: /api/GridBase/getColumnFilters/
---


#### Description

> 지정한 컬럼의 필터를 가져온다.  

#### Syntax

> function getColumnFilters (column)  

#### Parameters

> **column**  
> Type: Object  
> Data Column  


#### Return value

> Type: Objects  
> 필터 Objects  


#### Example

<pre class="prettyprint">
	var fieldName = grdMain.getCurrent().fieldName;
	var column = grdMain.columnByField(fieldName);
	var filters = grdMain.getColumnFilters(column);
	
	alert(JSON.stringify(filters));				
</pre>

