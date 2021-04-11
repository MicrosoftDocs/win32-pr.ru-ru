---
title: Идентификаторы свойств элементов автоматизации (UIAutomationClient. h)
description: В этом разделе описываются именованные константы, которые указывают свойства элементов модели автоматизации пользовательского интерфейса Майкрософт.
ms.assetid: f7613ad1-0b75-46fb-b9ac-b1ae9eea4193
topic_type:
- apiref
api_name:
- UIA_AcceleratorKeyPropertyId
- UIA_AccessKeyPropertyId
- UIA_AnnotationObjectsPropertyId
- UIA_AnnotationTypesPropertyId
- UIA_AriaPropertiesPropertyId
- UIA_AriaRolePropertyId
- UIA_AutomationIdPropertyId
- UIA_BoundingRectanglePropertyId
- UIA_CenterPointPropertyId
- UIA_ClassNamePropertyId
- UIA_ClickablePointPropertyId
- UIA_ControllerForPropertyId
- UIA_ControlTypePropertyId
- UIA_CulturePropertyId
- UIA_DescribedByPropertyId
- UIA_FillColorPropertyId
- UIA_FillTypePropertyId
- UIA_FlowsFromPropertyId
- UIA_FlowsToPropertyId
- UIA_FrameworkIdPropertyId
- UIA_FullDescriptionPropertyId
- UIA_HasKeyboardFocusPropertyId
- UIA_HeadingLevelPropertyId
- UIA_HelpTextPropertyId
- UIA_IsContentElementPropertyId
- UIA_IsControlElementPropertyId
- UIA_IsDataValidForFormPropertyId
- UIA_IsEnabledPropertyId
- UIA_IsKeyboardFocusablePropertyId
- UIA_IsOffscreenPropertyId
- UIA_IsPasswordPropertyId
- UIA_IsPeripheralPropertyId
- UIA_IsRequiredForFormPropertyId
- UIA_ItemStatusPropertyId
- UIA_ItemTypePropertyId
- UIA_LabeledByPropertyId
- UIA_LandmarkTypePropertyId
- UIA_LevelPropertyId
- UIA_LiveSettingPropertyId
- UIA_LocalizedControlTypePropertyId
- UIA_LocalizedLandmarkTypePropertyId
- UIA_NamePropertyId
- UIA_NativeWindowHandlePropertyId
- UIA_OptimizeForVisualContentPropertyId
- UIA_OrientationPropertyId
- UIA_OutlineColorPropertyId
- UIA_OutlineThicknessPropertyId
- UIA_PositionInSetPropertyId
- UIA_ProcessIdPropertyId
- UIA_ProviderDescriptionPropertyId
- UIA_RotationPropertyId
- UIA_RuntimeIdPropertyId
- UIA_SizePropertyId
- UIA_SizeOfSetPropertyId
- UIA_VisualEffectsPropertyId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c90b1a6d56fa62b6ddb241ce38c8cb2ae40afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137306"
---
# <a name="automation-element-property-identifiers"></a>Идентификаторы свойств элементов автоматизации

