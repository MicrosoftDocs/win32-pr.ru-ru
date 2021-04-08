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
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774876"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Основные сведения об объектной модели текста автоматизации пользовательского интерфейса

В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт обращаются к текстовому содержимому элемента управления на основе текста.

-   [Объектная модель для конкретного элемента управления](#control-specific-object-model)
-   [См. также](#related-topics)

Текстовые элементы управления предоставляют текстовое содержимое в клиентские приложения автоматизации пользовательского интерфейса через простую объектную модель текста. Клиентские приложения имеют доступ к объектной модели Text через интерфейсы шаблонов элементов управления [Text и TextRange](uiauto-about-text-and-textrange-patterns.md) , включая [**иуиаутоматионтекстпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) и [**иуиаутоматионтекстранже**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange). Клиентские приложения могут использовать эти интерфейсы для получения текстового содержимого, текстовых атрибутов и внедренных объектов, таких как таблицы и гиперссылки, из текстовых элементов управления.

Типы элементов управления, поддерживающие модель объектов текста модели автоматизации пользовательского интерфейса, включают в себя типы [Edit](uiauto-supporteditcontroltype.md) и [Document](uiauto-supportdocumentcontroltype.md) Control. Другие типы элементов управления, такие как [ToolTip](uiauto-supporttooltipcontroltype.md) и [Text](uiauto-supporttextcontroltype.md) , могут также поддерживать объектную модель текста, но не обязательно должны.

> [!Note]  
> Объектная модель текста модели автоматизации пользовательского интерфейса не предоставляет средств для вставки или изменения текста. Однако некоторые элементы управления позволяют вставлять и изменять текст либо с помощью интерфейса [**иуиаутоматионвалуепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) , либо с помощью прямого ввода с клавиатуры.

 

## <a name="control-specific-object-model"></a>Объектная модель для конкретного элемента управления

Элемент управления на основе текста, реализующий собственный модель DOM (DOM), может предоставлять модель DOM путем реализации шаблона элемента управления [ObjectModel](uiauto-implementingobjectmodel.md) . Предоставление модели DOM может предоставить клиентским приложениям больший доступ к содержимому элемента управления на основе текста и управлять им.

Клиентское приложение может определить, реализует ли конкретный текстовый элемент управления модель DOM путем извлечения интерфейса [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) элемента управления. Затем вызовите метод [**иуиаутоматионелемент:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , указав идентификатор свойства [**UIA \_ исобжектмоделпаттернаваилаблепропертид**](uiauto-control-pattern-availability-propids.md) , и вариант, который получает значение true, если элемент управления реализует DOM.

Чтобы получить доступ к модели DOM, вызовите метод [**иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , указав идентификатор шаблона элемента управления [**UIA \_ обжектмоделпаттернид**](uiauto-controlpattern-ids.md) и переменную, которая получает интерфейс [**иуиаутоматионобжектмоделпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) . Вызовите метод [**иуиаутоматионобжектмоделпаттерн:: жетундерлингобжектмодел**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) , чтобы получить интерфейс DOM.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Шаблоны элементов управления Text и TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Работа с элементами управления на основе текста](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




