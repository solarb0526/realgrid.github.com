---
layout: apipost
title: clearRowStates
part: Objects
objectname: DataProvider
directiontype: Function
permalink: /api/DataProvider/clearRowStates/
---


#### Description

> RowState가 "none"이 아닌 행들의 RowState를 모두 제거한다. 
> 이 때 deleteRows 매개변수를 true로 지정하면 "deleted"나 "createAndDeleted" 상태를 갖는 행들을 실제로 삭제한다.

#### Syntax

> function clearRowStates(deleteRows, rowEvents)

#### Parameters

> **deleteRows**  
> Type: boolean  
> true면 "deleted"나 "createAndDeleted" 상태를 갖는 행들을 실제로 삭제한다.  

> **rowEvents**  
> Type: Boolean  
> false면 상태 변경 이벤트를 발생시키지 않는다. 지정하지 않으면 false다.  

#### Return value

> None.

#### Example

<pre>
    provider.clearRowStates(true, false);
</pre>