В этом разделе описываются именованные константы, которые указывают свойства элементов модели автоматизации пользовательского интерфейса Майкрософт.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>акцелераторкэй</strong> , которое представляет собой строку, содержащую сочетание клавиш быстрого вызова (также называемое клавишей быстрого доступа) для элемента автоматизации. <br/> Сочетания клавиш вызывают действие. Например, сочетание клавиш CTRL + O часто используется для вызова диалогового окна Открыть общий файл. Элемент автоматизации, имеющий свойство <strong>акцелераторкэй</strong> , может реализовать шаблон элемента управления <a href="uiauto-implementinginvoke.md">Invoke</a> для действия, которое эквивалентно команде shortcut.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>AccessKey</strong> , которое представляет собой строку, содержащую символ клавиши доступа для элемента автоматизации.<br/> Клавиша доступа (иногда называемая назначенной клавишей) — это символ в тексте меню, пункте меню или метке элемента управления, например кнопки, которая активирует связанную функцию меню. Например, чтобы открыть меню «файл», для которого клавиша доступа обычно имеет вид «F», пользователь нажмет клавиши ALT + F.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>аннотатионобжектс</strong> , которое представляет собой список объектов аннотации в документе, таких как комментарий, верхний колонтитул, Примечание и т. д.<br/> Тип варианта: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: пустой массив<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>аннотатионтипес</strong> , которое представляет собой список типов заметок в документе, таких как комментарий, заголовок, нижний колонтитул и т. д.<br/> Тип варианта: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: пустой массив<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>ариапропертиес</strong> , которое представляет собой отформатированную строку, содержащую сведения о доступном свойстве ARIA для элемента автоматизации. Дополнительные сведения о сопоставлении состояний ARIA и свойств со свойствами и функциями модели автоматизации пользовательского интерфейса см. в статье <a href="uiauto-ariaspecification.md">Модель автоматизации пользовательского интерфейса для спецификаций интернет приложений, доступных в общедоступной спецификации</a>.<br/> <strong>Ариапропертиес</strong> — это коллекция пар "имя-значение" с разделителями <strong>=</strong> (Equals) и <strong>;</strong> (точка с запятой), например &quot; checked = true; Disabled = false &quot; . <strong>\</strong>Обратная косая черта () используется в качестве escape-символа, если эти символы-разделители или <strong>\</strong> присутствуют в значениях. Для обеспечения безопасности и других причин реализация поставщика этого свойства может предпринять шаги для проверки исходных свойств ARIA. Однако это не обязательно.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>ариароле</strong> , которое представляет собой строку, содержащую доступные сведения о роли ARIA для элемента автоматизации. Дополнительные сведения о сопоставлении ролей ARIA с типами элементов управления модели автоматизации пользовательского интерфейса см. в статье <a href="uiauto-ariaspecification.md">Модель автоматизации пользовательского интерфейса для спецификаций веб приложений, доступных в консорциуме W3C</a>.<br/>
<blockquote>
[!Note]<br />
В качестве варианта агент пользователя также может предложить локализованное описание роли W3C ARIA в свойстве <strong>локализедконтролтипе</strong> . Если локализованная строка не указана, система предоставит строку <strong>локализедконтролтипе</strong> по умолчанию для элемента.
</blockquote>
<br/> <br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>AutomationId</strong> , которое представляет собой строку, содержащую идентификатор автоматизации пользовательского интерфейса (ID) для элемента автоматизации.<br/> Если он доступен, <strong>AutomationId</strong> элемента должен быть одинаковым в любом экземпляре приложения, независимо от локального языка. Значение должно быть уникальным среди элементов того же уровня, но не обязательно уникальным для всего рабочего стола. Например, несколько экземпляров приложения или несколько представлений папок в проводнике Microsoft Windows могут содержать элементы с одним и тем же свойством <strong>AutomationId</strong> , например &quot; системменубар &quot; .<br/> Хотя поддержка <strong>AutomationId</strong> всегда рекомендуется для улучшения поддержки автоматического тестирования, это свойство не является обязательным. Там, где он поддерживается, <strong>AutomationId</strong> полезен для создания скрипта автоматизации тестирования, который выполняется независимо от языка пользовательского интерфейса. Клиенты не должны делать никаких предположений относительно значений <strong>AutomationId</strong> , предоставляемых другими приложениями. <strong>AutomationId</strong> не гарантирует стабильной работы в разных выпусках или сборках приложения.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>баундингректангле</strong> , которое указывает координаты прямоугольника, полностью охватывающего элемент автоматизации. Прямоугольник выражается в координатах физического экрана. Он может содержать точки, которые не могут быть выбраны, если фигура или щелчок области элемента пользовательского интерфейса являются неравномерными, или если элемент скрыт другими элементами пользовательского интерфейса.<br/> Тип варианта: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: [0, 0, 0, 0]<br/>
<blockquote>
[!Note]<br />
Это свойство имеет <strong>значение NULL</strong> , если в данный момент элемент не отображается в пользовательском интерфейсе.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>центерпоинт</strong> , которое указывает координаты центральной точки X и Y элемента автоматизации. Пространство координат — это то, что поставщик логически считает страницу.<br/> Тип варианта: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>className</strong> , которое представляет собой строку, содержащую имя класса для элемента автоматизации, назначенное разработчиком элемента управления.<br/> Имя класса зависит от реализации поставщика автоматизации пользовательского интерфейса и, следовательно, не всегда в стандартном формате. Однако если имя класса известно, его можно использовать для проверки работы приложения с ожидаемым элементом автоматизации.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>кликкаблепоинт</strong> , которое является точкой на элементе автоматизации, которую можно щелкнуть. Нельзя щелкнуть элемент, если он полностью или частично скрыт другим окном.<br/> Тип варианта: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>контроллерфор</strong> , которое является массивом элементов автоматизации, которые управляются элементом автоматизации, поддерживающим это свойство.<br/> <strong>Контроллерфор</strong> используется, когда элемент автоматизации влияет на один или несколько сегментов пользовательского интерфейса приложения или рабочего стола; в противном случае трудно связать воздействие операции управления с элементами пользовательского интерфейса.<br/> Этот идентификатор обычно используется для <a href="/windows/uwp/design/accessibility/accessible-text-requirements">автоматического предложения специальных возможностей</a>.<br/> Тип варианта для поставщиков: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Тип варианта для клиентов: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>иуиаутоматионелементаррай</strong></a> )<br/> Значение по умолчанию: пустой массив<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>ControlType</strong> , которое является классом, идентифицирующим тип элемента автоматизации. <strong>ControlType</strong> определяет характеристики элементов пользовательского интерфейса с помощью хорошо известных примитивов элементов управления пользовательского интерфейса, таких как кнопка или флажок. <br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Используйте значение по умолчанию, только если элемент Automation представляет совершенно новый тип элемента управления.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>culture</strong> , которое содержит код локали для элемента автоматизации (например, <code>0x0409</code> для &quot; en-US &quot; или English (США)).<br/> Каждый языковой стандарт имеет уникальный идентификатор, 32-разрядное значение, состоящее из идентификатора языка и идентификатора порядка сортировки. Идентификатор локали является стандартным международным числовым сокращением и содержит компоненты, необходимые для уникальной идентификации одного из установленных языковых стандартов, определенных операционной системой. Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">константы и строки идентификатора языка</a>.<br/> Это свойство может существовать отдельно для каждого элемента управления, но обычно доступно только на уровне приложения.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>DescribedBy</strong> , которое представляет собой массив элементов, предоставляющий дополнительные сведения об элементе автоматизации.<br/> <strong>DescribedBy</strong> используется, когда элемент автоматизации объясняется другим СЕГМЕНТОМ пользовательского интерфейса приложения. Например, свойство может указывать на текстовый элемент &quot; 2 529 элементов в группах 85, 10 элементов, выбранных &quot; из сложного настраиваемого объекта списка. Вместо использования объектной модели для клиентов с целью дайджеста аналогичной информации свойство <strong>DescribedBy</strong> может предоставлять быстрый доступ к ЭЛЕМЕНТУ пользовательского интерфейса, который может уже предлагать полезные сведения для конечных пользователей, описывающих элемент пользовательского интерфейса.<br/> Тип варианта для поставщиков: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Тип варианта для клиентов: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>иуиаутоматионелементаррай</strong></a>)<br/> Значение по умолчанию: пустой массив<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>FillColor</strong> , которое указывает цвет, используемый для заполнения элемента автоматизации. Этот атрибут указывается как COLORREF, 32-разрядное значение, используемое для указания цвета RGB или RGBA.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>объекта FillType</strong> , которое указывает шаблон, используемый для заполнения элемента автоматизации, например "нет", "цвет", "градиент", "изображение", "шаблон" и т. д.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>фловсфром</strong> , которое представляет собой массив элементов автоматизации, которые предлагают порядок чтения перед текущим элементом автоматизации. Поддерживается начиная с Windows 8.<br/> Свойство <strong>фловсфром</strong> указывает порядок чтения, когда элементы автоматизации не предоставляются или не структурированы в том же порядке чтения, как это определено пользователем. Хотя свойство <strong>фловсфром</strong> может указывать несколько предшествующих элементов, оно обычно содержит только предыдущий элемент в порядке чтения.<br/> Тип варианта для поставщиков: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Тип варианта для клиентов: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>иуиаутоматионелементаррай</strong></a>)<br/> Значение по умолчанию: пустой массив<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>фловсто</strong> , которое представляет собой массив элементов автоматизации, который предлагает порядок чтения после текущего элемента автоматизации.<br/> Свойство <strong>фловсто</strong> указывает порядок чтения, когда элементы автоматизации не предоставляются или не структурированы в том же порядке чтения, как это определено пользователем. Хотя свойство <strong>фловсто</strong> может указывать несколько успешных элементов, оно обычно содержит только следующий элемент в порядке чтения.<br/> Тип варианта для поставщиков: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Тип варианта для клиентов: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>иуиаутоматионелементаррай</strong></a>)<br/> Значение по умолчанию: пустой массив<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>фрамеворкид</strong> , которое представляет собой строку, содержащую имя базовой платформы пользовательского интерфейса, к которой принадлежит элемент автоматизации.<br/> <strong>Фрамеворкид</strong> позволяет клиентским приложениям обрабатывать элементы автоматизации по-разному в зависимости от конкретной платформы пользовательского интерфейса. Примерами значений свойств могут служить &quot; Win32 &quot; , &quot; WinForm &quot; и &quot; директуи &quot; .<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td style="text-align: left;">Свойство <strong>фуллдескриптион</strong> предоставляет локализованную строку, которая может содержать расширенный текст описания для элемента. <strong>Фуллдескриптион</strong> может содержать более полное описание элемента, чем может быть подходящим для <strong>имени</strong>элемента.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>хаскэйбоардфокус</strong> , которое является логическим значением, указывающим, имеет ли элемент автоматизации фокус клавиатуры.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>хеадинглевел</strong> , которое указывает уровень заголовка элемента модели автоматизации пользовательского интерфейса.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>HELPTEXT</strong> , которое является строкой текста справки, связанной с элементом автоматизации.<br/> Свойство <strong>HELPTEXT</strong> может поддерживаться с текстом заполнителя, показываемым в элементах управления "Правка" или "список". Например, &quot; введите текст здесь для поиска &quot; — это хороший кандидат на свойство <strong>HELPTEXT</strong> для элемента управления Edit, который помещает текст перед фактическим входом пользователя. Однако он не подходит для свойства Name элемента управления Edit.<br/> Если поддерживается <strong>HELPTEXT</strong> , строка должна соответствовать языку пользовательского интерфейса приложения или языку пользовательского интерфейса по умолчанию операционной системы.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>исконтентелемент</strong> , которое является логическим значением, указывающим, отображается ли элемент в представлении содержимого дерева элементов автоматизации. Дополнительные сведения см. в разделе <a href="uiauto-treeoverview.md">Общие сведения о дереве автоматизации пользовательского интерфейса</a>.<br/>
<blockquote>
[!Note]<br />
Чтобы элемент отображался в представлении содержимого, свойство <strong>исконтентелемент</strong> и свойство <strong>Исконтролелемент</strong> должны иметь <strong>значение true</strong>.
</blockquote>
<br/> <br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>true</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>исконтролелемент</strong> , которое является логическим значением, указывающим, отображается ли элемент в представлении элемента управления дерева элементов автоматизации. Дополнительные сведения см. в разделе <a href="uiauto-treeoverview.md">Общие сведения о дереве автоматизации пользовательского интерфейса</a>.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>true</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>исдатавалидфорформ</strong> , которое является логическим значением, указывающим, допустимо ли указанное или выбранное значение для правила формы, связанного с элементом автоматизации. Например, если пользователь указал &quot; 425-555-5555 &quot; для поля почтового индекса, которое требует 5 или 9 цифр, свойство <strong>исдатавалидфорформ</strong> может иметь значение <strong>false</strong> , чтобы указать, что данные являются недопустимыми.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>

