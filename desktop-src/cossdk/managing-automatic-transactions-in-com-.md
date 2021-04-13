---
description: В модели программирования COM+ можно разрабатывать компоненты так, чтобы сделать их лучше&\# 8212, включать бизнес-логику или устанавливать подключение к базе данных&\# 8212; и использовать платформу обработки транзакций Microsoft Windows для автоматизации транзакций.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Управление автоматическими транзакциями в COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539194"
---
# <a name="managing-automatic-transactions-in-com"></a><span data-ttu-id="34a94-103">Управление автоматическими транзакциями в COM+</span><span class="sxs-lookup"><span data-stu-id="34a94-103">Managing Automatic Transactions in COM+</span></span>

<span data-ttu-id="34a94-104">В модели программирования COM+ можно разрабатывать компоненты, чтобы сделать их лучше, обеспечивая бизнес-логику или установление подключения к базе данных, и использовать платформу обработки транзакций Microsoft Windows для автоматизации транзакций.</span><span class="sxs-lookup"><span data-stu-id="34a94-104">In the COM+ programming model, you can design your components to do what they do best—enabling business logic or establishing a database connection—and rely on the transaction processing framework of Microsoft Windows to automate transactions.</span></span>

## <a name="starting-a-transaction"></a><span data-ttu-id="34a94-105">Запуск транзакции</span><span class="sxs-lookup"><span data-stu-id="34a94-105">Starting a Transaction</span></span>

<span data-ttu-id="34a94-106">COM+ автоматически начинает транзакцию при возникновении одного из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="34a94-106">COM+ automatically begins a transaction when it encounters either of the following conditions:</span></span>

-   <span data-ttu-id="34a94-107">Когда нетранзакционный клиент вызывает компонент, для которого требуется транзакция или требуется новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="34a94-107">When a non-transactional client calls a component that requires a transaction or requires a new transaction.</span></span>
-   <span data-ttu-id="34a94-108">Когда клиент транзакций вызывает компонент, для которого требуется новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="34a94-108">When a transactional client calls a component that requires a new transaction.</span></span>

<span data-ttu-id="34a94-109">Если COM+ определяет, что объект должен иметь новую транзакцию, он сначала начинает транзакцию, а затем помещает в него объект.</span><span class="sxs-lookup"><span data-stu-id="34a94-109">If COM+ determines that an object should have a new transaction, it begins the transaction first and then places the object in it.</span></span> <span data-ttu-id="34a94-110">Этот процесс состоит из следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="34a94-110">The process includes the following steps:</span></span>

1.  <span data-ttu-id="34a94-111">COM+ создает объект контекста, устанавливает необходимые атрибуты [JIT-активации](com--just-in-time-activation.md) и [синхронизации](com--synchronization.md) и устанавливает для [флагов consistent и Done](consistent-and-done-flags.md) значение true и false соответственно.</span><span class="sxs-lookup"><span data-stu-id="34a94-111">COM+ creates a context object, sets both the [JIT activation](com--just-in-time-activation.md) and [Synchronization](com--synchronization.md) attributes to Required, and sets the [consistent and done flags](consistent-and-done-flags.md) to True and False, respectively.</span></span>
2.  <span data-ttu-id="34a94-112">COM+ взаимодействует с координатор распределенных транзакций (DTC) для начала транзакции.</span><span class="sxs-lookup"><span data-stu-id="34a94-112">COM+ communicates with the Distributed Transaction Coordinator (DTC) to begin a transaction.</span></span> <span data-ttu-id="34a94-113">DTC координирует физическую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="34a94-113">The DTC coordinates the physical transaction.</span></span>
3.  <span data-ttu-id="34a94-114">DTC создает идентификатор транзакции и передает его обратно в COM+.</span><span class="sxs-lookup"><span data-stu-id="34a94-114">The DTC generates a transaction identifier and passes it back to COM+.</span></span> <span data-ttu-id="34a94-115">Идентификатор транзакции устанавливает границу транзакции.</span><span class="sxs-lookup"><span data-stu-id="34a94-115">The transaction identifier establishes a transaction boundary.</span></span> <span data-ttu-id="34a94-116">Все объекты, участвующие в транзакции, имеют один и тот же идентификатор.</span><span class="sxs-lookup"><span data-stu-id="34a94-116">All objects participating in the transaction share the same identifier.</span></span>
4.  <span data-ttu-id="34a94-117">Когда клиент создает объект, COM+ активирует его в пределах границы транзакции.</span><span class="sxs-lookup"><span data-stu-id="34a94-117">When the client creates the object, COM+ activates it within the transaction boundary.</span></span>

## <a name="ending-a-transaction"></a><span data-ttu-id="34a94-118">Завершение транзакции</span><span class="sxs-lookup"><span data-stu-id="34a94-118">Ending a Transaction</span></span>

<span data-ttu-id="34a94-119">COM+ завершает автоматическую транзакцию путем ее фиксации или прерывания при выполнении одного из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="34a94-119">COM+ ends an automatic transaction by committing or aborting it when one of the following conditions occurs:</span></span>

-   <span data-ttu-id="34a94-120">Корневой объект транзакции завершает свою работу, и COM+ освобождает ее.</span><span class="sxs-lookup"><span data-stu-id="34a94-120">The root object of the transaction completes its work and COM+ releases it.</span></span> <span data-ttu-id="34a94-121">После деактивации корневого объекта транзакция пытается зафиксироваться.</span><span class="sxs-lookup"><span data-stu-id="34a94-121">After the root object deactivates, the transaction attempts to commit.</span></span>
-   <span data-ttu-id="34a94-122">Клиент освобождает корневой объект.</span><span class="sxs-lookup"><span data-stu-id="34a94-122">The client releases the root object.</span></span> <span data-ttu-id="34a94-123">Без ссылки корневой объект деактивируется, и транзакция пытается зафиксироваться.</span><span class="sxs-lookup"><span data-stu-id="34a94-123">Without a reference, the root object deactivates and the transaction attempts to commit.</span></span>
-   <span data-ttu-id="34a94-124">Транзакция превышает пороговое значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="34a94-124">The transaction exceeds its time-out threshold.</span></span> <span data-ttu-id="34a94-125">Транзакция автоматически прерывается, если не фиксируется в течение времени ожидания транзакции, деактивируются все объекты, связанные с транзакцией.</span><span class="sxs-lookup"><span data-stu-id="34a94-125">The transaction aborts automatically if not committed within the transaction time-out period, deactivating all objects associated with the transaction.</span></span> <span data-ttu-id="34a94-126">По умолчанию время ожидания транзакции составляет 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="34a94-126">The default transaction time-out period is 60 seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34a94-127">См. также</span><span class="sxs-lookup"><span data-stu-id="34a94-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34a94-128">Флаги consistent и Done</span><span class="sxs-lookup"><span data-stu-id="34a94-128">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="34a94-129">Ускорение транзакций путем уведомления корневого объекта</span><span class="sxs-lookup"><span data-stu-id="34a94-129">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[<span data-ttu-id="34a94-130">Завершение автоматической транзакции путем вызова Сеткомплете</span><span class="sxs-lookup"><span data-stu-id="34a94-130">Terminating an Automatic Transaction by Calling SetComplete</span></span>](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



