---
title: Интерфейсы обработки событий для клиентов
description: В этом разделе описываются интерфейсы обработки событий для неуправляемых клиентских приложений автоматизации пользовательского интерфейса.
ms.assetid: ce9c4044-f46b-42b7-af44-05aee728a0e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458be6fcf5ce47f285d46c0e61f80e0897f15613
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710133"
---
# <a name="event-handling-interfaces-for-clients"></a><span data-ttu-id="12eb5-103">Интерфейсы обработки событий для клиентов</span><span class="sxs-lookup"><span data-stu-id="12eb5-103">Event Handling Interfaces for Clients</span></span>

<span data-ttu-id="12eb5-104">В этом разделе описываются интерфейсы обработки событий для неуправляемых клиентских приложений автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="12eb5-104">This section describes the event handling interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12eb5-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="12eb5-105">In this section</span></span>



| <span data-ttu-id="12eb5-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="12eb5-106">Interface</span></span>                                                                                                              | <span data-ttu-id="12eb5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="12eb5-107">Description</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12eb5-108">**иуиаутоматиончанжесевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="12eb5-108">**IUIAutomationChangesEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationchangeseventhandler)<br/>                         | <span data-ttu-id="12eb5-109">Предоставляет метод для управления событиями Microsoft UI Automation, происходящими при изменении свойства.</span><span class="sxs-lookup"><span data-stu-id="12eb5-109">Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.</span></span><br/>                      |
| [<span data-ttu-id="12eb5-110">**иуиаутоматионевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="12eb5-110">**IUIAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)<br/>                                       | <span data-ttu-id="12eb5-111">Предоставляет метод для управления событиями автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="12eb5-111">Exposes a method to handle UI Automation events.</span></span><br/>                                                                      |
| [<span data-ttu-id="12eb5-112">**иуиаутоматионфокусчанжедевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="12eb5-112">**IUIAutomationFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)<br/>               | <span data-ttu-id="12eb5-113">Предоставляет метод для управления событиями, возникающими при переходе фокуса клавиатуры на другой элемент модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="12eb5-113">Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.</span></span><br/>     |
| [<span data-ttu-id="12eb5-114">**иуиаутоматионнотификатионевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="12eb5-114">**IUIAutomationNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)<br/>               | <span data-ttu-id="12eb5-115">Предоставляет метод для управления событиями уведомления автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="12eb5-115">Exposes a method to handle UI Automation notification events.</span></span><br/>                                                         |
| [<span data-ttu-id="12eb5-116">**иуиаутоматионпропертичанжедевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="12eb5-116">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)<br/>         | <span data-ttu-id="12eb5-117">Предоставляет метод для управления событиями автоматизации пользовательского интерфейса, происходящих при изменении свойства.</span><span class="sxs-lookup"><span data-stu-id="12eb5-117">Exposes a method to handle UI Automation events that occur when a property is changed.</span></span><br/>                                |
| [<span data-ttu-id="12eb5-118">**иуиаутоматионструктуречанжедевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="12eb5-118">**IUIAutomationStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler)<br/>       | <span data-ttu-id="12eb5-119">Предоставляет метод для управления событиями, происходящими при изменении древовидной структуры модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="12eb5-119">Exposes a method to handle events that occur when the UI Automation tree structure is changed.</span></span><br/>                        |
| [<span data-ttu-id="12eb5-120">**иуиаутоматионтекстедиттекстчанжедевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="12eb5-120">**IUIAutomationTextEditTextChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler)<br/> | <span data-ttu-id="12eb5-121">Предоставляет метод для управления событиями, происходящими, когда модель пользовательского интерфейса сообщает о событии изменения текста из элементов управления редактированием текста.</span><span class="sxs-lookup"><span data-stu-id="12eb5-121">Exposes a method to handle events that occur when UI Automation reports a text-changed event from text edit controls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="12eb5-122">См. также</span><span class="sxs-lookup"><span data-stu-id="12eb5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12eb5-123">Клиенты автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="12eb5-123">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





