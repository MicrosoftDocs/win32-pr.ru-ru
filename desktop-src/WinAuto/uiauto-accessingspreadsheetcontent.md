---
title: Доступ к содержимому электронной таблицы
description: В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт могут получать доступ к содержимому электронной таблицы.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- Клиенты, доступ к содержимому электронной таблицы
- Клиенты, текстовые элементы управления
- Клиенты, шаблон элемента управления электронной таблицы
- Клиенты, шаблон элемента управления Спреадшититем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09d34aeb484da056920a2b77d47ca199e11c00c99832412e9bf007807c49563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052352"
---
# <a name="accessing-spreadsheet-content"></a>Доступ к содержимому электронной таблицы

Текстовый элемент управления, содержащий электронную таблицу, может обеспечить клиентам доступ к содержимому, поддерживая шаблоны элементов управления [электронной таблицы](uiauto-implementingspreadsheet.md) и [спреадшититем](uiauto-implementingspreadsheetitem.md) . В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт могут получать доступ к содержимому электронной таблицы.

Чтобы определить, поддерживает ли текстовый элемент управления [электронную таблицу](uiauto-implementingspreadsheet.md) и шаблоны элементов управления [спреадшититем](uiauto-implementingspreadsheetitem.md) , сначала извлеките интерфейс [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) для элемента управления (см. раздел [Получение элементов модели автоматизации пользовательского интерфейса](uiauto-obtainingelements.md)). Затем вызовите метод [**иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , указав идентификатор шаблона элемента управления [**UIA \_ спреадшитпаттернид**](uiauto-controlpattern-ids.md) или [**UIA \_ спреадшититемпаттернид**](uiauto-controlpattern-ids.md), и вариант, который получает значение true, если элемент управления поддерживает определенный шаблон элемента управления.

Чтобы получить доступ к содержимому таблицы, извлеките интерфейс [**иуиаутоматионспреадшитпаттерн**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) , вызвав метод [**Иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) и указав [**UIA \_ спреадшитпаттернид**](uiauto-controlpattern-ids.md) в качестве идентификатора шаблона элемента управления. Затем используйте метод [**иуиаутоматионспреадшитпаттерн:: жетитембинаме**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) , чтобы получить интерфейс [**иуиаутоматионспреадшититем**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) для определенного элемента электронной таблицы (обычно это ячейка). Используйте свойства и методы интерфейса **иуиаутоматионспреадшититем** , чтобы получить формулу для ячейки и все заметки, связанные с ячейкой. Дополнительные сведения о заметках см [. в разделе Получение заметок.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Работа с элементами управления на основе текста](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 