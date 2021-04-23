---
description: Служба уведомлений о системных событиях работает с системой событий COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Архитектура Сенс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664212"
---
# <a name="sens-architecture"></a><span data-ttu-id="1a796-103">Архитектура Сенс</span><span class="sxs-lookup"><span data-stu-id="1a796-103">SENS Architecture</span></span>

<span data-ttu-id="1a796-104">Служба уведомлений о системных событиях работает с системой событий COM+.</span><span class="sxs-lookup"><span data-stu-id="1a796-104">The System Event Notification Service works with the COM+ Event System.</span></span> <span data-ttu-id="1a796-105">Сенс — это издатель событий для классов событий, которые он отслеживает: сеть, вход в систему и события питания/аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="1a796-105">SENS is an event publisher for the classes of events that it monitors: network, logon, and power/battery events.</span></span> <span data-ttu-id="1a796-106">Приложение, получающее уведомление, называется подписчиком на событие.</span><span class="sxs-lookup"><span data-stu-id="1a796-106">The application receiving a notification is called an event subscriber.</span></span>

<span data-ttu-id="1a796-107">Когда приложение подписывается на получение уведомлений, оно также может указывать фильтры, связанные с подписанными событиями.</span><span class="sxs-lookup"><span data-stu-id="1a796-107">When an application subscribes to receive notifications, it can also specify filters associated with the subscribed events.</span></span> <span data-ttu-id="1a796-108">События Сенс и COM+ используют фильтры, чтобы дополнительно определить, когда приложение должно получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="1a796-108">SENS and COM+ Events use the filters to further determine when the application should be notified.</span></span>

<span data-ttu-id="1a796-109">Уведомления являются асинхронными, поэтому приложение, получающее уведомление, не обязательно должно быть активным при отправке уведомления.</span><span class="sxs-lookup"><span data-stu-id="1a796-109">Notifications are asynchronous, so the application receiving the notification does not have to be active when the notification is sent.</span></span> <span data-ttu-id="1a796-110">Когда приложение подписывается на получение уведомлений, оно может указать, должно ли оно быть активировано при возникновении события или когда оно будет уведомлено позже, когда оно активно.</span><span class="sxs-lookup"><span data-stu-id="1a796-110">When an application subscribes to receive notifications, it can specify whether it should be activated when the event occurs or notified later when it is active.</span></span>

<span data-ttu-id="1a796-111">Подписка может быть временной и допустимой только до тех пор, пока приложение не будет остановлено или оно будет постоянным и действительным до тех пор, пока приложение не будет удалено из системы.</span><span class="sxs-lookup"><span data-stu-id="1a796-111">The subscription can be transient and valid only until the application stops running, or it can be persistent and valid until the application is removed from the system.</span></span>

<span data-ttu-id="1a796-112">Хранилище данных событий COM+ содержит сведения о издателе событий (Сенс), подписчиках событий и фильтрах.</span><span class="sxs-lookup"><span data-stu-id="1a796-112">A COM+ Events data store contains information about the event publisher (SENS), event subscribers, and filters.</span></span> <span data-ttu-id="1a796-113">Сенс также определяет исходящий интерфейс для каждого класса событий в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="1a796-113">SENS also predefines an outgoing interface for each event class in a type library.</span></span>



