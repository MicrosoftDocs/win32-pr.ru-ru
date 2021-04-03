---
description: 'События COM+ предоставляют два способа управления событиями, которые достигают подписчиков: фильтрацию и фильтрацию параметров издателя.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Фильтрация событий в COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807798"
---
# <a name="filtering-events-in-com"></a><span data-ttu-id="2afa6-103">Фильтрация событий в COM+</span><span class="sxs-lookup"><span data-stu-id="2afa6-103">Filtering Events in COM+</span></span>

<span data-ttu-id="2afa6-104">События COM+ предоставляют два способа управления событиями, которые достигают подписчиков: *фильтрацию* и *фильтрацию параметров* издателя.</span><span class="sxs-lookup"><span data-stu-id="2afa6-104">COM+ Events provides two ways to control which events reach which subscribers: *publisher filtering* and *parameter filtering*.</span></span>

## <a name="publisher-filtering"></a><span data-ttu-id="2afa6-105">Фильтрация издателя</span><span class="sxs-lookup"><span data-stu-id="2afa6-105">Publisher Filtering</span></span>

<span data-ttu-id="2afa6-106">Фильтрация издателя управляет порядком и срабатыванием метода события в объекте [класса событий](the-com--event-class-object.md) .</span><span class="sxs-lookup"><span data-stu-id="2afa6-106">Publisher filtering controls the order and firing of an event method by an [event class](the-com--event-class-object.md) object.</span></span> <span data-ttu-id="2afa6-107">Фильтрация издателя позволяет издателю определить, какие подписчики получают определенное событие.</span><span class="sxs-lookup"><span data-stu-id="2afa6-107">Publisher filtering allows the publisher to determine which subscribers receive a particular event.</span></span>

<span data-ttu-id="2afa6-108">Примером эффективного использования фильтрации издателя является обмен на фондовой бирже.</span><span class="sxs-lookup"><span data-stu-id="2afa6-108">An example of effective use of publisher filtering is that of a stock exchange.</span></span> <span data-ttu-id="2afa6-109">Большинству подписчиков нужно иметь представление о добавлении нового запаса.</span><span class="sxs-lookup"><span data-stu-id="2afa6-109">Most subscribers want to know when a new stock is added.</span></span> <span data-ttu-id="2afa6-110">Однако многие из этих же подписчиков могут не захотеть быть в курсе каждого изменения стоимости акций.</span><span class="sxs-lookup"><span data-stu-id="2afa6-110">However, many of these same subscribers may not want to know whenever each stock price changes.</span></span> <span data-ttu-id="2afa6-111">Фильтрация издателя обеспечивает детализацию, необходимую для эффективной доставки событий только тем подписчикам, которые хотят получить эти сведения.</span><span class="sxs-lookup"><span data-stu-id="2afa6-111">Publisher filtering provides the granularity required to effectively deliver events to only the subscribers who want this information.</span></span>

<span data-ttu-id="2afa6-112">При вызове метода для объекта класса событий «экземпляр» он собирает все фильтры издателя для этого метода.</span><span class="sxs-lookup"><span data-stu-id="2afa6-112">When a method is invoked on the instantiated event class object, it collects any publisher filters on that method.</span></span> <span data-ttu-id="2afa6-113">Фильтр заставляет объект события вызывать метод события для конкретного подписчика.</span><span class="sxs-lookup"><span data-stu-id="2afa6-113">The filter forces the event object to fire the event method to a specific subscriber.</span></span> <span data-ttu-id="2afa6-114">Фильтр определяет, какие подписки должны срабатывать и в каком порядке их запускать.</span><span class="sxs-lookup"><span data-stu-id="2afa6-114">The filter determines which subscriptions to fire and in which order to fire them.</span></span> <span data-ttu-id="2afa6-115">Например, фильтр может прочитать список подписок и создать заказ на основе некоторых критериев приложения, а затем вызвать подписчиков в таком порядке.</span><span class="sxs-lookup"><span data-stu-id="2afa6-115">For example, the filter could read the subscription list and create the order based on some application criteria and then call the subscribers in that order.</span></span>

<span data-ttu-id="2afa6-116">Подробные инструкции по созданию фильтра издателя см. в разделе [Создание фильтра издателя](creating-a-publisher-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2afa6-116">For detailed instructions on creating a publisher filter, see [Creating a Publisher Filter](creating-a-publisher-filter.md).</span></span>

## <a name="parameter-filtering"></a><span data-ttu-id="2afa6-117">Фильтрация параметров</span><span class="sxs-lookup"><span data-stu-id="2afa6-117">Parameter Filtering</span></span>

<span data-ttu-id="2afa6-118">В отличие от фильтрации издателя, служба событий COM+ предоставляет необязательную фильтрацию параметров подписчика для каждой подписки и вызов метода события.</span><span class="sxs-lookup"><span data-stu-id="2afa6-118">In contrast to publisher filtering, the COM+ Events service provides an optional subscriber parameter filtering for each subscription and each event method invocation.</span></span> <span data-ttu-id="2afa6-119">При фильтрации параметров свойство параметром filterCriteria подписки оценивается по параметрам метода события.</span><span class="sxs-lookup"><span data-stu-id="2afa6-119">Parameter filtering evaluates the subscription FilterCriteria property against the parameters of the event method.</span></span> <span data-ttu-id="2afa6-120">Этот тип фильтрации используется для каждого метода, каждой подписки и обеспечивает уровень фильтрации подписчиков в источнике событий.</span><span class="sxs-lookup"><span data-stu-id="2afa6-120">This type of filtering is used on a per-method, per-subscription basis and provides a level of subscriber filtering at the event source.</span></span> <span data-ttu-id="2afa6-121">Строка условий фильтра распознает операторы отношения для проверки равенства (=, = =,!,! =, ~, ~ =,  <>), вложенные круглые скобки, **а также логические** ключевые слова **и**, **или**.</span><span class="sxs-lookup"><span data-stu-id="2afa6-121">The filter criteria string recognizes relational operators for checking equality (=, ==, !, !=, ~, ~=, <>), nested parentheses, and logical keywords **AND**, **OR**, or **NOT**.</span></span>

<span data-ttu-id="2afa6-122">Фильтрация параметров происходит после фильтрации издателя и запуска объекта стандартного события для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="2afa6-122">Parameter filtering occurs after any publisher filtering and when the standard event object is fired for a given subscription.</span></span> <span data-ttu-id="2afa6-123">Если используется фильтрация издателя, Фильтрация параметров происходит только в том случае, если фильтр издателя вызывает [**ифирингконтрол:: фиресубскриптион**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span><span class="sxs-lookup"><span data-stu-id="2afa6-123">If publisher filtering is used, parameter filtering occurs only when the publisher filter invokes [**IFiringControl::FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span></span> <span data-ttu-id="2afa6-124">По этой причине фильтрация и фильтрация параметров издателя могут составляться вместе, но фильтрация издателя имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="2afa6-124">Because of this, publisher filtering and parameter filtering can compose together but publisher filtering takes precedence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2afa6-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2afa6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2afa6-126">Публикация и доставка событий в COM+</span><span class="sxs-lookup"><span data-stu-id="2afa6-126">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="2afa6-127">Подписки</span><span class="sxs-lookup"><span data-stu-id="2afa6-127">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="2afa6-128">Объект класса событий COM+</span><span class="sxs-lookup"><span data-stu-id="2afa6-128">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="2afa6-129">Использование событий COM+ с компонентами в очереди COM+</span><span class="sxs-lookup"><span data-stu-id="2afa6-129">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



