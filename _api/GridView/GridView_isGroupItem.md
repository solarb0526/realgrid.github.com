---
layout: apipost
title: isGroupItem
part: Objects
objectname: GridView
directiontype: Function
permalink: /api/GridView/isGroupItem/
---


#### Description

> 지정한 ItemIndex가 그룹 아이템인지 확인한다.

#### Syntax

> function isGroupItem(itemIndex)

#### Parameters

> **itemIndex**  
> Type: number  
> 확인하려는 그리드상의 index

#### Return value

> Type: boolean  
> 그룹 아이템 여부

#### Example

<pre class="prettyprint">
    var bGroupItem = grid.isGroupItem(1);
</pre>

