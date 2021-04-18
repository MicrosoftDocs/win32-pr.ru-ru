---
description: Управление временем существования и состоянием объекта
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Управление временем существования и состоянием объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701239"
---
# <a name="controlling-object-lifetime-and-state"></a><span data-ttu-id="1589e-103">Управление временем существования и состоянием объекта</span><span class="sxs-lookup"><span data-stu-id="1589e-103">Controlling Object Lifetime and State</span></span>

<span data-ttu-id="1589e-104">Объект poold может принимать участие в том, как COM+ управляет своими действиями в пуле, реализуя [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span><span class="sxs-lookup"><span data-stu-id="1589e-104">A pooled object can participate in how COM+ manages its activity in the pool by implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="1589e-105">При создании объекта в составе пула он объединяется в более крупный объект, который будет управлять этим объектом, вызывая следующие методы в **IObjectControl** в обычных точках жизненного цикла объекта:</span><span class="sxs-lookup"><span data-stu-id="1589e-105">When a pooled object is created, it is aggregated into a larger object that will manage the object by calling the following methods on **IObjectControl** at regular points in the object's lifecycle:</span></span>

-   <span data-ttu-id="1589e-106">[**Активация**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)— вызывается при каждом возврате объекта клиенту, активированном в определенном контексте.</span><span class="sxs-lookup"><span data-stu-id="1589e-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—Called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="1589e-107">[**Деактивация —**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)вызывается всякий раз, когда объект освобождается клиентом, или, в случае JIT-активируемого объекта, при деактивации.</span><span class="sxs-lookup"><span data-stu-id="1589e-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—Called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="1589e-108">[**Канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)— вызывается каждый раз, когда объект возвращается в общий пул.</span><span class="sxs-lookup"><span data-stu-id="1589e-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—Called whenever an object is to be returned to the general pool.</span></span>

<span data-ttu-id="1589e-109">Реализация [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) является необязательной, за исключением объектов транзакций, которые всегда должны реализовывать [**канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) для отслеживания состояния ресурсов, которые они хранят.</span><span class="sxs-lookup"><span data-stu-id="1589e-109">Implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) is optional, except for transactional objects, which should always implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) to monitor the state of the resources they hold.</span></span> <span data-ttu-id="1589e-110">Однако рекомендуется реализовать **IObjectControl** в большинстве случаев, поскольку он обеспечивает эффективный способ управления поведением объекта в составе пула, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="1589e-110">However, it is advisable to implement **IObjectControl** in most cases because it provides an efficient way to manage the behavior of a pooled object, as described below.</span></span>

## <a name="performing-context-specific-initialization"></a><span data-ttu-id="1589e-111">Выполнение инициализации Context-Specific</span><span class="sxs-lookup"><span data-stu-id="1589e-111">Performing Context-Specific Initialization</span></span>

<span data-ttu-id="1589e-112">С помощью функции [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)можно инициализировать объект в контексте, в котором он активирован для данного клиента.</span><span class="sxs-lookup"><span data-stu-id="1589e-112">Using [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), you can initialize the object in the context in which it is activated for a given client.</span></span> <span data-ttu-id="1589e-113">Например, чтобы определить, имеет ли объект сходство транзакций (его ресурсы могут быть уже прикреплены), вы можете получить идентификатор транзакции, связанный с контекстом.</span><span class="sxs-lookup"><span data-stu-id="1589e-113">For example, to determine whether the object has transaction affinity (its resources may already be enlisted), you might get the transaction ID associated with the context.</span></span>

<span data-ttu-id="1589e-114">Обычно для выполнения инициализации, которая согласована в любых методах, предоставляемых объектом, как правило, используется команда [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), которая рассматривается как часть конструктора объекта, относящаяся к контексту.</span><span class="sxs-lookup"><span data-stu-id="1589e-114">Typically you would use [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)to perform initialization that is consistent across any methods exposed by the object, treating it as the context-specific portion of the object's constructor.</span></span>

## <a name="cleaning-up-any-client-state"></a><span data-ttu-id="1589e-115">Очистка любого состояния клиента</span><span class="sxs-lookup"><span data-stu-id="1589e-115">Cleaning Up Any Client State</span></span>

<span data-ttu-id="1589e-116">С помощью функции [**деактивации**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)можно избавиться от любого клиентского состояния, которое может существовать, чтобы объект возвращался в пул в полностью общем состоянии и затем использоваться любым клиентом без ущерба для безопасности или изоляции.</span><span class="sxs-lookup"><span data-stu-id="1589e-116">Using [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), you can get rid of any client-specific state that might exist so that your object returns to the pool in a completely generic state and can then be used by any client without compromising security or isolation.</span></span>

## <a name="controlling-reuse-of-the-object"></a><span data-ttu-id="1589e-117">Управление повторной использованием объекта</span><span class="sxs-lookup"><span data-stu-id="1589e-117">Controlling Reuse of the Object</span></span>

<span data-ttu-id="1589e-118">С помощью [**канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)можно отслеживать внутреннее состояние объекта и сообщать о его порасположении для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="1589e-118">Using [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), you can monitor the internal state of your object and report on whether it is fit for its reuse.</span></span> <span data-ttu-id="1589e-119">Если **канбепулед** возвращает значение true, а максимальное значение пула не достигнуто, объект помещается обратно в общий пул.</span><span class="sxs-lookup"><span data-stu-id="1589e-119">If **CanBePooled** returns True and the pool maximum has not been reached, the object is placed back in the general pool.</span></span> <span data-ttu-id="1589e-120">Если **канбепулед** возвращает значение false, объект отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="1589e-120">If **CanBePooled** returns False, the object is discarded.</span></span> <span data-ttu-id="1589e-121">В случае с транзакционными компонентами возврат значения false приведет к повреждение текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="1589e-121">In the case of transactional components, returning False will doom the current transaction.</span></span>

<span data-ttu-id="1589e-122">Как правило, вы сохраняете некоторые глобальные элементы данных для объекта, и если вы обнаружите, что подключение является недопустимым или ресурс какого-то типа находится в неисправном состоянии, установите его в соответствии с текущей ситуацией и верните его с помощью [**канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="1589e-122">Typically, you would keep some global data member for the object, and if you detect a connection to be bad or a resource of some kind to be in a bad state, set this to reflect the current situation and return it through [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="1589e-123">Если объект не реализует [**канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), экземпляры будут по-прежнему использоваться повторно, пока не будет достигнут максимальный уровень пула.</span><span class="sxs-lookup"><span data-stu-id="1589e-123">If an object does not implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), instances will continue to be reused until the pool maximum level is reached.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1589e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="1589e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1589e-125">Строки конструктора объектов COM+</span><span class="sxs-lookup"><span data-stu-id="1589e-125">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="1589e-126">Как работает пул объектов</span><span class="sxs-lookup"><span data-stu-id="1589e-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="1589e-127">Повышение производительности с помощью пула объектов</span><span class="sxs-lookup"><span data-stu-id="1589e-127">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="1589e-128">Группирование транзакционных объектов в пул</span><span class="sxs-lookup"><span data-stu-id="1589e-128">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="1589e-129">Требования к объектам в пуле</span><span class="sxs-lookup"><span data-stu-id="1589e-129">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



