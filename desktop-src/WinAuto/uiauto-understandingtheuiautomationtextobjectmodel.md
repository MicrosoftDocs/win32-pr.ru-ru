---
title: Основные сведения об объектной модели текста автоматизации пользовательского интерфейса
description: В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт обращаются к текстовому содержимому элемента управления на основе текста.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- Клиенты, общие сведения о модели объектов текста автоматизации пользовательского интерфейса
- Клиенты, текстовые элементы управления
- Клиенты, текстовые диапазоны
- Клиенты, шаблон элемента управления Text
- Клиенты, шаблон элемента управления TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655f291e9cc11d925f947617fe31be96ebd81a2dbff73506a0e474dcde9e4446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823901"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Основные сведения об объектной модели текста автоматизации пользовательского интерфейса

В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт обращаются к текстовому содержимому элемента управления на основе текста.

-   [Объектная модель для конкретного элемента управления](#control-specific-object-model)
-   [Связанные темы](#related-topics)

Текстовые элементы управления предоставляют текстовое содержимое в клиентские приложения автоматизации пользовательского интерфейса через простую объектную модель текста. Клиентские приложения имеют доступ к объектной модели Text через интерфейсы шаблонов элементов управления [Text и TextRange](uiauto-about-text-and-textrange-patterns.md) , включая [**иуиаутоматионтекстпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) и [**иуиаутоматионтекстранже**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange). Клиентские приложения могут использовать эти интерфейсы для получения текстового содержимого, текстовых атрибутов и внедренных объектов, таких как таблицы и гиперссылки, из текстовых элементов управления.

Типы элементов управления, поддерживающие модель объектов текста модели автоматизации пользовательского интерфейса, включают в себя типы [Edit](uiauto-supporteditcontroltype.md) и [Document](uiauto-supportdocumentcontroltype.md) Control. Другие типы элементов управления, такие как [ToolTip](uiauto-supporttooltipcontroltype.md) и [Text](uiauto-supporttextcontroltype.md) , могут также поддерживать объектную модель текста, но не обязательно должны.

> [!Note]  
> Объектная модель текста модели автоматизации пользовательского интерфейса не предоставляет средств для вставки или изменения текста. Однако некоторые элементы управления позволяют вставлять и изменять текст либо с помощью интерфейса [**иуиаутоматионвалуепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) , либо с помощью прямого ввода с клавиатуры.

 

## <a name="control-specific-object-model"></a>Объектная модель для конкретного элемента управления

Элемент управления на основе текста, реализующий собственный модель DOM (DOM), может предоставлять модель DOM путем реализации шаблона элемента управления [ObjectModel](uiauto-implementingobjectmodel.md) . Предоставление модели DOM может предоставить клиентским приложениям больший доступ к содержимому элемента управления на основе текста и управлять им.

Клиентское приложение может определить, реализует ли конкретный текстовый элемент управления модель DOM путем извлечения интерфейса [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) элемента управления. Затем вызовите метод [**иуиаутоматионелемент:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , указав идентификатор свойства [**UIA \_ исобжектмоделпаттернаваилаблепропертид**](uiauto-control-pattern-availability-propids.md) , и вариант, который получает значение true, если элемент управления реализует DOM.

Чтобы получить доступ к модели DOM, вызовите метод [**иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , указав идентификатор шаблона элемента управления [**UIA \_ обжектмоделпаттернид**](uiauto-controlpattern-ids.md) и переменную, которая получает интерфейс [**иуиаутоматионобжектмоделпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) . Вызовите метод [**иуиаутоматионобжектмоделпаттерн:: жетундерлингобжектмодел**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) , чтобы получить интерфейс DOM.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Шаблоны элементов управления Text и TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Работа с элементами управления на основе текста](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




