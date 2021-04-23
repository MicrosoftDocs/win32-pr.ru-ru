---
description: Основные понятия событий COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Основные понятия событий COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807966"
---
# <a name="com-events-concepts"></a><span data-ttu-id="ed709-103">Основные понятия событий COM+</span><span class="sxs-lookup"><span data-stu-id="ed709-103">COM+ Events Concepts</span></span>

<span data-ttu-id="ed709-104">Служба событий COM+ — это автоматизированная, *слабо связанная система событий* , которая хранит сведения о событиях от разных издателей в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="ed709-104">The COM+ events service is an automated, *loosely coupled event* system that stores event information from different publishers in the COM+ catalog.</span></span> <span data-ttu-id="ed709-105">Подписчики могут запрашивать это хранилище событий и выбирать события, о которых они хотят услышать.</span><span class="sxs-lookup"><span data-stu-id="ed709-105">Subscribers can query this event store and select the events that they want to hear about.</span></span>

> [!Note]  
> <span data-ttu-id="ed709-106">*Событие* определяется методом в интерфейсе COM+, называемом *методом события*, и порождено издателем и отправляется правильным подписчикам или подписчикам через службу событий COM+.</span><span class="sxs-lookup"><span data-stu-id="ed709-106">An *event* is identified by a method in a COM+ interface, known as an *event method*, and is originated by a publisher and dispatched to the correct subscriber or subscribers through the COM+ events service.</span></span> <span data-ttu-id="ed709-107">Методы событий должны иметь уникальные имена и могут содержать только входные параметры (без выходных или входных/выходных параметров).</span><span class="sxs-lookup"><span data-stu-id="ed709-107">Event methods must be uniquely named and can contain only input parameters (no output or input/output parameters).</span></span> <span data-ttu-id="ed709-108">Возвращаемое значение должно быть значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ed709-108">The return value must be an **HRESULT**.</span></span>

 

<span data-ttu-id="ed709-109">Служба событий COM+ обрабатывает большую часть семантики событий для издателя и подписчика.</span><span class="sxs-lookup"><span data-stu-id="ed709-109">The COM+ events service handles most of the event semantics for the publisher and subscriber.</span></span> <span data-ttu-id="ed709-110">Издатели предлагают публиковать типы событий, а подписчики — запросы типов событий от издателей.</span><span class="sxs-lookup"><span data-stu-id="ed709-110">Publishers offer to publish event types, and subscribers request event types from publishers.</span></span> <span data-ttu-id="ed709-111">В отличие от *тесно взаимосвязанных систем событий* , где издатели должны справляться с нагрузкой непосредственно вызывающими подписчиками, служба событий com+ обслуживает данные подписки в каталоге COM+ независимо от издателя и подписчика.</span><span class="sxs-lookup"><span data-stu-id="ed709-111">Unlike a *tightly coupled event* system, where publishers must handle the overhead of calling subscribers directly, the COM+ events service maintains subscription data in the COM+ catalog, independent of the publisher and subscriber.</span></span> <span data-ttu-id="ed709-112">Это упрощает модель программирования для издателя и подписчика, поскольку компоненту подписчика COM+ не требуется включать логику для создания подписок.</span><span class="sxs-lookup"><span data-stu-id="ed709-112">This simplifies the programming model for the publisher and subscriber because the COM+ subscriber component does not need to contain the logic for building subscriptions.</span></span>

<span data-ttu-id="ed709-113">Так как жизненный цикл данных подписки на события COM+ отделен от издателя или подписчика, подписки можно создавать до тех пор, пока не будут активными приложения подписчика или издателя.</span><span class="sxs-lookup"><span data-stu-id="ed709-113">Because the life cycle of the COM+ events subscription data is separate from that of either the publisher or the subscriber, subscriptions can be built prior to either the subscriber or the publisher applications being active.</span></span> <span data-ttu-id="ed709-114">Это также означает, что издатели и подписчики можно разрабатывать и развертывать отдельно.</span><span class="sxs-lookup"><span data-stu-id="ed709-114">This also means that publishers and subscribers can be developed and deployed separately.</span></span> <span data-ttu-id="ed709-115">Издатель может быть написан без знания числа и расположения подписчиков.</span><span class="sxs-lookup"><span data-stu-id="ed709-115">The publisher can be written without knowledge of the number and location of the subscribers.</span></span> <span data-ttu-id="ed709-116">Подписчики используют службу событий COM+ для поиска издателя и управления их подписками.</span><span class="sxs-lookup"><span data-stu-id="ed709-116">The subscribers use the COM+ Events service to find the publisher and manage their subscriptions.</span></span>

<span data-ttu-id="ed709-117">Следующие подразделы в этом разделе содержат подробные сведения об основных элементах службы событий COM+ и способах их использования.</span><span class="sxs-lookup"><span data-stu-id="ed709-117">The following topics in this section provide detailed information about the core elements of the COM+ events service and how to use them.</span></span>

-   [<span data-ttu-id="ed709-118">Объект класса событий COM+</span><span class="sxs-lookup"><span data-stu-id="ed709-118">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
-   [<span data-ttu-id="ed709-119">Подписки</span><span class="sxs-lookup"><span data-stu-id="ed709-119">Subscriptions</span></span>](subscriptions.md)
-   [<span data-ttu-id="ed709-120">Публикация и доставка событий в COM+</span><span class="sxs-lookup"><span data-stu-id="ed709-120">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
-   [<span data-ttu-id="ed709-121">Фильтрация событий в COM+</span><span class="sxs-lookup"><span data-stu-id="ed709-121">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
-   [<span data-ttu-id="ed709-122">Использование событий COM+ с компонентами в очереди COM+</span><span class="sxs-lookup"><span data-stu-id="ed709-122">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a><span data-ttu-id="ed709-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ed709-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed709-124">Вопросы безопасности событий COM+</span><span class="sxs-lookup"><span data-stu-id="ed709-124">COM+ Events Security Considerations</span></span>](com--events-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="ed709-125">Задачи событий COM+</span><span class="sxs-lookup"><span data-stu-id="ed709-125">COM+ Events Tasks</span></span>](com--events-tasks.md)
</dt> </dl>

 

 



