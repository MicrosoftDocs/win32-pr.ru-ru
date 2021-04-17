---
description: При настройке компонента для объединения в пул COM+ будет поддерживать его экземпляры в пуле, что будет готово к активации любому клиенту, запрашивающему компонент. Все запросы на создание объектов будут обрабатываться диспетчером пула.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Как работает пул объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710739"
---
# <a name="how-object-pooling-works"></a><span data-ttu-id="bfeca-104">Как работает пул объектов</span><span class="sxs-lookup"><span data-stu-id="bfeca-104">How Object Pooling Works</span></span>

<span data-ttu-id="bfeca-105">При настройке компонента для объединения в пул COM+ будет поддерживать его экземпляры в пуле, что будет готово к активации любому клиенту, запрашивающему компонент.</span><span class="sxs-lookup"><span data-stu-id="bfeca-105">When you configure a component to be pooled, COM+ will maintain instances of it in a pool, ready to be activated for any client requesting the component.</span></span> <span data-ttu-id="bfeca-106">Все запросы на создание объектов будут обрабатываться диспетчером пула.</span><span class="sxs-lookup"><span data-stu-id="bfeca-106">Any object creation requests will be handled through the pool manager.</span></span>

<span data-ttu-id="bfeca-107">Пулы настраиваются и обслуживаются отдельно для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="bfeca-107">Pools are configured and maintained on a per-component basis.</span></span> <span data-ttu-id="bfeca-108">Пул состоит из однородных объектов, использующих один и тот же идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="bfeca-108">A pool consists of homogeneous objects that share the same CLSID.</span></span> <span data-ttu-id="bfeca-109">Единственным исключением являются объекты транзакций, для которых поддерживаются подгруппы, содержащие объекты, имеющие сходство транзакций, пока транзакция находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="bfeca-109">The only exception is for transactional objects, for which subpools are maintained containing objects that have transaction affinity while a transaction is pending.</span></span>

<span data-ttu-id="bfeca-110">При запуске приложения пул будет заполнен до минимального уровня, указанного администратором, при условии, что создание объекта завершится успешно.</span><span class="sxs-lookup"><span data-stu-id="bfeca-110">When the application starts, the pool will be populated up to the minimum level that you have administratively specified, as long as object creation succeeds.</span></span> <span data-ttu-id="bfeca-111">По мере того как клиентские запросы для компонента поступают в систему, они выполняются на основе первого поступления из пула.</span><span class="sxs-lookup"><span data-stu-id="bfeca-111">As client requests for the component come in, they are satisfied on a first-come first-served basis from the pool.</span></span> <span data-ttu-id="bfeca-112">Если объекты в пуле недоступны, а пул еще не находится на указанном максимальном уровне, то для клиента создается и активируется новый объект.</span><span class="sxs-lookup"><span data-stu-id="bfeca-112">If no pooled objects are available and the pool is not yet at its specified maximum level, a new object is created and activated for the client.</span></span>

