---
layout: apipost
title: setDataProvider
part: Objects
objectname: GridBase
directiontype: Function
permalink: /api/GridBase/setDataProvider/
---


#### Description

> 그리드에 [Data Provider](/api/LocalDataProvider/)를 연결한다.

#### Syntax

> function setDataProvider(provider)

#### Parameters

> **provider**  
> Type: [LocalDataProvider](/api/LocalDataProvider/)  
> Data Provider  

#### Return value

> None.

#### Example

<pre class="prettyprint">
    var grdMain = new RealGrids.GridView(id);
    var dataProvider = new RealGrids.LocalDataProvider();
    var grdMain.setDataProvider(dataProvider);
</pre>