<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td style="text-align: left;">Определяет свойство " <strong>DIALOG</strong> ", которое является логическим значением, указывающим, является ли элемент автоматизации диалоговым окном. Например, такие специальные технологии, как средства чтения с экрана, обычно говорят о названии диалогового окна, элементе управления в диалоговом окне, а затем содержимом диалогового окна до элемента управления "элемент с сортировкой" ( &quot; сохранить изменения перед закрытием &quot; ). Для стандартных окон средство чтения с экрана обычно говорит заголовок окна, за которым следует элемент управления с упором. Для свойства <strong>«</strong> IsTrue» можно задать значение <strong>true</strong> , чтобы указать, что клиентское приложение должно обрабатывать элемент как диалоговое окно.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>

<tr class="even">
<td style="text-align: left;"><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>"Enabled",</strong> которое является логическим значением, указывающим, включен ли элемент пользовательского интерфейса, на который ссылается элемент автоматизации, с помощью которого можно взаимодействовать.<br/> Если включенное состояние элемента управления имеет <strong>значение false</strong>, предполагается, что дочерние элементы управления также не включены. Клиенты не должны ждать событий изменения свойств из дочерних элементов при изменении состояния родительского элемента управления.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>искэйбоардфокусабле</strong> , которое является логическим значением, указывающим, может ли элемент автоматизации принимать фокус клавиатуры.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>исоффскрин</strong> , которое является логическим значением, указывающим, полностью ли прокручивается элемент автоматизации (например, элемент в списке, находящийся за пределами окна просмотра объекта-контейнера) или свернутый из представления (например, элемент в представлении в виде дерева или меню или в свернутом окне). Если элемент имеет точку щелчка, которая может вызвать получение фокуса, элемент считается на экране, а часть элемента — вне экрана.<br/> Значение свойства не зависит от перекрытия другими окнами или от того, является ли элемент видимым на определенном мониторе.<br/> Если свойство <strong>исоффскрин</strong> имеет <strong>значение true</strong>, элемент пользовательского интерфейса прокручивается за пределы экрана или сворачивается. Элемент временно скрыт, но остается в восприятии конечного пользователя и продолжает включаться в модель пользовательского интерфейса. Объект можно вернуть в представление с помощью прокрутки, щелкнув раскрывающийся список и т. д.<br/> Объекты, которые конечный пользователь не воспринимает или &quot; программно скрывают &quot; (например, диалоговое окно, которое было закрыто, но базовый объект по-прежнему кэшируется приложением), не должен находиться в дереве элементов автоматизации в первую очередь (вместо установки состояния <strong>исоффскрин</strong> в <strong>true</strong>).<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td style="text-align: left;">Определяет свойство " <strong>Password</strong> ", которое является логическим значением, указывающим, содержит ли элемент автоматизации защищенное содержимое или пароль.<br/> Если свойство <strong></strong> <strong>IsTrue имеет значение true</strong> и элемент имеет фокус клавиатуры, то клиентское приложение должно отключить вывод клавиатуры или обратную связь ввода с клавиатуры, которая может предоставить защищенную информацию пользователя. Попытка доступа к свойству <strong>value</strong> защищенного элемента (элемент управления "поле ввода") может привести к возникновению ошибки.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td style="text-align: left;">Определяет свойство " <strong>периферию</strong> ", которое является логическим значением, указывающим, представляет ли элемент автоматизации Пользовательский интерфейс. Пользовательский интерфейс периферийных устройств отображается и поддерживает взаимодействие с пользователем, но не принимает фокус клавиатуры при появлении. Примерами пользовательского интерфейса периферийных устройств являются всплывающие окна, всплывающие подсказки, контекстные меню или плавающие уведомления. Поддерживается начиная с Windows 8.1.<br/> Если свойство « <strong>периферийное</strong> » имеет <strong>значение true</strong>, то клиентское приложение не может предположить, что фокус сделан элементом, даже если он в настоящее время является интерактивным.<br/> Это свойство относится к следующим типам элементов управления:<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>исрекуиредфорформ</strong> , которое является логическим значением, указывающим, должен ли элемент автоматизации заполняться в форме.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>итемстатус</strong> , которое представляет собой текстовую строку, описывающую состояние элемента элемента автоматизации.<br/> <strong>Итемстатус</strong> позволяет клиенту определить, передает ли элемент состояние элемента, а также состояние. Например, элемент, связанный с контактом в приложении для обмена сообщениями, может быть &quot; занят &quot; или &quot; подключен &quot; .<br/> Если <strong>итемстатус</strong> поддерживается, строка должна соответствовать языку пользовательского интерфейса приложения или языку пользовательского интерфейса по умолчанию операционной системы.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>ItemType</strong> , являющееся текстовой строкой, описывающей тип элемента автоматизации.<br/> <strong>ItemType</strong> используется для получения сведений о элементах в списке, представлении в виде дерева или сетке данных. Например, элемент в представлении каталога файлов может быть &quot; файлом документа &quot; или &quot; папкой &quot; .<br/> Если значение <strong>ItemType</strong> поддерживается, строка должна соответствовать языку пользовательского интерфейса приложения или языку пользовательского интерфейса по умолчанию операционной системы.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>лабеледби</strong> , которое является элементом автоматизации, содержащим текстовую метку для данного элемента.<br/> Это свойство может использоваться для получения, например, статической текстовой метки для поля со списком.<br/> Тип варианта: <strong>VT_UNKNOWN</strong><br/> Значение по умолчанию: <strong>null</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>ландмарктипе</strong> , которое является <a href="landmark-type-identifiers.md"><strong>идентификатором типа ориентира</strong></a> , связанным с элементом.<br/> Свойство <strong>ландмарктипе</strong> описывает элемент, представляющий группу элементов. Например, ориентир поиска может представлять набор связанных элементов управления для поиска.<br/> Если используется <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> , <strong>UIA_LocalizedLandmarkTypePropertyId</strong> требуется для описания пользовательского ориентира.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>Level</strong> , которое является целым числом, сопоставленным с элементом автоматизации, равным 1.<br/> Свойство <strong>Level</strong> описывает расположение элемента внутри иерархических или неработающих иерархических структур. Например, маркированный или нумерованный список, заголовки или другие элементы структурированных данных могут иметь различные связи типа «родители-потомки». <strong>Уровень</strong> . описывает, где в структуре находится элемент.<br/> Рекомендуется использовать <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">шаблон элемента управления кустомнавигатион</a> в сочетании с <strong>уровнем</strong>.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>LiveSetting</strong> , которое поддерживается элементом автоматизации, представляющим динамическую область. Свойство <strong>LiveSetting</strong> указывает уровень " &quot; мягкости" &quot; , который должен использоваться клиентом для уведомления пользователя об изменениях в динамической области. Это свойство может быть одним из значений перечисления <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>LiveSetting</strong></a> . Поддерживается начиная с Windows 8.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>локализедконтролтипе</strong> , являющееся текстовой строкой, описывающей тип элемента управления, представляемого элементом автоматизации. Строка должна содержать только символы нижнего регистра:
<ul>
<li>Исправить: &quot; кнопка&quot;</li>
<li>Ошибка: &quot; кнопка&quot;</li>
</ul>
<br/> Если поставщик элементов не указал <strong>локализедконтролтипе</strong> , локализованная строка по умолчанию предоставляется платформой в соответствии с типом элемента управления (например, &quot; кнопка &quot; для типа элемента управления <a href="uiauto-supportbuttoncontroltype.md">Button</a> ). Элемент автоматизации с типом <strong>пользовательского</strong> элемента управления должен поддерживать локализованную строку типа элемента управления, представляющую роль элемента (например, &quot; палитру цветов &quot; для пользовательского элемента управления, позволяющую пользователям выбирать и задавать цвета).<br/> Если указано пользовательское значение, строка должна соответствовать языку пользовательского интерфейса приложения или языку пользовательского интерфейса по умолчанию операционной системы.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td style="text-align: left;">Определяет <strong>локализедландмарктипе</strong>— текстовую строку, описывающую тип ориентира, который представляет элемент автоматизации.<br/> Его следует использовать в сочетании с <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> однако <strong>локализедландмарктипе</strong> должен всегда иметь приоритет над <strong>ландмарктипе</strong> и использоваться для описания ориентира перед <strong>ландмарктипе</strong>.<br/> Строка должна соответствовать языку пользовательского интерфейса приложения или языку пользовательского интерфейса по умолчанию операционной системы.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>Name</strong> , которое представляет собой строку, содержащую имя элемента автоматизации.<br/> Свойство <strong>Name</strong> должно быть таким же, как и текст метки на экране. Например, <strong>имя</strong> должно быть &quot; Просмотрено &quot; для элемента Button с меткой &quot; Обзор &quot; . Свойство <strong>Name</strong> не должно включать назначенный символ для клавиш доступа (то есть &quot; & &quot; ), который подчеркнут в текстовом представлении пользовательского интерфейса. Кроме того, свойство <strong>Name</strong> не должно быть расширенной или измененной версией метки на экране, так как несоответствие имени и метки может привести к путанице между клиентскими приложениями и пользователями.<br/> Если соответствующий текст метки не отображается на экране или заменяется графикой, следует выбрать альтернативный текст. Альтернативный текст должен быть кратким, интуитивно понятным и локализованным для языка пользовательского интерфейса приложения или языком пользовательского интерфейса по умолчанию операционной системы. Альтернативный текст не должен быть подробным описанием визуальных элементов, а краткое описание функции или функции пользовательского интерфейса, как если бы оно было помечено простым текстом. Например, кнопка меню Пуск Windows называется &quot; Start &quot; (кнопка) вместо &quot; эмблемы Windows на синей круглой сфере &quot; (кнопка). Дополнительные сведения см. в разделе <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">Создание текстовых эквивалентов для изображений</a>.<br/> Если в метке пользовательского интерфейса используется текстовая графика (например, при использовании &quot; >> &quot; для кнопки, добавляющей элемент слева направо), свойство <strong>Name</strong> должно быть переопределено соответствующим альтернативным текстом (например, &quot; Add &quot; ). Однако использование текстовых изображений в качестве метки пользовательского интерфейса не рекомендуется из-за особенностей локализации и доступности.<br/> Свойство <strong>Name</strong> не должно включать сведения о роли или типе элемента управления, например &quot; кнопку &quot; или &quot; список &quot; ; в противном случае он будет конфликтовать с текстом из свойства <strong>локализедконтролтипе</strong> , когда добавляются эти два свойства (многие существующие вспомогательные технологии делают это).<br/> Свойство <strong>Name</strong> не может использоваться в качестве уникального идентификатора среди одноуровневых элементов. Однако при условии, что она согласована с представлением пользовательского интерфейса, одно и то же значение <strong>имени</strong> может поддерживаться между одноранговыми узлами. Для автоматизации тестирования клиенты должны использовать свойство <strong>AutomationId</strong> или <strong>рунтимеид</strong> .<br/> Элементу управления "текст" не всегда обязательно иметь свойство <strong>Name</strong> , идентичное тексту, отображаемому в элементе управления, пока также поддерживается шаблон <strong>текста</strong> .<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>нативевиндовхандле</strong> , которое представляет собой целое число, представляющее дескриптор (<strong>HWND</strong>) окна элемента автоматизации, если оно существует; в противном случае это свойство равно 0.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>оптимизефорвисуалконтент</strong> , которое является логическим значением, указывающим, предоставляет ли поставщик только видимые элементы. Поставщик может использовать это свойство для оптимизации производительности при работе с очень большими фрагментами содержимого. Например, в качестве страницы пользователя с большим содержимым поставщик может удалить элементы содержимого, которые больше не видны. При уничтожении элемента содержимого поставщик должен вернуть код ошибки <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> . Поддерживается начиная с Windows 8.<br/> Тип варианта: <strong>VT_BOOL</strong><br/> Значение по умолчанию: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>Orientation</strong> , которое указывает ориентацию элемента управления, представленного элементом автоматизации. Свойство выражается как значение из перечисляемого типа <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>ориентатионтипе</strong></a> .<br/> Свойство <strong>Orientation</strong> поддерживается элементами управления, такими как полосы прокрутки и ползунки, которые могут иметь вертикальную или горизонтальную ориентацию. В противном случае он всегда может быть <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>. Это означает, что элемент управления не имеет ориентации.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>OutlineColor</strong> , которое указывает цвет, используемый для контура элемента автоматизации. Этот атрибут указывается как <strong>COLORREF</strong>, 32-разрядное значение, используемое для указания цвета RGB или RGBA.<br/> Тип варианта: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>OutlineThickness</strong> , которое задает ширину контура элемента автоматизации.<br/> Тип варианта: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>поситионинсет</strong> , которое является целым числом, связанным с элементом автоматизации, равным 1. <strong>Поситионинсет</strong> описывает порядковое расположение элемента в наборе элементов, которые считаются одноуровневыми элементами.<br/> <strong>Поситионинсет</strong> работает в координации со свойством <strong>sizeof</strong> , чтобы описать порядковое расположение в наборе.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>ProcessID</strong> , которое является целым числом, представляющим идентификатор процесса (ID) элемента автоматизации.<br/> Идентификатор процесса (ID) назначается операционной системой. Его можно просмотреть в столбце <strong>PID</strong> на вкладке <strong>процессы</strong> в диспетчере задач.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>ProviderDescription</strong> , которое представляет собой отформатированную строку, содержащую сведения об источнике поставщика автоматизации пользовательского интерфейса для элемента автоматизации, включая сведения о прокси-сервере.<br/> Тип варианта: <strong>VT_BSTR</strong><br/> Значение по умолчанию: пустая строка<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>вращения</strong> , которое указывает угол поворота в неуказанных единицах.<br/> Тип варианта: <strong>VT_R8</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>рунтимеид</strong> , которое представляет собой массив целых чисел, представляющих идентификатор элемента автоматизации.<br/> Идентификатор уникален на рабочем столе, но он гарантированно уникален только в пользовательском интерфейсе рабочего стола, на котором он был создан. Идентификаторы можно использовать повторно с течением времени.<br/> Формат <strong>рунтимеид</strong> может изменяться. Возвращенный идентификатор должен обрабатываться как непрозрачное значение и использоваться только для сравнения; Например, чтобы определить, находится ли элемент автоматизации в кэше.<br/> Тип варианта: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>size</strong> , которое задает ширину и высоту элемента автоматизации.<br/> Тип варианта: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Значение по умолчанию: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td style="text-align: left;">Идентифицирует свойство <strong>sizeof</strong> , которое является целым числом, сопоставленным с элементом автоматизации, равным 1. <strong>Sizeof</strong> описывает количество элементов автоматизации в группе или наборе, которые считаются элементами того же уровня.<br/> <strong>Sizeof</strong> работает в координации со свойством <strong>поситионинсет</strong> для описания количества элементов в наборе.<br/> Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td style="text-align: left;">Определяет свойство <strong>висуалеффектс</strong> , которое является битовым полем, которое определяет эффекты в элементе автоматизации, такие как тень, отражение, свечение, сглаженные края или Багетная рамка.<br/> Висуалеффектс:<br/>
<ul>
<li>VisualEffects_Shadow: 0x1</li>
<li>VisualEffects_Reflection: 0x2</li>
<li>VisualEffects_Glow: 0x4</li>
<li>VisualEffects_SoftEdges: 0x8</li>
<li>VisualEffects_Bevel: 0x10</li>
</ul>
Тип варианта: <strong>VT_I4</strong><br/> Значение по умолчанию: 0<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows XP \|\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2003 \|\]<br/>                                     |
| Header<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о свойствах автоматизированного пользовательского интерфейса](uiauto-propertiesoverview.md)
</dt> <dt>

[Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md)
</dt> </dl>