| <span data-ttu-id="1a796-114">Класс событий</span><span class="sxs-lookup"><span data-stu-id="1a796-114">Event class</span></span>    | <span data-ttu-id="1a796-115">Код GUID</span><span class="sxs-lookup"><span data-stu-id="1a796-115">GUID</span></span>                          | <span data-ttu-id="1a796-116">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="1a796-116">Interface</span></span>    |
|----------------|-------------------------------|--------------|
| <span data-ttu-id="1a796-117">Сетевые события</span><span class="sxs-lookup"><span data-stu-id="1a796-117">Network events</span></span> | <span data-ttu-id="1a796-118">\_сеть сенсгуид EVENTCLASS \_</span><span class="sxs-lookup"><span data-stu-id="1a796-118">SENSGUID\_EVENTCLASS\_NETWORK</span></span> | <span data-ttu-id="1a796-119">исенснетворк</span><span class="sxs-lookup"><span data-stu-id="1a796-119">ISensNetwork</span></span> |
| <span data-ttu-id="1a796-120">События входа</span><span class="sxs-lookup"><span data-stu-id="1a796-120">Logon events</span></span>   | <span data-ttu-id="1a796-121">\_Вход сенсгуид EVENTCLASS \_</span><span class="sxs-lookup"><span data-stu-id="1a796-121">SENSGUID\_EVENTCLASS\_LOGON</span></span>   | <span data-ttu-id="1a796-122">исенслогон</span><span class="sxs-lookup"><span data-stu-id="1a796-122">ISensLogon</span></span>   |
| <span data-ttu-id="1a796-123">События питания</span><span class="sxs-lookup"><span data-stu-id="1a796-123">Power events</span></span>   | <span data-ttu-id="1a796-124">СЕНСГУИД \_ EVENTCLASS \_ ONNOW</span><span class="sxs-lookup"><span data-stu-id="1a796-124">SENSGUID\_EVENTCLASS\_ONNOW</span></span>   | <span data-ttu-id="1a796-125">исенсоннов</span><span class="sxs-lookup"><span data-stu-id="1a796-125">ISensOnNow</span></span>   |



 

<span data-ttu-id="1a796-126">Чтобы получать уведомления для любого из этих событий, приложение должно выполнить два действия:</span><span class="sxs-lookup"><span data-stu-id="1a796-126">To receive notifications for any of these events, your application must do two things:</span></span>

-   <span data-ttu-id="1a796-127">Подпишитесь на интересующие вас события Сенс.</span><span class="sxs-lookup"><span data-stu-id="1a796-127">Subscribe to the SENS events that interest you.</span></span> <span data-ttu-id="1a796-128">Чтобы подписываться на событие, используйте интерфейсы **иевентсубскриптион** и **ИЕВЕНТСИСТЕМ** в событиях com+.</span><span class="sxs-lookup"><span data-stu-id="1a796-128">To subscribe to an event, use the **IEventSubscription** and **IEventSystem** interfaces in COM+ Events.</span></span> <span data-ttu-id="1a796-129">Необходимо указать идентификатор для классов событий и идентификатор издателя Сенс, СЕНСГУИД \_ Publisher.</span><span class="sxs-lookup"><span data-stu-id="1a796-129">You need to supply an identifier for the event classes and the SENS publisher identifier, SENSGUID\_PUBLISHER.</span></span> <span data-ttu-id="1a796-130">Подписки относятся к каждому уровню событий, поэтому приложение-подписчика должно также указывать, какие события в классе представляют интерес.</span><span class="sxs-lookup"><span data-stu-id="1a796-130">Subscriptions are on a per event level so the subscribing application must also specify which events within the class are of interest.</span></span> <span data-ttu-id="1a796-131">Каждое событие соответствует методу в интерфейсе, соответствующему его классу событий.</span><span class="sxs-lookup"><span data-stu-id="1a796-131">Each event corresponds to a method in the interface corresponding to its event class.</span></span>
-   <span data-ttu-id="1a796-132">Создайте объект приемника с реализацией для каждого интерфейса, который вы обрабатываете.</span><span class="sxs-lookup"><span data-stu-id="1a796-132">Create a sink object with an implementation for each interface that you handle.</span></span> <span data-ttu-id="1a796-133">Дополнительные сведения об этих интерфейсах и событиях, поддерживаемых в каждом из них, см. в разделе [**исенснетворк**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**исенслогон**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)и [**исенсоннов**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) .</span><span class="sxs-lookup"><span data-stu-id="1a796-133">See [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon), and [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) for more information about these interfaces and the events supported in each one.</span></span>

<span data-ttu-id="1a796-134">При возникновении одного из наблюдаемых событий Сенс обрабатывает каждую подписку со связанными фильтрами и уведомляет подписчиков через систему событий COM+.</span><span class="sxs-lookup"><span data-stu-id="1a796-134">When one of the monitored events occurs, SENS processes each subscription with any associated filters and notifies the subscribers through the COM+ Event system.</span></span>

 

 



