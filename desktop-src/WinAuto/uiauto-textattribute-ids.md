---
title: Идентификаторы текстовых атрибутов (UIAutomationClient. h)
description: В этом разделе описываются именованные константы, используемые для определения текстовых атрибутов диапазона текста Microsoft UI Automation.
ms.assetid: 67d86817-6a3f-4047-88d9-34f33f52a563
topic_type:
- apiref
api_name:
- UIA_AfterParagraphSpacingAttributeId
- UIA_AnimationStyleAttributeId
- UIA_AnnotationObjectsAttributeId
- UIA_AnnotationTypesAttributeId
- UIA_BackgroundColorAttributeId
- UIA_BeforeParagraphSpacingAttributeId
- UIA_BulletStyleAttributeId
- UIA_CapStyleAttributeId
- UIA_CaretBidiModeAttributeId
- UIA_CaretPositionAttributeId
- UIA_CultureAttributeId
- UIA_FontNameAttributeId
- UIA_FontSizeAttributeId
- UIA_FontWeightAttributeId
- UIA_ForegroundColorAttributeId
- UIA_HorizontalTextAlignmentAttributeId
- UIA_IndentationFirstLineAttributeId
- UIA_IndentationLeadingAttributeId
- UIA_IndentationTrailingAttributeId
- UIA_IsActiveAttributeId
- UIA_IsHiddenAttributeId
- UIA_IsItalicAttributeId
- UIA_IsReadOnlyAttributeId
- UIA_IsSubscriptAttributeId
- UIA_IsSuperscriptAttributeId
- UIA_LineSpacingAttributeId
- UIA_LinkAttributeId
- UIA_MarginBottomAttributeId
- UIA_MarginLeadingAttributeId
- UIA_MarginTopAttributeId
- UIA_MarginTrailingAttributeId
- UIA_OutlineStylesAttributeId
- UIA_OverlineColorAttributeId
- UIA_OverlineStyleAttributeId
- UIA_SelectionActiveEndAttributeId
- UIA_StrikethroughColorAttributeId
- UIA_StrikethroughStyleAttributeId
- UIA_StyleIdAttributeId
- UIA_StyleNameAttributeId
- UIA_TabsAttributeId
- UIA_TextFlowDirectionsAttributeId
- UIA_UnderlineColorAttributeId
- UIA_UnderlineStyleAttributeId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e84ba97b387097233b7a838fbe192585b9676b6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468771"
---
# <a name="text-attribute-identifiers"></a>Идентификаторы атрибутов текста

В этом разделе описываются именованные константы, используемые для определения текстовых атрибутов диапазона текста Microsoft UI Automation. Эти константы используются со следующими методами.

-   [**Итекстранжепровидер:: Финдаттрибуте**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**Итекстранжепровидер:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**Иуиаутоматионтекстранже:: Финдаттрибуте**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**Иуиаутоматионтекстранже:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)




