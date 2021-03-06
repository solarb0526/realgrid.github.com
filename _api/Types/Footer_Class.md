---
layout: apipost
title: Footer
part: Types
typename: Config Classes
order: Footer
objectname: 
directiontype: 
permalink: /api/types/Footer/
---

#### Description

> 푸터 영역과 관련된 설정 모델이다. 푸터는 컬럼 및 컬럼그룹들의 푸터와 Indicator, StateBar, CheckBar 등의 Foot 영역들로 구성된다.

#### Properties

> **height**  
> Type: number  
> Default: 0  
> Footer의 높이를 픽셀 단위로 지정한다. 0이면 자동으로 계산된다. 0보다 큰 값이면 이 값과 minHeight에 지정한 값 중 큰 값으로 지정된다.

> **minHeight**  
> Type: number  
> Default: 23  
> Footer의 최소 높이를 지정한다.  

> **resizable**  
> Type: boolean   
> Default: false  
> 사용자가 Footer 왼쪽 셀의 위쪽을 마우스 드래깅해서 헤더의 높이를 변경하게 할 수 있도록 할 것인 지를 지정한다.

> **visible**  
> Type: boolean   
> Default: true     
> true면 Footer를 표시한다.  
