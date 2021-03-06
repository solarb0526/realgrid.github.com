---
layout: apipost
title: setFixedOptions
part: Objects
objectname: GridBase
directiontype: Function
permalink: /api/GridBase/setFixedOptions/
---


#### Description

> 그리드 고정 영역에 관한 정보를 설정한다. [FixedOptions](/api/types/FixedOptions/)이 설정 모델이다.

#### Syntax

> function setFixedOptions(options)

#### Parameters

> **options**  
> Type: Object   
> [FixedOptions](/api/types/FixedOptions/) 모델과 같은 설정 정보. [FixedOptions](/api/types/FixedOptions/) 중 변경하고자 하는 값들만 전달하면 된다.  

#### Return value

> None.

#### Example

<pre class="prettyprint">
    grid.setFixedOptions({
        colCount: 2,
        rowCount: 0,
        ...
    });
</pre>

