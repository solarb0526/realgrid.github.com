---
layout: apipost
title: checkRow
part: Objects
objectname: TreeView
directiontype: Function
permalink: /api/TreeView/checkRow/
---


#### Description

> 입력된 rowId에 해당하는 아이템을 체크하거나 해제한다.  

#### Syntax

> function checkRow(rowId, checked, exclusive)  

#### Parameters

> **rowId**  
> Type: Number  
> [TreeDataProvider](/api/TreeView/) 데이터행의 Index이다.  

> **checked**  
> Type: Boolean  
> Default: true  
> true로 입력을 하면 입력된 rowId의 데이터행을 체크한다. false로 입력하면 해제한다.  

> **exclusive**  
> Type: Boolean  
> Default: false  
> true로 입력하면 체크된 다른 아이템이 있는 경우 체크를 해제하고 입력된 rowId만 체크한다.  

#### Return value

> None.

#### Example

<pre class="prettyprint">
    treeMain.checkItem(treeMain.getCurrent().dataRow,true,false);
</pre>

