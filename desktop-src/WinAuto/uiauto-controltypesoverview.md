---
title: Общие сведения о типах элементов управления автоматизации пользовательского интерфейса
description: Типы элементов управления Microsoft UI Automation — это свойства, которые служат известными идентификаторами, которые указывают тип элемента управления, представляемого определенным элементом пользовательского интерфейса, например поле со списком или кнопку.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Модель автоматизации пользовательского интерфейса, общие сведения о типах элементов управления
- Модель автоматизации пользовательского интерфейса, свойство UIA_LocalizedControlTypePropertyId
- типы элементов управления, сведения
- типы элементов управления, реквизиты
- типы элементов управления, предварительные требования
- типы элементов управления, предопределенные
- типы элементов управления, UIA_LocalizedControlTypePropertyId свойство
- стандартные типы элементов управления
- UIA_LocalizedControlTypePropertyId, свойство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533209"
---
# <a name="ui-automation-control-types-overview"></a>Общие сведения о типах элементов управления автоматизации пользовательского интерфейса

Типы элементов управления Microsoft UI Automation — это свойства, которые служат известными идентификаторами, которые указывают тип элемента управления, представляемого определенным элементом пользовательского интерфейса, например поле со списком или кнопку. Клиентские приложения используют тип для определения возможностей элемента управления и для определения способа взаимодействия с ним.

В этом разделе содержатся следующие подразделы.

