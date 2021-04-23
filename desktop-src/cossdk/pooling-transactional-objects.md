---
description: Для транзакционных компонентов, которые должны быть помещены в пул, предъявляются особые требования.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Группирование транзакционных объектов в пул
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701230"
---
# <a name="pooling-transactional-objects"></a><span data-ttu-id="af96c-103">Группирование транзакционных объектов в пул</span><span class="sxs-lookup"><span data-stu-id="af96c-103">Pooling Transactional Objects</span></span>

<span data-ttu-id="af96c-104">Для транзакционных компонентов, которые должны быть помещены в пул, предъявляются особые требования.</span><span class="sxs-lookup"><span data-stu-id="af96c-104">Transactional components that are to be pooled have special requirements.</span></span>

## <a name="manually-enlisting-resources"></a><span data-ttu-id="af96c-105">Прикрепление ресурсов вручную</span><span class="sxs-lookup"><span data-stu-id="af96c-105">Manually Enlisting Resources</span></span>

<span data-ttu-id="af96c-106">Объекты в пуле, участвующие в транзакциях, должны прикреплять управляемые ресурсы вручную.</span><span class="sxs-lookup"><span data-stu-id="af96c-106">Poolable objects that participate in transactions must manually enlist managed resources.</span></span> <span data-ttu-id="af96c-107">Если объект хранит управляемые ресурсы между клиентами, диспетчер ресурсов не будет автоматически прикрепляться к транзакции при активации объекта в заданном контексте.</span><span class="sxs-lookup"><span data-stu-id="af96c-107">If an object holds managed resources between clients, there will be no way for the resource manager to automatically enlist in a transaction when the object is activated in a given context.</span></span>

<span data-ttu-id="af96c-108">Сам объект должен выполнить логику обнаружения транзакции, отключить автоматическое прикрепление диспетчера ресурсов и вручную прикрепить все ресурсы, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="af96c-108">The object itself must handle the logic of detecting the transaction, turning off the resource manager's auto-enlistment, and manually enlisting any resources that it holds.</span></span> <span data-ttu-id="af96c-109">Эти действия относятся к используемому диспетчеру ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af96c-109">The steps for doing this are specific to the resource manager that you are using.</span></span> <span data-ttu-id="af96c-110">Если вам нужно прикрепить вручную, обратитесь к документации по диспетчеру ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af96c-110">If you need to do manual enlistment, consult the documentation for your resource manager.</span></span>

<span data-ttu-id="af96c-111">Как описано ниже, объекты могут быть объединены в пул с сопоставлением транзакций, пока транзакция активна и может быть активирована с помощью сходства транзакций, если вызывается клиентом, связанным с этой транзакцией.</span><span class="sxs-lookup"><span data-stu-id="af96c-111">As described below, objects can be pooled with transaction affinity while a transaction is active and can be activated with transaction affinity if called by a client associated with that transaction.</span></span> <span data-ttu-id="af96c-112">Перед прикреплением ресурсов необходимо сначала проверить соответствие транзакций.</span><span class="sxs-lookup"><span data-stu-id="af96c-112">Before enlisting resources, you should first check for transaction affinity.</span></span> <span data-ttu-id="af96c-113">Если объект взят из пула, относящегося к этой транзакции, он уже выполнил работу в этой транзакции и закрепляет ее ресурсы.</span><span class="sxs-lookup"><span data-stu-id="af96c-113">If the object has been taken from the pool specific to that transaction, it has already done work in that transaction and enlisted its resources.</span></span>

## <a name="turning-off-automatic-enlistment"></a><span data-ttu-id="af96c-114">Отключение автоматического прикрепления</span><span class="sxs-lookup"><span data-stu-id="af96c-114">Turning Off Automatic Enlistment</span></span>

<span data-ttu-id="af96c-115">Автоматическое прикрепление должно быть отключено после получения ресурса, обычно в конструкторе объекта.</span><span class="sxs-lookup"><span data-stu-id="af96c-115">Automatic enlistment should be turned off after the resource is acquired, usually in the object's constructor.</span></span> <span data-ttu-id="af96c-116">То есть вы отключаете автоматическое прикрепление, а затем подключаетесь.</span><span class="sxs-lookup"><span data-stu-id="af96c-116">That is, you disable automatic enlistment and then connect.</span></span>

<span data-ttu-id="af96c-117">Отключение автоматического прикрепления иногда может быть незаметной процедурой, особенно в случае многоуровневых поставщиков доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="af96c-117">Disabling auto-enlistment can sometimes be a subtle procedure, particularly in the case of layered data access providers.</span></span> <span data-ttu-id="af96c-118">Автоматическое прикрепление иногда связывается с пулом соединений, как и с ODBC, и иногда не так, как с OLE DB.</span><span class="sxs-lookup"><span data-stu-id="af96c-118">Auto-enlistment is sometimes coupled with connection pooling, as with ODBC, and sometimes not, as with OLE DB.</span></span> <span data-ttu-id="af96c-119">Может потребоваться обеспечить отключение автоматического прикрепления на нескольких уровнях поставщиков.</span><span class="sxs-lookup"><span data-stu-id="af96c-119">You might need to ensure that auto-enlistment is off at several levels of providers.</span></span>