| Константа/значение | Описание | 
|----------------|-------------|
| <span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt><dt>40042</dt></dl> | Определяет атрибут текста <strong>афтерпараграфспаЦинг</strong> , указывающий размер интервала после абзаца.<br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_AnimationStyleAttributeId</strong></dt><dt>40000</dt></dl> | Определяет атрибут текста <strong>аниматионстиле</strong> , указывающий тип анимации, применяемой к тексту. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>аниматионстиле</strong></a> . <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br /> | 
| <span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt><dt>40032</dt></dl> | Определяет атрибут текста <strong>аннотатионобжектс</strong> , который поддерживает массив интерфейсов <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2</strong></a> , по одному для каждого элемента в текущем текстовом диапазоне, который реализует шаблон элемента управления <a href="uiauto-implementingannotation.md">Annotation</a> . Каждый элемент может также реализовать другие шаблоны элементов управления, необходимые для описания заметки. Например, аннотация, которая является комментарием, также поддерживает шаблон элемента управления <a href="uiauto-implementingtextandtextrange.md">Text</a> . Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_UNKNOWN</strong><br /> Значение по умолчанию: пустой массив <br /> | 
| <span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationTypesAttributeId</strong></dt><dt>40031</dt></dl> | Определяет атрибут текста <strong>аннотатионтипес</strong> , который поддерживает список идентификаторов типов заметок для диапазона текста. Список возможных значений см. в разделе <a href="uiauto-annotation-type-identifiers.md"><strong>идентификаторы типов заметок</strong></a>. Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_ARRAY</strong> | <strong>VT_I4</strong><br /> Значение по умолчанию: пустой массив <br /> | 
| <span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_BackgroundColorAttributeId</strong></dt><dt>40001</dt></dl> | Определяет атрибут текста <strong>BackgroundColor</strong> , указывающий цвет фона текста. Этот атрибут указан как <a href="/windows/win32/gdi/colorref">COLORREF</a>; 32-разрядное значение, используемое для указания цвета RGB или RGBA. <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: 0 <br /> | 
| <span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt><dt>40041</dt></dl> | Определяет атрибут текста <strong>бефорепараграфспаЦинг</strong> , указывающий размер интервала перед абзацем.<br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_BulletStyleAttributeId</strong></dt><dt>40002</dt></dl> | Определяет атрибут текста <strong>буллетстиле</strong> , указывающий стиль маркеров, используемых в текстовом диапазоне. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>буллетстиле</strong></a> .<br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br /> | 
| <span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_CapStyleAttributeId</strong></dt><dt>40003</dt></dl> | Определяет атрибут текста <strong>капстиле</strong> , определяющий стиль капитализации для текста. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong>капстиле</strong></a> . <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br /> | 
| <span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl><dt><strong>UIA_CaretBidiModeAttributeId</strong></dt><dt>40039</dt></dl> | Определяет атрибут текста <strong>каретбидимоде</strong> , который указывает направление потока текста в текстовом диапазоне. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>каретбидимоде</strong></a> . Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br /> | 
| <span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl><dt><strong>UIA_CaretPositionAttributeId</strong></dt><dt>40038</dt></dl> | Определяет атрибут текста <strong>каретпоситион</strong> , который указывает, находится ли курсор в начале или в конце строки текста в диапазоне текста. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>каретпоситион</strong></a> . Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br /> | 
| <span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl><dt><strong>UIA_CultureAttributeId</strong></dt><dt>40004</dt></dl> | Определяет атрибут текста <strong>языка и региональных параметров</strong> , задающий языковой стандарт для текста по идентификатору локали (LCID). <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: языковой стандарт пользовательского интерфейса приложения<br /> | 
| <span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl><dt><strong>UIA_FontNameAttributeId</strong></dt><dt>40005</dt></dl> | Определяет атрибут текста <strong>FontName</strong> , который указывает имя шрифта. Примеры: "Arial Black"; «Arial Narrow». Строка имени шрифта не локализована. <br /> Тип варианта: <strong>VT_BSTR</strong><br /> Значение по умолчанию: пустая строка<br /> | 
| <span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl><dt><strong>UIA_FontSizeAttributeId</strong></dt><dt>40006</dt></dl> | Определяет атрибут текста <strong>FontSize</strong> , указывающий размер кегля шрифта. <br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl><dt><strong>UIA_FontWeightAttributeId</strong></dt><dt>40007</dt></dl> | Определяет атрибут текста <strong>FontWeight</strong> , который задает относительный штрих, толщину или полужирное начертание шрифта. Атрибут <strong>FontWeight</strong> моделируется после элемента <strong>Лфвеигхт</strong> структуры GDI <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> и связанных стандартов и может принимать одно из следующих значений:<ul><li>0 = <strong>DontCare</strong></li><li>100 = <strong>тонкий</strong></li><li>200 = <strong>тонкий</strong> или <strong>ултралигхт</strong></li><li>300 = <strong>светлое</strong></li><li>400 = <strong>Обычная</strong> или <strong>Обычная</strong></li><li>500 = <strong>средний</strong></li><li>600 = <strong>полужирный</strong></li><li>700 = <strong>полужирный</strong></li><li>800 = <strong>екстраболд</strong> или <strong>жирный</strong></li><li>900 = <strong>Высокая</strong> или <strong>черная</strong></li></ul><br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_ForegroundColorAttributeId</strong></dt><dt>40008</dt></dl> | Определяет атрибут текста <strong>ForegroundColor</strong> , указывающий цвет переднего плана текста. Этот атрибут указывается как <a href="/windows/win32/gdi/colorref">COLORREF</a>, 32-разрядное значение, используемое для указания цвета RGB или RGBA. <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl><dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt><dt>40009</dt></dl> | Определяет атрибут текста <strong>хоризонталтексталигнмент</strong> , который указывает, как текст выстраивается горизонтально. Этот атрибут указан как значение из перечисляемого типа <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>хоризонталтексталигнментенум</strong></a> . <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br /> | 
| <span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt><dt>40010</dt></dl> | Определяет атрибут текста <strong>индентатионфирстлине</strong> , указывающий, насколько далеко в точках для отступа первой строки абзаца. <br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationLeadingAttributeId</strong></dt><dt>40011</dt></dl> | Определяет атрибут текста <strong>индентатионлеадинг</strong> , который задает начальный отступ в пунктах. <br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationTrailingAttributeId</strong></dt><dt>40012</dt></dl> | Определяет атрибут текста <strong>индентатионтраилинг</strong> , который указывает отступ в конце в пунктах. <br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl><dt><strong>UIA_IsActiveAttributeId</strong></dt><dt>40036</dt></dl> | Определяет атрибут <strong>полнотекстовой текст</strong> , указывающий, имеет ли элемент управления, содержащий текстовый диапазон, фокус клавиатуры (<strong>true</strong>) или нет (<strong>false</strong>). Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_BOOL</strong><br /> Значение по умолчанию: <strong>false</strong><br /> | 
| <span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl><dt><strong>UIA_IsHiddenAttributeId</strong></dt><dt>40013</dt></dl> | Определяет атрибут « <strong>скрытый</strong> текст», который указывает, является ли текст скрытым (<strong>true</strong>) или видимым (<strong>false</strong>). <br /> Тип варианта: <strong>VT_BOOL</strong><br /> Значение по умолчанию: <strong>false</strong><br /> | 
| <span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl><dt><strong>UIA_IsItalicAttributeId</strong></dt><dt>40014</dt></dl> | Определяет атрибут текста « <strong>Italic</strong> », который указывает, является ли текст курсивом (<strong>true</strong>) или нет (<strong>false</strong>). <br /> Тип варианта: <strong>VT_BOOL</strong><br /> Значение по умолчанию: <strong>false</strong><br /> | 
| <span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl><dt><strong>UIA_IsReadOnlyAttributeId</strong></dt><dt>40015</dt></dl> | Определяет атрибут Text, <strong>доступный только для</strong> чтения (<strong>true</strong>), или может быть изменен (<strong>false</strong>). <br /> Тип варианта: <strong>VT_BOOL</strong><br /> Значение по умолчанию: <strong>false</strong><br /> | 
| <span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSubscriptAttributeId</strong></dt><dt>40016</dt></dl> | Определяет атрибут текста <strong>иссубскрипт</strong> , который указывает, является ли текст подстрочным (<strong>true</strong>) или нет (<strong>false</strong>). <br /> Тип варианта: <strong>VT_BOOL</strong><br /> Значение по умолчанию: <strong>false</strong><br /> | 
| <span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSuperscriptAttributeId</strong></dt><dt>40017</dt></dl> | Определяет атрибут текста <strong>иссуперскрипт</strong> , который указывает, является ли текст подстрочным (<strong>true</strong>) или нет (<strong>false</strong>). <br /> Тип варианта: <strong>VT_BOOL</strong><br /> Значение по умолчанию: <strong>false</strong><br /> | 
| <span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_LineSpacingAttributeId</strong></dt><dt>40040</dt></dl> | Определяет атрибут текста <strong>линеспаЦинг</strong> , определяющий интервал между строками текста.<br /> Тип варианта: <strong>VT_BSTR</strong><br /> Значение по умолчанию: "ЛинеспаЦингаттрибутедефаулт"<br /> | 
| <span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl><dt><strong>UIA_LinkAttributeId</strong></dt><dt>40035</dt></dl> | Определяет атрибут текста <strong>ссылки</strong> , который содержит интерфейс <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>иуиаутоматионтекстранже</strong></a> текстового диапазона, который является целевым объектом внутренней ссылки в документе. Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_UNKNOWN</strong><br /> Значение по умолчанию: <strong>null</strong><br /> | 
| <span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl><dt><strong>UIA_MarginBottomAttributeId</strong></dt><dt>40018</dt></dl> | Определяет атрибут текста <strong>MarginBottom</strong> , указывающий размер (в пунктах) нижнего поля, применяемого к странице, связанной с текстовым диапазоном. <br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginLeadingAttributeId</strong></dt><dt>40019</dt></dl> | Определяет атрибут текста <strong>маргинлеадинг</strong> , указывающий размер (в пунктах) начального поля, который применяется к странице, связанной с текстовым диапазоном. <br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTopAttributeId</strong></dt><dt>40020</dt></dl> | Определяет атрибут текста <strong>MarginTop</strong> , который задает размер (в пунктах) верхнего поля, применяемого к странице, связанной с текстовым диапазоном. <br /> Тип варианта: <strong>VT_R8</strong><br /> Значение ддефаулт: 0<br /> | 
| <span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTrailingAttributeId</strong></dt><dt>40021</dt></dl> | Определяет атрибут текста <strong>маргинтраилинг</strong> , указывающий размер (в пунктах) конечного поля, применяемого к странице, связанной с текстовым диапазоном. <br /> Тип варианта: <strong>VT_R8</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl><dt><strong>UIA_OutlineStylesAttributeId</strong></dt><dt>40022</dt></dl> | Определяет атрибут текста <strong>аутлинестилес</strong> , указывающий стиль контура текста. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>аутлинестилес</strong></a> . <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br /> | 
| <span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineColorAttributeId</strong></dt><dt>40023</dt></dl> | Определяет атрибут текста <strong>оверлинеколор</strong> , указывающий цвет декорирования текста. Этот атрибут указывается как <a href="/windows/win32/gdi/colorref">COLORREF</a>, 32-разрядное значение, используемое для указания цвета RGB или RGBA. <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineStyleAttributeId</strong></dt><dt>40024</dt></dl> | Определяет атрибут текста <strong>оверлинестиле</strong> , определяющий стиль декорирования текста. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>текстдекоратионлинестилинум</strong></a> . <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl><dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt><dt>40037</dt></dl> | Определяет атрибут текста <strong>селектионактивинд</strong> , который указывает положение курсора относительно текстового диапазона, представляющего текущий выделенный текст. Этот атрибут указан как значение из перечисления <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>активинд</strong></a> . Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br /> | 
| <span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughColorAttributeId</strong></dt><dt>40025</dt></dl> | Определяет атрибут текста <strong>стрикесраугхколор</strong> , указывающий цвет оформления текста зачеркивания. Этот атрибут указывается как <a href="/windows/win32/gdi/colorref">COLORREF</a>, 32-разрядное значение, используемое для указания цвета RGB или RGBA. <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt><dt>40026</dt></dl> | Определяет атрибут текста <strong>стрикесраугхстиле</strong> , определяющий стиль оформления текста зачеркивания. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>текстдекоратионлинестилинум</strong></a> . <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl><dt><strong>UIA_StyleIdAttributeId</strong></dt><dt>40034</dt></dl> | Определяет атрибут текста <strong>стилеид</strong> , который указывает, какие стили текста используются для текстового диапазона. Список возможных значений см. в разделе <a href="uiauto-style-identifiers.md"><strong>идентификаторы стилей</strong></a>. Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: 0 <br /> | 
| <span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl><dt><strong>UIA_StyleNameAttributeId</strong></dt><dt>40033</dt></dl> | Определяет атрибут текста <strong>stylename</strong> , который определяет локализованное имя текстового стиля, используемого для текстового диапазона. Поддерживается начиная с Windows 8.<br /> Тип варианта: <strong>VT_BSTR</strong><br /> Значение по умолчанию: пустая строка<br /> | 
| <span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl><dt><strong>UIA_TabsAttributeId</strong></dt><dt>40027</dt></dl> | Определяет атрибут текста <strong>табуляции</strong> , который представляет собой массив, указывающий позиции табуляции для текстового диапазона. Каждый элемент массива задает расстояние (в пунктах) от начального поля. <br /> Тип варианта: <strong> VT_ARRAY | VT_R8</strong><br /> Значение по умолчанию: пустой массив<br /> | 
| <span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl><dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt><dt>40028</dt></dl> | Определяет атрибут текста <strong>текстфловдиректионс</strong> , указывающий направление потока текста. Этот атрибут указывается как сочетание значений из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>фловдиректионс</strong></a> . <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br /> | 
| <span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineColorAttributeId</strong></dt><dt>40029</dt></dl> | Определяет атрибут текста <strong>ундерлинеколор</strong> , указывающий цвет оформления текста подчеркивания. Этот атрибут указывается как <a href="/windows/win32/gdi/colorref">COLORREF</a>, 32-разрядное значение, используемое для указания цвета RGB или RGBA. <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: 0<br /> | 
| <span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineStyleAttributeId</strong></dt><dt>40030</dt></dl> | Определяет атрибут текста <strong>ундерлинестиле</strong> , определяющий стиль оформления текста подчеркивания. Этот атрибут указан как значение из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>текстдекоратионлинестилинум</strong></a> . <br /> Тип варианта: <strong>VT_I4</strong><br /> Значение по умолчанию: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 




## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений XP \|\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2003 \|\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**Итекстранжепровидер:: Финдаттрибуте**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**Итекстранжепровидер:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**Иуиаутоматион:: Финдаттрибуте**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**Иуиаутоматион:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**Зрения**
</dt> <dt>

[Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
