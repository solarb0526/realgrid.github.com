---
layout: apipost
title: getJsonRows
part: Objects
objectname: DataProvider
directiontype: Function
permalink: /api/DataProvider/getJsonRows/
---


#### Description

> 지정한 범위 내의 데이터행들을 JSON 객체의 배열로 가져온다.

#### Syntax

> function getJsonRows(startRow, endRow)

#### Parameters

> **startRow**  
> Type: number  
> 시작 행 번호  

> **endRow**  
> Type: number  
> 끝 행 번호. 0보다 작은 값이면 마지막 행까지 가져온다.  

#### Return value

> Type: Array of object.  
> JSON 객체로 만들어진 데이터행들의 목록.  

#### Example

<pre class="prettyprint">
    var rows = provider.getJsonRows(10, 19);
</pre>