## <a name="implementing-iobjectcontrol"></a><span data-ttu-id="af96c-120">Реализация IObjectControl</span><span class="sxs-lookup"><span data-stu-id="af96c-120">Implementing IObjectControl</span></span>

<span data-ttu-id="af96c-121">Объекты в пуле, участвующие в транзакциях, должны отслеживать текущее состояние ресурсов, которые они хранятся.</span><span class="sxs-lookup"><span data-stu-id="af96c-121">Poolable objects that participate in transactions must monitor the current state of resources they are holding.</span></span> <span data-ttu-id="af96c-122">Если объект обнаруживает, что он находится в непригодном для использования состоянии, например, если соединение является недопустимым, оно должно возвращать значение false для [**IObjectControl:: канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="af96c-122">If the object detects that it is in a non-reusable state—for example, if a connection is bad—it should return False for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span> <span data-ttu-id="af96c-123">Это приведет к удалению экземпляра объекта и неудачу текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="af96c-123">This will have the effect of both discarding the object instance and dooming the current transaction.</span></span>

## <a name="transaction-specific-pools"></a><span data-ttu-id="af96c-124">Пулы Transaction-Specific</span><span class="sxs-lookup"><span data-stu-id="af96c-124">Transaction-Specific Pools</span></span>

<span data-ttu-id="af96c-125">Пул объектов обычно является однородным, а любой объект в пуле, который в настоящее время не используется, имеет хорошее значение для возврата к любому клиенту.</span><span class="sxs-lookup"><span data-stu-id="af96c-125">A pool of objects is generally homogenous, and any pooled object not currently in use is good to return to any client.</span></span> <span data-ttu-id="af96c-126">Единственное исключение из этого правила — в случае с объектами транзакций, для которых оптимизирована Группировка объектов.</span><span class="sxs-lookup"><span data-stu-id="af96c-126">The only exception to this rule is in the case of transactional objects, for which object pooling is optimized.</span></span> <span data-ttu-id="af96c-127">Когда клиент, запрашивающий объект, имеет связанную транзакцию, COM+ проверит пул на наличие доступного объекта, уже связанного с этой транзакцией.</span><span class="sxs-lookup"><span data-stu-id="af96c-127">When the client requesting an object has an associated transaction, COM+ will scan the pool for an available object that is already associated with that transaction.</span></span> <span data-ttu-id="af96c-128">Если найден объект с сходством транзакций, он возвращается клиенту. в противном случае возвращается объект из общего пула.</span><span class="sxs-lookup"><span data-stu-id="af96c-128">If an object with transaction affinity is found, it is returned to the client; otherwise, an object from the general pool is returned.</span></span>

<span data-ttu-id="af96c-129">Таким образом, будут поддерживаться специальные подгруппы, содержащие объекты с сходством для конкретной транзакции.</span><span class="sxs-lookup"><span data-stu-id="af96c-129">In this manner, special subpools are maintained containing objects with affinity for a particular transaction.</span></span> <span data-ttu-id="af96c-130">Когда транзакция фиксируется или прерывается, эти объекты возвращаются в общий пул без сходства транзакций, готового к использованию любым клиентом.</span><span class="sxs-lookup"><span data-stu-id="af96c-130">When the transaction commits or aborts, these objects are returned to the general pool with no transaction affinity, ready to be used by any client.</span></span>

<span data-ttu-id="af96c-131">По этой причине, когда компонент вручную прикрепляет свои управляемые ресурсы в транзакции, он должен сначала проверить, не были ли они прикреплены.</span><span class="sxs-lookup"><span data-stu-id="af96c-131">For this reason, when your component manually enlists its managed resources in a transaction, it should first check to see whether they are already enlisted.</span></span> <span data-ttu-id="af96c-132">В этом случае нет необходимости прикрепляться к.</span><span class="sxs-lookup"><span data-stu-id="af96c-132">If so, there is no need to enlist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af96c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="af96c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af96c-134">Строки конструктора объектов COM+</span><span class="sxs-lookup"><span data-stu-id="af96c-134">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="af96c-135">Управление временем существования и состоянием объекта</span><span class="sxs-lookup"><span data-stu-id="af96c-135">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="af96c-136">Как работает пул объектов</span><span class="sxs-lookup"><span data-stu-id="af96c-136">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="af96c-137">Повышение производительности с помощью пула объектов</span><span class="sxs-lookup"><span data-stu-id="af96c-137">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="af96c-138">Требования к объектам в пуле</span><span class="sxs-lookup"><span data-stu-id="af96c-138">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



