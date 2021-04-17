---
title: Использование сборщика событий Windows
description: В этом разделе перечислены разделы, объясняющие задачи, которые можно выполнить с помощью пакета SDK сборщика событий Windows. Примеры кода и объяснения для всех задач включены в следующие разделы.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691204"
---
# <a name="using-windows-event-collector"></a><span data-ttu-id="7716f-104">Использование сборщика событий Windows</span><span class="sxs-lookup"><span data-stu-id="7716f-104">Using Windows Event Collector</span></span>

<span data-ttu-id="7716f-105">В этом разделе перечислены разделы, объясняющие задачи, которые можно выполнить с помощью пакета SDK сборщика событий Windows.</span><span class="sxs-lookup"><span data-stu-id="7716f-105">This section lists the topics that explain the tasks that can be accomplished using the Windows Event Collector SDK.</span></span> <span data-ttu-id="7716f-106">Примеры кода и объяснения для всех задач включены в следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="7716f-106">Code examples and explanations for all the tasks are included in each of the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7716f-107">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="7716f-107">In This Section</span></span>

-   [<span data-ttu-id="7716f-108">Создание подписки, инициированной сборщиком</span><span class="sxs-lookup"><span data-stu-id="7716f-108">Creating a Collector Initiated Subscription</span></span>](creating-an-event-collector-subscription.md)

    <span data-ttu-id="7716f-109">Содержит сведения и пример кода C++ для создания подписки, инициированной сборщиком.</span><span class="sxs-lookup"><span data-stu-id="7716f-109">Provides information and a C++ code example for creating a collector-initiated subscription.</span></span> <span data-ttu-id="7716f-110">Подписка, инициированная сборщиком, позволяет принимать события на локальном компьютере (сборщике событий), пересылаемые с удаленного компьютера (источника событий).</span><span class="sxs-lookup"><span data-stu-id="7716f-110">A collector-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source).</span></span>

-   [<span data-ttu-id="7716f-111">Настройка исходной подписки, инициированной источником</span><span class="sxs-lookup"><span data-stu-id="7716f-111">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)

    <span data-ttu-id="7716f-112">Содержит сведения и пример кода C++ для создания подписки, инициированной исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="7716f-112">Provides information and a C++ code example for creating a source-initiated subscription.</span></span> <span data-ttu-id="7716f-113">Подписка, инициированная источником, позволяет принимать события на локальном компьютере (сборщике событий), пересылаемые с удаленного компьютера (источника событий), не указывая источники событий в подписке.</span><span class="sxs-lookup"><span data-stu-id="7716f-113">A source-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source) without specifying the event sources in the subscription.</span></span>

-   [<span data-ttu-id="7716f-114">Добавление источника событий к подписке, инициированной сборщиком</span><span class="sxs-lookup"><span data-stu-id="7716f-114">Adding an Event Source to a Collector Initiated Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)

    <span data-ttu-id="7716f-115">Содержит сведения и пример кода C++ для добавления источника события (локального компьютера или удаленного компьютера) к подписке, инициированной сборщиком.</span><span class="sxs-lookup"><span data-stu-id="7716f-115">Provides information and a C++ code example for adding an event source (local computer or remote computer) to a collector-initiated subscription.</span></span> <span data-ttu-id="7716f-116">Подписка, инициированная сборщиком, не может начать сбор событий, пока в подписку не будет добавлен источник событий.</span><span class="sxs-lookup"><span data-stu-id="7716f-116">A collector initiated subscription cannot start collecting events until an event source is added to the subscription.</span></span>

-   [<span data-ttu-id="7716f-117">Создание подписок на события оборудования</span><span class="sxs-lookup"><span data-stu-id="7716f-117">Creating Hardware Event Subscriptions</span></span>](creating-hardware-event-subscriptions.md)

    <span data-ttu-id="7716f-118">Содержит сведения о создании подписки на события для получения событий оборудования с компьютера, на котором установлен контроллер управления основной платой (BMC).</span><span class="sxs-lookup"><span data-stu-id="7716f-118">Provides information about how to create an event subscription in order to receive hardware events from a computer that has a Baseboard Management Controller (BMC) installed.</span></span>

-   [<span data-ttu-id="7716f-119">Удаление подписки сборщика событий</span><span class="sxs-lookup"><span data-stu-id="7716f-119">Deleting an Event Collector Subscription</span></span>](deleting-an-event-collector-subscription.md)

    <span data-ttu-id="7716f-120">Содержит сведения и пример кода C++ для удаления подписки сборщика событий с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="7716f-120">Provides information and a C++ code example for deleting an Event Collector subscription from a local computer.</span></span>

