---
layout: apipost
title: PasteOptions
part: Types
typename: Config Classes
order: PasteOptions
objectname: 
directiontype: 
permalink: /api/types/PasteOptions/
---


#### Description

> 붙여넣기시 사용하는 옵션 정보이다.  

#### Properies

> **singleMode**  
> Type: boolean  
> Default: false  
> true면 클립보드의 내용과 상관없이 포커스를 갖는 셀 하나에만 값을 붙여 넣는다.  

> **startEdit**  
> Type: boolean  
> Default: true  
> 붙여넣게 될 값이 복수 행이 아니고, 붙여넣을 행이 아직 편집 중이 아니면 편집을 시작한다. false면 이 행에 연결된 데이터행을 업데이트한다.

> **commitEdit**  
> Type: boolean  
> Default: true  
> 복수 행 붙여넣기일 때 기존 편집 상태를 commit 한다. false로 지정하면 기존 편집을 취소한다. 

> **enableAppend**  
> Type: boolean  
> Default: true  
> 붙여넣을 복수 행이 기존 행의 범위를 넘어설 때 행을 추가한다.  

> **fillFieldDefaults**  
> Type: boolean  
> Default: false  
> true이면 행 추가시 포함되지 않은 필드의 값을 data field의 기본값으로 채운다.  

> **fillColumnDefaults**  
> Type: boolean  
> Default: false  
> true이면 행 추가시 포함되지 않은 필드의 값을 컬럼의 기본값으로 채운다. fillFieldDefaults가   true라면 데이터필드의 기본값을 먼저 적용한 후 컬럼 기본값을 적용한다.  

> **forceRowValidation**  
> Type: boolean  
> Default: false  
> true이면 복수행 붙여 넣기 중 행별로 행 validation을 실행한다.  

> **forceColumnValidation**  
> Type: boolean  
> Default: false  
> 복수행 붙여 넣기 중 행별로 컬럼 validation을 실행한다. forceRowValidation가 true 라면 행 validation을 먼저 실행한다.

> **datetimeFormats**  
> Type:  
> Default: null  
> 데이터필드에 지정된 datetimeFormat 외에 datetime 필드의 값으로 변환할 때 사용할 하나 이상의 형식을 지정한다.

> **booleanFormat**  
> Type:  
> Default: null  
> 데이터필드에 지정된 booleanFormat이나 기본 형식 이 외에, boolean 필드의 값으로 변환할 때 사용할 변환 형식을 지정한다

> **numberChars**  
> Type:  
> Default: null  
> number 필드 값으로 변환할 때 에러로 판단하지 않고 무시해도 되는 하나 이상의 문자열들을 지정한다. 즉, 여기에 지정한 문자열들을 모두 빈 문자열로 치환한 후 숫자로 변환한다.

> **selectionBase**  
> Type: boolean  
> Default: false  
> 붙여넣기 시작 위치를 지정한다. true면 focus 셀이 포함된 선택 영역의 처음 셀부터 붙여넣기 한다. false면 focus 셀 부터 붙여넣기 한다. 기본값은 false.

> **stopOnError**  
> Type: boolean  
> Default: true  
> true면 Validation이 실패하거나 형변환이 실패하면 나머지 붙여넣기를 중지하고 예외를 발생시킨다.  
> false면 실패한 행은 수정이나 추가하지 않고 계속 진행한다. 이 때, 기존 행을 수정하는 경우, 에러가 있는 행은 건너뛰고 수정하지 않는다.   

> **noEditEvent**  
> Type: boolean  
> Default: true  
> true면 onEditRowChanged가 발생하지 않는다. onEditRowPasted는 지정여부와 상관없이 항상 발생한다.  

> **checkReadOnly**  
> Type: boolean  
> Default: false  
> true이면 readOnly이거나 editable이 false인 Column은 paste대상에서 제외된다.     

#### See Also

> [Copy & Paste](http://demo.realgrid.net/Demo/CopyAndPaste) 참조

  