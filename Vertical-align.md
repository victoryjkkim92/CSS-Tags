# CSS vertical-align Property

### Definition and Usage

The vertical-align property sets the vertical alignment of an element.


*	Default value:	baseline
*	Inherited:	no
*	Animatable:	yes. Read about animatable
*	Version:	CSS1
*	JavaScript syntax: object.style.verticalAlign="top"

### CSS Syntax

vertical-align: baseline|length|sub|super|top|text-top|middle|bottom|text-bottom|initial|inherit;

### Property Values

|	Value	 :		Description		|

* baseline	:	The element is aligned with the baseline of the parent. This is default	

	부모의 baseline에 맞추어 해당 엘리먼트의 baseline 을 정렬합니다.  몇몇 replaced elements의 베이스라인은 예를들면`<textarea>`은 HTML 명세에 정의되어 있지 않으므로, 이 키워드는 브라우저마다 다른 결과를 보여줍니다.


* length	:	Raises or lower an element by the specified length. Negative values are allowed. Read about length units

	해당 엘리먼트의 baseline을 부모의 baseline에서 주어진 길이만큼 위로 정렬합

		
*	%	:	Raises or lower an element in a percent of the "line-height" property. Negative values are allowed

	`<length>` value와 마찬가지로 해당 엘리먼트의 baseline을 부모의 baseline에서 line-height의 퍼센트로 주어진 퍼센트만큼 위로 정렬합니다.
	
	
*	sub	:	The element is aligned with the subscript baseline of the parent	
	
	해당 엘리먼트의 baseline을 부모의 subscript-baseline으로 정렬합니다.

*	super	:	The element is aligned with the superscript baseline of the parent	

	해당 엘리먼트의 baseline을 부모의 superscript-baseline으로 정렬합니다.

*	top		:	The element is aligned with the top of the tallest element on the line
	
	해당 엘리먼트의 top과 이것의 자손들의 top을 전체 라인의 top으로 정렬합니다.
	
*	text-top	:	The element is aligned with the top of the parent element's font	

	해당 엘리먼트의 top을 부모 엘리먼트 폰트의 top으로 정렬합니다.

*	middle		:	The element is placed in the middle of the parent element

	해당 엘리먼트의 middle을 부모의 baseline + x-height / 2 로 정렬합니다.
	
*	bottom		:	The element is aligned with the lowest element on the line	

	해당 엘리먼트의 bottom과 이것의 자손들의 bottom을 전체 라인의 bottom으로 정렬합니다.

*	text-bottom	:	The element is aligned with the bottom of the parent element's font	

	해당 엘리먼트의 bottom을 부모 엘리먼트 폰트의 bottom으로 정렬합니다.


*	initial	:	Sets this property to its default value. Read about initial
	
*	inherit	:	Inherits this property from its parent element. Read about inherit


vertical-align CSS 속성은 inline 또는 table-cell box에서의 수직 정렬을 지정합니다.

```
/* keyword values */
vertical-align: baseline;
vertical-align: sub;
vertical-align: super;
vertical-align: text-top;
vertical-align: text-bottom;
vertical-align: middle;
vertical-align: top;
vertical-align: bottom;

/* <length> values */
vertical-align: 10em;
vertical-align: 4px;

/* <percentage> values */
vertical-align: 20%;

/* Global values */
vertical-align: inherit;
vertical-align: initial;
vertical-align: unset;
```

vertical-align 속성은 두 컨텍스트에서 사용될 수 있습니다:

* 엘리먼트의 box를 이것이 포함된 line box 내부에서 수직 정렬하고자 할 때. 예를 들어서, `<img>` 엘리먼트를 텍스트 엘리먼트의 라인 속에서 정렬할 때 쓰일 수 있습니다:

* table의 한 셀에서 포함하고 있는 내용을 수직 정렬할 때:


## vertical-align은 오로지 inline과 table-cell 엘리먼트에만 적용된다는 것에 주의하세요: 이 속성을 block level 엘리먼트에 사용할 수 없습니다.