<span data-ttu-id="bfeca-113">Когда пул достигает максимального уровня, клиентские запросы помещаются в очередь и получат первый доступный объект из пула.</span><span class="sxs-lookup"><span data-stu-id="bfeca-113">When the pool reaches its maximum level, client requests are queued and will receive the first available object from the pool.</span></span> <span data-ttu-id="bfeca-114">Количество объектов, включая активированные и отключенные, никогда не превысит максимальное значение пула.</span><span class="sxs-lookup"><span data-stu-id="bfeca-114">The number of objects, including both activated and deactivated, will never exceed the maximum pool value.</span></span> <span data-ttu-id="bfeca-115">Время ожидания запросов на создание объектов истечет через административно указанный период, чтобы можно было контролировать, как долго клиенты будут ожидать создания объектов.</span><span class="sxs-lookup"><span data-stu-id="bfeca-115">Object creation requests will time out after an administratively specified period so that you can control how long clients will wait for object creation.</span></span> <span data-ttu-id="bfeca-116">По истечении времени ожидания клиент получит сообщение об ошибке E \_ timeout из [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="bfeca-116">Upon a time-out failure, the client will get back the error E\_TIMEOUT from [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="bfeca-117">Когда это возможно, COM+ будет пытаться повторно использовать объект после его освобождения клиентом, пока пул не достигнет максимального уровня.</span><span class="sxs-lookup"><span data-stu-id="bfeca-117">Whenever possible, COM+ will attempt to reuse an object after a client releases it, until the pool reaches its maximum level.</span></span> <span data-ttu-id="bfeca-118">Объект отвечает за наблюдение за его состоянием, чтобы определить, можно ли его использовать повторно и вернуть соответствующее значение для [**IObjectControl:: канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="bfeca-118">The object is responsible for monitoring its state to determine whether it can be reused and should return an appropriate value for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="bfeca-119">При создании объекта в составе пула он объединяется в объект большего размера, который будет управлять временем существования объекта.</span><span class="sxs-lookup"><span data-stu-id="bfeca-119">When a pooled object is created, it is aggregated into a larger object that will manage the object's lifetime.</span></span> <span data-ttu-id="bfeca-120">Внешний объект вызывает методы [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) в нужное время в жизненном цикле объекта, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="bfeca-120">The outer object calls methods on [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) at appropriate times in the object's life cycle, as follows:</span></span>

-   <span data-ttu-id="bfeca-121">Метод [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) вызывается всякий раз, когда объект возвращается клиенту, активируется в определенном контексте.</span><span class="sxs-lookup"><span data-stu-id="bfeca-121">The [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) method is called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="bfeca-122">Метод [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) вызывается всякий раз, когда объект освобождается клиентом, или, в случае JIT-активируемого объекта, при деактивации.</span><span class="sxs-lookup"><span data-stu-id="bfeca-122">The [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) method is called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="bfeca-123">Метод [**канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) вызывается всякий раз, когда объект возвращается в общий пул.</span><span class="sxs-lookup"><span data-stu-id="bfeca-123">The [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) method is called whenever an object is to be returned to the general pool.</span></span> <span data-ttu-id="bfeca-124">Если объект обнаруживает, что некоторые повторно используемые ресурсы находятся в неправильном состоянии, он должен вернуть **значение false** для этого метода, и диспетчер пула удалит объект.</span><span class="sxs-lookup"><span data-stu-id="bfeca-124">If the object detects that some reusable resource is in a bad state, it should return **FALSE** for this method and the pool manager will discard the object.</span></span>

<span data-ttu-id="bfeca-125">Объект не обязательно должен реализовывать [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span><span class="sxs-lookup"><span data-stu-id="bfeca-125">An object does not necessarily need to implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="bfeca-126">В противном случае экземпляры всегда будут использоваться повторно, пока не будет достигнут максимальный уровень пула.</span><span class="sxs-lookup"><span data-stu-id="bfeca-126">If it does not, instances will always be reused, until the pool maximum level is reached.</span></span>

<span data-ttu-id="bfeca-127">Дополнительные сведения о настройке компонентов для объединения в пул см. в разделе [Настройка компонента для объединения в пул](configuring-a-component-to-be-pooled.md).</span><span class="sxs-lookup"><span data-stu-id="bfeca-127">For details about how to configure components to be pooled, see [Configuring a Component to Be Pooled](configuring-a-component-to-be-pooled.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfeca-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bfeca-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfeca-129">Строки конструктора объектов COM+</span><span class="sxs-lookup"><span data-stu-id="bfeca-129">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="bfeca-130">Управление временем существования и состоянием объекта</span><span class="sxs-lookup"><span data-stu-id="bfeca-130">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="bfeca-131">Повышение производительности с помощью пула объектов</span><span class="sxs-lookup"><span data-stu-id="bfeca-131">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="bfeca-132">Группирование транзакционных объектов в пул</span><span class="sxs-lookup"><span data-stu-id="bfeca-132">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="bfeca-133">Требования к объектам в пуле</span><span class="sxs-lookup"><span data-stu-id="bfeca-133">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
