---
description: Состояния ресурсов в пуле, доступные для распределителя ресурсов COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Состояния ресурсов в пуле, доступные для распределителя ресурсов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496326"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a><span data-ttu-id="de655-103">Состояния ресурсов в пуле, доступные для распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="de655-103">Pooled Resource States Available to COM+ Resource Dispenser</span></span>

<span data-ttu-id="de655-104">В любой момент времени ресурс либо используется, либо не используется, либо прикреплен к транзакции или не прикреплен к нему.</span><span class="sxs-lookup"><span data-stu-id="de655-104">At any one time, a resource is either in use or not in use and is either enlisted or not enlisted in a transaction.</span></span> <span data-ttu-id="de655-105">При этом выдаются четыре возможных состояния ресурсов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="de655-105">This yields four possible resource states, as follows:</span></span>

-   <span data-ttu-id="de655-106">**Ресурсы в неприкрепленной инвентаризации.**</span><span class="sxs-lookup"><span data-stu-id="de655-106">**Resources in unenlisted inventory.**</span></span> <span data-ttu-id="de655-107">Ресурс, который не используется объектом и не закрепляется в транзакции, находится в неприкрепленной инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="de655-107">A resource that is not in use by an object and not enlisted in a transaction is in unenlisted inventory.</span></span> <span data-ttu-id="de655-108">Ресурс в общем учете доступен для назначения.</span><span class="sxs-lookup"><span data-stu-id="de655-108">A resource in general inventory is available for assignment.</span></span>

-   <span data-ttu-id="de655-109">**Ресурсы в прикрепленных запасах.**</span><span class="sxs-lookup"><span data-stu-id="de655-109">**Resources in enlisted inventory.**</span></span> <span data-ttu-id="de655-110">Ресурс, который не используется объектом, но прикрепленный к транзакции, находится в прикрепленных запасах.</span><span class="sxs-lookup"><span data-stu-id="de655-110">A resource that is not in use by an object but is enlisted in a transaction is in enlisted inventory.</span></span> <span data-ttu-id="de655-111">Такой ресурс доступен для назначения только тем объектам, которые выполняются в той же транзакции.</span><span class="sxs-lookup"><span data-stu-id="de655-111">Such a resource is available for assignment only to objects running in the same transaction.</span></span> <span data-ttu-id="de655-112">Ресурс перемещается из прикрепленной инвентаризации в неприкрепленную инвентаризацию, когда COM+ Уведомляет диспетчер распределителя о завершении транзакции.</span><span class="sxs-lookup"><span data-stu-id="de655-112">A resource moves from enlisted inventory to unenlisted inventory when COM+ notifies the dispenser manager that the transaction is complete.</span></span>

-   <span data-ttu-id="de655-113">**Ресурсы в неприкрепленном использовании.**</span><span class="sxs-lookup"><span data-stu-id="de655-113">**Resources in unenlisted use.**</span></span> <span data-ttu-id="de655-114">Если ресурс назначен объекту, а экземпляр не выполняется в транзакции, или распределитель ресурсов определил ресурс как нетранзакционный, этот ресурс будет использоваться в качестве неприкрепленного.</span><span class="sxs-lookup"><span data-stu-id="de655-114">If a resource is assigned to an object and the instance is not running in a transaction or the resource dispenser has identified the resource as non-transactional, this resource is in unenlisted use.</span></span>

-   <span data-ttu-id="de655-115">**Ресурсы в прикрепленном использовании.**</span><span class="sxs-lookup"><span data-stu-id="de655-115">**Resources in enlisted use.**</span></span> <span data-ttu-id="de655-116">Если ресурс назначен объекту, экземпляр выполняется в транзакции, а распределитель ресурсов успешно прикрепляет ресурс в транзакции, этот ресурс находится в прикрепленном использовании.</span><span class="sxs-lookup"><span data-stu-id="de655-116">If a resource is assigned to an object, the instance is running in a transaction, and the resource dispenser has successfully enlisted the resource in the transaction, this resource is in enlisted use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de655-117">См. также</span><span class="sxs-lookup"><span data-stu-id="de655-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de655-118">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="de655-118">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="de655-119">Прикрепление ресурса в транзакции</span><span class="sxs-lookup"><span data-stu-id="de655-119">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



