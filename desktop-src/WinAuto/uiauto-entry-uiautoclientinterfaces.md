---
title: Интерфейсы элементов модели автоматизации пользовательского интерфейса для клиентов
description: В этом разделе описываются интерфейсы, используемые клиентом Microsoft UI Automation для поиска, доступа и запроса элементов автоматизации пользовательского интерфейса.
ms.assetid: dd7cdcf1-3511-424f-b729-b71a7e11cdd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a08859784d18905adbed463ac776bb2e717211f
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "103989880"
---
# <a name="ui-automation-element-interfaces-for-clients"></a>Интерфейсы элементов модели автоматизации пользовательского интерфейса для клиентов

В этом разделе описываются интерфейсы, используемые клиентом Microsoft UI Automation для поиска, доступа и запроса элементов автоматизации пользовательского интерфейса.

## <a name="in-this-section"></a>Содержание раздела



| Интерфейс                                                                        | Описание                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)<br/>                         | Предоставляет методы, позволяющие клиентским приложениям автоматизации пользовательского интерфейса обнаруживать, получать доступ и фильтровать элементы автоматизации пользовательского интерфейса. Модель автоматизации пользовательского интерфейса предоставляет каждый элемент модели автоматизации пользовательского интерфейса в виде объекта, представленного интерфейсом [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) . Элементы этого интерфейса не относятся к конкретному элементу.<br/> |
| [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2)<br/>                       | Расширяет интерфейс [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , чтобы предоставить дополнительные методы для управления функциональными возможностями автоматизации пользовательского интерфейса.<br/>                                                                                                                                                                                                   |
| [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3)<br/>                       | Расширяет интерфейс [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2) , чтобы предоставить дополнительные методы для управления функциональными возможностями автоматизации пользовательского интерфейса.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4)<br/>                       | Расширяет интерфейс [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3) , чтобы предоставить дополнительные методы для управления функциональными возможностями автоматизации пользовательского интерфейса.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5)<br/>                       | Расширяет интерфейс [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4) , чтобы предоставить дополнительные методы для управления функциональными возможностями автоматизации пользовательского интерфейса.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation6)<br/>                       | Расширяет интерфейс [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5) , чтобы предоставить дополнительные методы для управления функциональными возможностями автоматизации пользовательского интерфейса.<br/>                                                                                                                                                                                                 |
| [**иуиаутоматионкачерекуест**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest)<br/> | Обеспечивает доступ к свойствам и методам запроса кэша. Клиентские приложения используют этот интерфейс для указания свойств и шаблонов элементов управления, которые кэшируются при получении элемента модели автоматизации пользовательского интерфейса.<br/>                                                                                                                                                 |
| [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)<br/>           | Предоставляет методы и свойства для элемента модели автоматизации пользовательского интерфейса, представляющего элемент пользовательского интерфейса. <br/>                                                                                                                                                                                                                                                        |
| [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2)<br/>         | Расширяет интерфейс [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . <br/>                                                                                                                                                                                                                                                             |
| [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3)<br/>         | Расширяет интерфейс [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2) . <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4)<br/>         | Расширяет интерфейс [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3) . <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5)<br/>         | Расширяет интерфейс [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) для предоставления доступа к текущим и кэшированным данным ориентира.<br/>                                                                                                                                                                                                      |
| [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>         | Расширяет интерфейс [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5) для предоставления доступа к текущим и кэшированным полным описаниям.<br/>                                                                                                                                                                                                  |
| [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>         | Расширяет интерфейс [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6) .<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>         | Расширяет интерфейс [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7) .<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement9**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/>         | Расширяет интерфейс [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8) .<br/>                                                                                                                                                                                                                                                            |
| [**иуиаутоматионелементаррай**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)<br/> | Представляет коллекцию элементов модели автоматизации пользовательского интерфейса.<br/>                                                                                                                                                                                                                                                                                              |
| [**иуиаутоматионрегистрар**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar)<br/>       | Предоставляет методы для регистрации новых шаблонов элементов управления, свойств и событий.<br/>                                                                                                                                                                                                                                                                   |
| [**иуиаутоматионтривалкер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)<br/>     | Предоставляет свойства и методы, которые клиентские приложения модели автоматизации пользовательского интерфейса используют для просмотра элементов автоматизации пользовательского интерфейса на рабочем столе и навигации по ним. <br/>                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Клиенты автоматизации пользовательского интерфейса](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





