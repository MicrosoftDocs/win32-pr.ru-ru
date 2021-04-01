---
description: 'Данные подписки находятся в каталоге COM+ подписки. Подписку можно создать с помощью средства администрирования "службы компонентов" или программно с помощью интерфейса Икомадминкаталог:: Инсталлкомпонент.'
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Подписки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262617"
---
# <a name="subscriptions"></a><span data-ttu-id="bae2e-104">Подписки</span><span class="sxs-lookup"><span data-stu-id="bae2e-104">Subscriptions</span></span>

<span data-ttu-id="bae2e-105">Данные подписки находятся в каталоге COM+ подписки.</span><span class="sxs-lookup"><span data-stu-id="bae2e-105">Subscription data resides in the subscription COM+ catalog.</span></span> <span data-ttu-id="bae2e-106">Подписку можно создать с помощью средства администрирования "службы компонентов" или программно с помощью интерфейса [**икомадминкаталог:: инсталлкомпонент**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) .</span><span class="sxs-lookup"><span data-stu-id="bae2e-106">A subscription can be created either by using the Component Services administrative tool or programmatically by using the [**ICOMAdminCatalog::InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) interface.</span></span>

<span data-ttu-id="bae2e-107">Коллекция [**субскриптионсфоркомпонент**](subscriptionsforcomponent.md) используется для добавления, удаления или изменения сведений, относящихся к подпискам.</span><span class="sxs-lookup"><span data-stu-id="bae2e-107">The [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection is used to add, delete, or change information pertaining to subscriptions.</span></span> <span data-ttu-id="bae2e-108">Коллекция **субскриптионсфоркомпонент** является дочерней коллекцией для компонента.</span><span class="sxs-lookup"><span data-stu-id="bae2e-108">The **SubscriptionsForComponent** collection is a child collection to a component.</span></span> <span data-ttu-id="bae2e-109">Чтобы добавить подписку, получите коллекцию **субскриптионсфоркомпонент** компонента и используйте метод [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) , чтобы добавить запись в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="bae2e-109">To add a subscription, get the component's **SubscriptionsForComponent** collection and use the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method to add an entry to the collection.</span></span> <span data-ttu-id="bae2e-110">Чтобы настроить различные свойства объекта Subscription, используйте свойство [**value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) .</span><span class="sxs-lookup"><span data-stu-id="bae2e-110">To set up the various properties of the subscription object, use the [**Value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) property.</span></span> <span data-ttu-id="bae2e-111">Чтобы сохранить изменения, используйте команду [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) в объекте коллекции **субскриптионсфоркомпонент** .</span><span class="sxs-lookup"><span data-stu-id="bae2e-111">To save the changes, use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the **SubscriptionsForComponent** collection object.</span></span>

<span data-ttu-id="bae2e-112">Можно также использовать средство администрирования служб компонентов, чтобы изменить некоторые, но не все свойства подписки.</span><span class="sxs-lookup"><span data-stu-id="bae2e-112">You can also use the Component Services administration tool to modify some, but not all, of the subscription properties.</span></span> <span data-ttu-id="bae2e-113">Подписки указывают следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="bae2e-113">Subscriptions specify the following information:</span></span>

-   <span data-ttu-id="bae2e-114">Удостоверение и расположение подписчика</span><span class="sxs-lookup"><span data-stu-id="bae2e-114">Identity and location of the subscriber</span></span>
-   <span data-ttu-id="bae2e-115">Метод доставки.</span><span class="sxs-lookup"><span data-stu-id="bae2e-115">Delivery method</span></span>
-   <span data-ttu-id="bae2e-116">Методы событий для доставки</span><span class="sxs-lookup"><span data-stu-id="bae2e-116">Event methods to deliver</span></span>
-   <span data-ttu-id="bae2e-117">Объект класса событий и свойство PublisherID компонента класса событий, из которого подписчик желает получать события</span><span class="sxs-lookup"><span data-stu-id="bae2e-117">Event class object and PublisherID property of an event class component from which the subscriber wants to receive events</span></span>

<span data-ttu-id="bae2e-118">Подписки существуют независимо от объектов класса событий.</span><span class="sxs-lookup"><span data-stu-id="bae2e-118">Subscriptions exist independently from event class objects.</span></span> <span data-ttu-id="bae2e-119">Вы можете отключить подписку, задав для свойства Enabled значение false.</span><span class="sxs-lookup"><span data-stu-id="bae2e-119">You can disable a subscription by setting the Enabled property to False.</span></span> <span data-ttu-id="bae2e-120">Отключенная подписка не вызывается событиями COM+.</span><span class="sxs-lookup"><span data-stu-id="bae2e-120">A disabled subscription is not called by COM+ Events.</span></span>

<span data-ttu-id="bae2e-121">Существуют следующие три типа подписок:</span><span class="sxs-lookup"><span data-stu-id="bae2e-121">The three types of subscriptions are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="bae2e-122"><span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Надежно</span><span class="sxs-lookup"><span data-stu-id="bae2e-122"><span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistent</span></span>
</dt> <dd>

<span data-ttu-id="bae2e-123">Постоянные подписки находятся в каталоге COM+ и не зависят от времени существования подписчика.</span><span class="sxs-lookup"><span data-stu-id="bae2e-123">Persistent subscriptions reside in the COM+ catalog and are independent from the subscriber's lifetime.</span></span> <span data-ttu-id="bae2e-124">Постоянные подписки сохранили перезагрузку системы.</span><span class="sxs-lookup"><span data-stu-id="bae2e-124">Persistent subscriptions survive a system restart.</span></span> <span data-ttu-id="bae2e-125">Как правило, постоянная подписка создается, когда приложение устанавливается на компьютере подписчика и удаляется при удалении приложения.</span><span class="sxs-lookup"><span data-stu-id="bae2e-125">Generally, a persistent subscription is created when an application is installed on a subscriber's computer and removed when the application is removed.</span></span> <span data-ttu-id="bae2e-126">После создания постоянной подписки события COM+ активируют подписчик каждый раз, когда в него должно быть доставлено событие.</span><span class="sxs-lookup"><span data-stu-id="bae2e-126">After a persistent subscription is created, COM+ Events activates the subscriber each time an event should be delivered to it.</span></span>

<span data-ttu-id="bae2e-127">Когда издатель создает и вызывает объект [класса событий](the-com--event-class-object.md) , объект ищет все постоянные подписки в каталоге COM+ и создает новый экземпляр каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="bae2e-127">When a publisher instantiates and makes a call on an [event class](the-com--event-class-object.md) object, the object looks for all the persistent subscriptions in the COM+ catalog and creates a new instance of each object.</span></span> <span data-ttu-id="bae2e-128">Процесс создания может быть либо прямым, либо через моникер для очередей компонентов.</span><span class="sxs-lookup"><span data-stu-id="bae2e-128">The creation process can be either direct or through a moniker for queued components.</span></span> <span data-ttu-id="bae2e-129">Укажите объект подписчика по свойству [**субскрибермоникер**](subscriptionsforcomponent.md) подписки.</span><span class="sxs-lookup"><span data-stu-id="bae2e-129">Specify the subscriber object by the [**SubscriberMoniker**](subscriptionsforcomponent.md) property of the subscription.</span></span> <span data-ttu-id="bae2e-130">Объекты подписчиков, созданные постоянной подпиской, всегда освобождаются после каждого вызова события.</span><span class="sxs-lookup"><span data-stu-id="bae2e-130">Subscriber objects created by a persistent subscription are always released after each event call.</span></span>

</dd> <dt>

<span data-ttu-id="bae2e-131"><span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Регулярные</span><span class="sxs-lookup"><span data-stu-id="bae2e-131"><span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transient</span></span>
</dt> <dd>

<span data-ttu-id="bae2e-132">Для временных подписок можно использовать коллекцию [**трансиентсубскриптионс**](transientsubscriptions.md) , родительский объект которых является объектом корневого каталога.</span><span class="sxs-lookup"><span data-stu-id="bae2e-132">For transient subscriptions, you can use the [**TransientSubscriptions**](transientsubscriptions.md) collection, whose parent object is the root catalog object.</span></span> <span data-ttu-id="bae2e-133">Временные подписки запрашивают событие для определенного объекта подписчика, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="bae2e-133">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="bae2e-134">Временные подписки хранятся в каталоге COM+, но подписка удаляется при остановке системы событий или операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bae2e-134">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="bae2e-135">В отличие от постоянных подписок, временные подписки привязаны к определенному объекту и хранятся только в системе событий.</span><span class="sxs-lookup"><span data-stu-id="bae2e-135">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="bae2e-136">Временные подписки могут быть более эффективными, чем постоянные подписки, но необходимо управлять жизненным циклом объектов.</span><span class="sxs-lookup"><span data-stu-id="bae2e-136">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span> <span data-ttu-id="bae2e-137">Сведения о регистрации временной подписки см. в разделе [регистрация временной подписки](registering-a-transient-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="bae2e-137">For information about registering a transient subscription, see [Registering a Transient Subscription](registering-a-transient-subscription.md).</span></span>

</dd> <dt>

<span data-ttu-id="bae2e-138"><span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>На пользователя</span><span class="sxs-lookup"><span data-stu-id="bae2e-138"><span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Per user</span></span>
</dt> <dd>

<span data-ttu-id="bae2e-139">Подписки на пользователя могут доставлять события только при входе подписчика на компьютер системы событий.</span><span class="sxs-lookup"><span data-stu-id="bae2e-139">Per User subscriptions can deliver events only when the subscriber is logged on to the event system's computer.</span></span> <span data-ttu-id="bae2e-140">Когда подписчик входит в систему, система событий включает все подписки, для которых установлен *флаг "* **значение true** ", а для параметра *username* — имя пользователя, выполнившего вход.</span><span class="sxs-lookup"><span data-stu-id="bae2e-140">When the subscriber logs on, the event system enables all subscriptions on which the *PerUser* flag is set to **TRUE** and *UserName* is set to the name of the user who is logged on.</span></span> <span data-ttu-id="bae2e-141">При выходе подписчика из системы подписки отключаются.</span><span class="sxs-lookup"><span data-stu-id="bae2e-141">When the subscriber logs off, the subscriptions are disabled.</span></span>

<span data-ttu-id="bae2e-142">Подписки на пользователя вступают в силу только в том случае, если издатель и подписчик находятся на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bae2e-142">Per User subscriptions are effective only when the publisher and subscriber are on the same computer.</span></span> <span data-ttu-id="bae2e-143">Вход и выход из системы обнаруживаются только на компьютере издателя, а не на компьютере, на котором находится объект подписчика.</span><span class="sxs-lookup"><span data-stu-id="bae2e-143">Logon and logoff are detected only at the publisher's computer—not the computer on which the subscriber object resides.</span></span>

</dd> </dl>

<span data-ttu-id="bae2e-144">Система событий использует мета-события для уведомления заинтересованных подписчиков при создании, изменении или удалении объектов класса событий или подписок.</span><span class="sxs-lookup"><span data-stu-id="bae2e-144">The event system uses meta-events to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span> <span data-ttu-id="bae2e-145">Чтобы получить метаданные из системы событий, приложения должны создать подписку, находящейся на компьютере системы событий и указывающую идентификатор интерфейса (IID \_ иевентобжектчанже).</span><span class="sxs-lookup"><span data-stu-id="bae2e-145">To receive meta-events from the event system, applications must create a subscription that resides on the event system's computer and that specifies the firing interface ID (IID\_IEventObjectChange).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bae2e-146">См. также</span><span class="sxs-lookup"><span data-stu-id="bae2e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae2e-147">Фильтрация событий в COM+</span><span class="sxs-lookup"><span data-stu-id="bae2e-147">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="bae2e-148">Публикация и доставка событий в COM+</span><span class="sxs-lookup"><span data-stu-id="bae2e-148">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="bae2e-149">Объект класса событий COM+</span><span class="sxs-lookup"><span data-stu-id="bae2e-149">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="bae2e-150">Использование событий COM+ с компонентами в очереди COM+</span><span class="sxs-lookup"><span data-stu-id="bae2e-150">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