-   [<span data-ttu-id="7716f-121">Отображение свойств подписки сборщика событий</span><span class="sxs-lookup"><span data-stu-id="7716f-121">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)

    <span data-ttu-id="7716f-122">Содержит сведения и пример кода C++ для отображения значений свойств подписки сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="7716f-122">Provides information and a C++ code example for displaying the property values of an Event Collector subscription.</span></span> <span data-ttu-id="7716f-123">Значения свойств могут предоставлять полезную информацию, такую как адреса источников событий, состояние подписки и источников событий, а также сведения о доставке событий.</span><span class="sxs-lookup"><span data-stu-id="7716f-123">Property values can provide useful information, such as the addresses of event sources, the status of the subscription and event sources, and information about how events are delivered.</span></span>

-   [<span data-ttu-id="7716f-124">Отображение состояния подписки сборщика событий</span><span class="sxs-lookup"><span data-stu-id="7716f-124">Displaying the Status of an Event Collector Subscription</span></span>](displaying-the-status-of-an-event-collector-subscription.md)

    <span data-ttu-id="7716f-125">Содержит сведения и пример кода C++ для отображения состояния времени выполнения источников событий, связанных с подпиской сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="7716f-125">Provides information and a C++ code example for displaying the run time status of events sources that are associated to an Event Collector subscription.</span></span> <span data-ttu-id="7716f-126">Это позволяет просматривать сообщения об ошибках, которые могут помочь в решении проблем, препятствующих пересылке событий источником событий.</span><span class="sxs-lookup"><span data-stu-id="7716f-126">This enables you to view error messages that can help solve problems, which prevent an event source from forwarding events.</span></span>

-   [<span data-ttu-id="7716f-127">Список подписок сборщика событий</span><span class="sxs-lookup"><span data-stu-id="7716f-127">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)

    <span data-ttu-id="7716f-128">Содержит сведения и пример кода C++ для перечисления подписок, существующих на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7716f-128">Provides information and a C++ code example for listing the subscriptions that exist on a local computer.</span></span> <span data-ttu-id="7716f-129">Вы можете использовать имена подписок, полученные с помощью этого примера, для удаления подписки, добавления источника событий в подписку, получения свойств подписки или просмотра состояния подписки.</span><span class="sxs-lookup"><span data-stu-id="7716f-129">You can use the subscription names that are obtained with this example to delete a subscription, add an event source to a subscription, retrieve the properties of a subscription, or view the status of a subscription.</span></span>

-   [<span data-ttu-id="7716f-130">Удаление источника событий из подписки, инициированной сборщиком</span><span class="sxs-lookup"><span data-stu-id="7716f-130">Removing an Event Source from a Collector Initiated Subscription</span></span>](removing-an-event-source-from-an-event-collector-subscription.md)

    <span data-ttu-id="7716f-131">Содержит сведения и пример кода C++ для удаления источника событий из подписки, инициированной сборщиком.</span><span class="sxs-lookup"><span data-stu-id="7716f-131">Provides information and a C++ code example for removing an event source from a collector-initiated subscription.</span></span> <span data-ttu-id="7716f-132">Источник событий можно удалить из подписки, инициированной сборщиком, без отключения подписки.</span><span class="sxs-lookup"><span data-stu-id="7716f-132">You can remove an event source from a collector-initiated subscription without disabling the subscription.</span></span>

-   [<span data-ttu-id="7716f-133">Повторная попытка подписки сборщика событий</span><span class="sxs-lookup"><span data-stu-id="7716f-133">Retrying an Event Collector Subscription</span></span>](retrying-an-event-collector-subscription.md)

    <span data-ttu-id="7716f-134">Содержит сведения и пример кода C++ для повторной попытки подписки сборщика событий в случае сбоя одного или нескольких источников событий.</span><span class="sxs-lookup"><span data-stu-id="7716f-134">Provides information and a C++ code example for retrying an Event Collector subscription when one or more event sources have failed.</span></span> <span data-ttu-id="7716f-135">Вы можете повторить попытку одного источника событий или повторить всю подписку.</span><span class="sxs-lookup"><span data-stu-id="7716f-135">You can retry a single event source or you can retry the entire subscription.</span></span>

 

 




