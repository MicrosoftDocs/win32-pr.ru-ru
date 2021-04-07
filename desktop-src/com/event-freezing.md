---
title: Замораживание события
description: Замораживание события
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888280"
---
# <a name="event-freezing"></a><span data-ttu-id="1a189-103">Замораживание события</span><span class="sxs-lookup"><span data-stu-id="1a189-103">Event Freezing</span></span>

<span data-ttu-id="1a189-104">Контейнер может уведомлять элемент управления о том, что он не готов к реагированию на события, вызывая [**метод интерфейса IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="1a189-104">A container can notify a control that it is not ready to respond to events by calling [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE**.</span></span> <span data-ttu-id="1a189-105">Он может разморозить события, вызвав **FreezeEvents** с **false**.</span><span class="sxs-lookup"><span data-stu-id="1a189-105">It can unfreeze the events by calling **FreezeEvents** with **FALSE**.</span></span> <span data-ttu-id="1a189-106">Когда контейнер замораживает события, он фиксирует обработку событий, а не события. то есть контейнер может по-прежнему принимать события, когда события заморожены.</span><span class="sxs-lookup"><span data-stu-id="1a189-106">When a container freezes events, it is freezing event processing, not event receiving; that is, a container can still receive events while events are frozen.</span></span> <span data-ttu-id="1a189-107">Если контейнер получает уведомление о событии, когда его события фиксируются, контейнер должен игнорировать событие.</span><span class="sxs-lookup"><span data-stu-id="1a189-107">If a container receives an event notification while its events are frozen, the container should ignore the event.</span></span> <span data-ttu-id="1a189-108">Другие действия не подходят.</span><span class="sxs-lookup"><span data-stu-id="1a189-108">No other action is appropriate.</span></span>

<span data-ttu-id="1a189-109">Элементу управления следует заметку о вызове контейнера [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) со значением **true** , если это важно для элемента управления о том, что событие не пропущено.</span><span class="sxs-lookup"><span data-stu-id="1a189-109">A control should take note of a container's call to [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE** if it is important to the control that an event is not missed.</span></span> <span data-ttu-id="1a189-110">Хотя обработка событий контейнера заморожена, элемент управления должен реализовать один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="1a189-110">While a container's event processing is frozen, a control should implement one of the following techniques:</span></span>

-   <span data-ttu-id="1a189-111">Инициируйте события в полном наборе знаний о том, что контейнер не будет предпринимать никаких действий.</span><span class="sxs-lookup"><span data-stu-id="1a189-111">Fire the events in the full knowledge that the container will take no action.</span></span>
-   <span data-ttu-id="1a189-112">Отменить все события, которые были бы вызваны элементом управления.</span><span class="sxs-lookup"><span data-stu-id="1a189-112">Discard all events that the control would have fired.</span></span>
-   <span data-ttu-id="1a189-113">Помещает все ожидающие события в очередь и запускает их после того, как контейнер вызвал [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) со значением **false**.</span><span class="sxs-lookup"><span data-stu-id="1a189-113">Queue up all pending events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>
-   <span data-ttu-id="1a189-114">Ставить в очередь только значимые или важные события и запускать их после того, как контейнер вызвал [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) со значением **false**.</span><span class="sxs-lookup"><span data-stu-id="1a189-114">Queue up only relevant or important events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>

<span data-ttu-id="1a189-115">Каждый прием приемлем и подходит в различных обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="1a189-115">Each technique is acceptable and appropriate in different circumstances.</span></span> <span data-ttu-id="1a189-116">Разработчик элемента управления отвечает за определение и реализацию соответствующего метода для функций элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1a189-116">The control developer is responsible for determining and implementing the appropriate technique for the control's functionality.</span></span>

 

 