-   [Необходимые компоненты элементов управления автоматизации пользовательского интерфейса](#ui-automation-control-type-requisites)
-   [Свойство Локализедконтролтипе](#the-localizedcontroltype-property)
-   [Текущие типы элементов управления автоматизации пользовательского интерфейса](#current-ui-automation-control-types)
-   [См. также](#related-topics)

## <a name="ui-automation-control-type-requisites"></a>Необходимые компоненты элементов управления автоматизации пользовательского интерфейса

Каждый тип элемента управления модели автоматизации пользовательского интерфейса имеет набор связанных с ним условий. Когда поставщик присваивает элементу управления тип, поставщик должен обеспечить соответствие элемента управления всем условиям, связанным с этим типом элемента управления. Условия включают следующее.

-   Шаблоны элементов управления модели автоматизации пользовательского интерфейса: каждый тип элемента управления имеет набор шаблонов элементов управления, которые должен поддерживать элемент управления, необязательный набор и набор, который элемент управления не должен поддерживать.
-   Значения свойств автоматизации пользовательского интерфейса. Каждый тип элемента управления содержит набор свойств, которые должен поддерживать элемент управления.
-   События автоматизации пользовательского интерфейса. Каждый тип элемента управления содержит набор событий, которые должен поддерживать элемент управления.
-   Дерево автоматизации пользовательского интерфейса. Каждый тип элемента управления определяет порядок отображения элемента управления в дереве автоматизации пользовательского интерфейса.

Если элемент управления удовлетворяет условиям для определенного типа элемента управления, значение свойства [**иуиаутоматионелемент:: куррентконтролтипе**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (или [**Иуиаутоматионелемент:: качедконтролтипе**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) будет означать, что тип элемента управления.

Если элемент управления не соответствует спецификациям для конкретного типа элемента управления, используйте [**UIA \_ кустомконтролтипеид**](uiauto-controltype-ids.md) в качестве идентификатора типа элемента управления и полностью Опишите элемент управления с помощью соответствующих шаблонов элементов управления и свойств. Можно также задать для свойства [**UIA \_ локализедконтролтипепропертид**](uiauto-automation-element-propids.md) строку, которая лучше описывает тип элемента управления.

## <a name="the-localizedcontroltype-property"></a>Свойство Локализедконтролтипе

Если для описания элемента управления используется стандартный тип элемента управления, используйте значение по умолчанию для свойства [**UIA \_ локализедконтролтипепропертид**](uiauto-automation-element-propids.md) и позвольте автоматизации пользовательского интерфейса предоставить локализованную строку для правильного предоставления поставщикам. Если для описания элемента управления нельзя использовать стандартный тип элемента управления, задайте для свойства **UIA \_ локализедконтролтипепропертид** локализованную строку, которая точно описывает тип элемента управления. Строка должна быть краткой, но достаточно точной, чтобы с помощью вспомогательной технологии, такой как средство чтения с экрана, можно было использовать его в пользовательском интерфейсе для информирования пользователя о типе элемента управления.

## <a name="current-ui-automation-control-types"></a>Текущие типы элементов управления автоматизации пользовательского интерфейса

В следующих разделах описываются типы элементов управления модели автоматизации пользовательского интерфейса. Для каждого типа элемента управления описание включает набор условий, которые должен поддерживать элемент управления данного типа:

-   Тип элемента управления панель приложений
-   [Тип элемента управления Button](uiauto-supportbuttoncontroltype.md)
-   [Тип элемента управления Calendar](uiauto-supportcalendarcontroltype.md)
-   [Тип элемента управления CheckBox](uiauto-supportcheckboxcontroltype.md)
-   [Тип элемента управления ComboBox](uiauto-supportcomboboxcontroltype.md)
-   [Тип элемента управления DataGrid](uiauto-supportdatagridcontroltype.md)
-   [Тип элемента управления DataItem](uiauto-supportdataitemcontroltype.md)
-   [Тип элемента управления документом](uiauto-supportdocumentcontroltype.md)
-   [Изменить тип элемента управления](uiauto-supporteditcontroltype.md)
-   [Тип элемента управления Group](uiauto-supportgroupcontroltype.md)
-   [Тип элемента управления "заголовок"](uiauto-supportheadercontroltype.md)
-   [Тип элемента управления HeaderItem](uiauto-supportheaderitemcontroltype.md)
-   [Тип элемента управления HyperLink](uiauto-supporthyperlinkcontroltype.md)
-   [Тип элемента управления Image](uiauto-supportimagecontroltype.md)
-   [Тип элемента управления List](uiauto-supportlistcontroltype.md)
-   [Тип элемента управления ListItem](uiauto-supportlistitemcontroltype.md)
-   [Тип элемента управления Menu](uiauto-supportmenucontroltype.md)
-   [Тип элемента управления MenuBar](uiauto-supportmenubarcontroltype.md)
-   [Тип элемента управления MenuItem](uiauto-supportmenuitemcontroltype.md)
-   [Тип элемента управления панели](uiauto-supportpanecontroltype.md)
-   [Тип элемента управления ProgressBar](uiauto-supportprogressbarcontroltype.md)
-   [Тип элемента управления RadioButton](uiauto-supportradiobuttoncontroltype.md)
-   [Тип элемента управления ScrollBar](uiauto-supportscrollbarcontroltype.md)
-   [Тип элемента управления Семантикзум](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [Тип элемента управления Separator](uiauto-supportseparatorcontroltype.md)
-   [Тип элемента управления Slider](uiauto-supportslidercontroltype.md)
-   [Тип элемента управления "Счетчик"](uiauto-supportspinnercontroltype.md)
-   [Тип элемента управления SplitButton](uiauto-supportsplitbuttoncontroltype.md)
-   [Тип элемента управления StatusBar](uiauto-supportstatusbarcontroltype.md)
-   [Тип элемента управления Tab](uiauto-supporttabcontroltype.md)
-   [Тип элемента управления TabItem](uiauto-supporttabitemcontroltype.md)
-   [Тип элемента управления Table](uiauto-supporttablecontroltype.md)
-   [Тип элемента управления "текст"](uiauto-supporttextcontroltype.md)
-   [Тип элемента управления Thumb](uiauto-supportthumbcontroltype.md)
-   [Тип элемента управления "заголовок"](uiauto-supporttitlebarcontroltype.md)
-   [Тип элемента управления ToolBar](uiauto-supporttoolbarcontroltype.md)
-   [Тип элемента управления ToolTip](uiauto-supporttooltipcontroltype.md)
-   [Тип элемента управления "дерево"](uiauto-supporttreecontroltype.md)
-   [Тип элемента управления TreeItem](uiauto-supporttreeitemcontroltype.md)
-   [Тип элемента управления окна](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Идентификаторы типов элементов управления](uiauto-controltype-ids.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Поддержка типов элементов управления модели автоматизации пользовательского интерфейса](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[Поддержка автоматизации пользовательского интерфейса для стандартных элементов управления](uiauto-controlsupport.md)
</dt> <dt>

[Основы модели автоматизации пользовательского интерфейса](entry-uiautocore-overview.md)
</dt> </dl>

 

 