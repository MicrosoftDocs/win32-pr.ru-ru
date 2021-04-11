---
title: Интерфейсы условий свойств для клиентов
description: В этом разделе описываются интерфейсы условий свойств для клиентов автоматизации пользовательского интерфейса для приложений Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070093"
---
# <a name="property-condition-interfaces-for-clients"></a>Интерфейсы условий свойств для клиентов

В этом разделе описываются интерфейсы условий свойств для клиентов автоматизации пользовательского интерфейса для приложений Microsoft Win32.

## <a name="in-this-section"></a>Содержание раздела



| Интерфейс                                                                                  | Описание                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иуиаутоматионандкондитион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Предоставляет свойства и методы, которые клиентские приложения автоматизации пользовательского интерфейса Майкрософт могут использовать для получения сведений о условии свойства, основанного на и. <br/> |
| [**иуиаутоматионбулкондитион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Представляет условие, которое может иметь **значение true** (выбирает все элементы) или **false** (не выбирает элементов).<br/>                                           |
| [**иуиаутоматионкондитион**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Это основной интерфейс для условий, используемых для фильтрации при поиске элементов в дереве модели автоматизации пользовательского интерфейса.<br/>                                   |
| [**иуиаутоматионноткондитион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Представляет условие, которое является отрицательным для другого условия.<br/>                                                                                       |
| [**иуиаутоматионоркондитион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Представляет условие, состоящие из нескольких условий, по крайней мере одно из которых должно иметь значение true.<br/>                                                              |
| [**иуиаутоматионпропертикондитион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Представляет условие на основе значения свойства, используемого для поиска элементов модели автоматизации пользовательского интерфейса.<br/>                                                           |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Клиенты автоматизации пользовательского интерфейса](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

