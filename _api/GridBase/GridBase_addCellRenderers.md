---
layout: apipost
title: addCellRenderers
part: Objects
objectname: GridBase
directiontype: Function
permalink: /api/GridBase/addCellRenderers/
---


#### Description

> 데이터셀 렌더러 정보들을 미리 추가한다.
> 컬럼 동적 스타일에 추가한 renderer 값을 이용하면, 같은 컬럼에서 값에 따라 다른 렌더러를 사용하여 셀을 표시할 수 있다.

#### Syntax

> function addCellRenderers(renderers)

#### Parameters

> **renderers**  
> Type: Object  
> 계층적 구조로 구성되는 렌더러 데이터  

#### Return value

> None.

#### Example

<pre class="prettyprint">
	grdMain.addCellRenderers([{
		"id": "bar01",
		"type": "bar"
	}, {
		"id": "bar02",
		"type": "bar",
		"maximum": 100000,
		"showLabel": false
	}, {
		"id": "check01",
		"type": "check",
		"editable": true,
		"startEditOnClick": true,
		"trueValues": "True",
		"falseValues": "False",
		"labelPosition": "right"				
	}, {
		"id": "shape01",
		"type": "shape"
	}, {
		"id": "signal01",
		"type": "signal",
		"barCount": 10,
		"minimum": 0,
		"maximum": 100
	}, {
		"id": "signal02",
		"type": "signal",
		"barCount": 10,
		"minimum": 0,
		"maximum": 100000
	}]);
</pre>

