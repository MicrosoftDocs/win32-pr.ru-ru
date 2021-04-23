---
description: Прикрепление ресурса в транзакции
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Прикрепление ресурса в транзакции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423497"
---
# <a name="enlisting-a-resource-in-a-transaction"></a><span data-ttu-id="29f59-103">Прикрепление ресурса в транзакции</span><span class="sxs-lookup"><span data-stu-id="29f59-103">Enlisting a Resource in a Transaction</span></span>

<span data-ttu-id="29f59-104">После выделения ресурса, но непосредственно перед возвращением ресурса в распределитель ресурсов Диспетчер распределителя проверяет с помощью COM+, чтобы определить, выполняется ли вызывающий объект в транзакции.</span><span class="sxs-lookup"><span data-stu-id="29f59-104">After a resource is allocated, but just before returning the resource to the resource dispenser, the dispenser manager checks with COM+ to see whether the calling object is running within a transaction.</span></span> <span data-ttu-id="29f59-105">Если вызывающий объект выполняется в рамках транзакции, диспетчер распределителя обращается к распределителе ресурсов и запрашивает его прикрепление к ресурсу в транзакции.</span><span class="sxs-lookup"><span data-stu-id="29f59-105">If the calling object is running within a transaction, the dispenser manager calls back to the resource dispenser and asks it to enlist the resource in the transaction.</span></span> <span data-ttu-id="29f59-106">Затем ресурс возвращается в распределитель ресурсов, который затем возвращает его вызывающему экземпляру.</span><span class="sxs-lookup"><span data-stu-id="29f59-106">Then the resource is returned to the resource dispenser, which then returns it to the calling instance.</span></span>

<span data-ttu-id="29f59-107">Распределитель ресурсов должен иметь возможность прикрепления к транзакции OLE с координатор распределенных транзакций (DTC).</span><span class="sxs-lookup"><span data-stu-id="29f59-107">The resource dispenser must be able to enlist in an OLE transaction with the Distributed Transaction Coordinator (DTC).</span></span>

> [!Note]  
> <span data-ttu-id="29f59-108">Прикрепление транзакции является необязательным, когда распределитель ресурсов распределяет нетранзакционные ресурсы, такие как память или потоки.</span><span class="sxs-lookup"><span data-stu-id="29f59-108">Transaction enlistment is optional when a resource dispenser dispenses non-transactional resources, such as memory or threads.</span></span>

 

<span data-ttu-id="29f59-109">По завершении транзакции COM+ Уведомляет диспетчер распределителя о том, была ли она зафиксирована или прервана.</span><span class="sxs-lookup"><span data-stu-id="29f59-109">When a transaction is complete, COM+ notifies the dispenser manager about whether it committed or aborted.</span></span> <span data-ttu-id="29f59-110">Затем Диспетчер распределителя сообщает каждому контейнеру распределителя ресурсов, что все ресурсы, прикрепленные к этой транзакции, теперь можно переместить в общий учет.</span><span class="sxs-lookup"><span data-stu-id="29f59-110">Then the dispenser manager notifies each resource dispenser's holder that any resources enlisted in this transaction can now be moved to general inventory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29f59-111">См. также</span><span class="sxs-lookup"><span data-stu-id="29f59-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f59-112">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="29f59-112">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="29f59-113">Состояния ресурсов в пуле, доступные для распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="29f59-113">Pooled Resource States Available to COM+ Resource Dispenser</span></span>](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[<span data-ttu-id="29f59-114">Процесс выделения ресурсов распределителя ресурсов</span><span class="sxs-lookup"><span data-stu-id="29f59-114">Resource Dispenser Resource Allocation Process</span></span>](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



