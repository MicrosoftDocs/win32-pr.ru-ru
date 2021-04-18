---
description: Отслеживание нераспределенных ресурсов
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Отслеживание нераспределенных ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701263"
---
# <a name="tracking-non-allocated-resources"></a><span data-ttu-id="d7f55-103">Отслеживание нераспределенных ресурсов</span><span class="sxs-lookup"><span data-stu-id="d7f55-103">Tracking Non-Allocated Resources</span></span>

<span data-ttu-id="d7f55-104">Диспетчер распределителя может отслеживанию ресурса, который не поддается инвентаризации, на основе знаний о времени существования объекта.</span><span class="sxs-lookup"><span data-stu-id="d7f55-104">The dispenser manager can track a resource that is not inventoried, based on knowledge of the object's lifetime.</span></span> <span data-ttu-id="d7f55-105">При освобождении отслеживания невыделенный ресурс уничтожается и, следовательно, не возвращается в опись.</span><span class="sxs-lookup"><span data-stu-id="d7f55-105">When a tracked, non-allocated resource is freed, it is destroyed and therefore not returned to inventory.</span></span> <span data-ttu-id="d7f55-106">Этот режим только для наблюдения за ресурсами, которые недорого создавать и уничтожать, более удобен, чем хранение их в инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="d7f55-106">This track-only mode for resources that are inexpensive to create and destroy is more useful than storing them in inventory.</span></span> <span data-ttu-id="d7f55-107">Этот режим также полезен для управления распределителем памяти или для ресурса, который трудно выполнять инвентаризацию из-за слишком большого числа различных типов.</span><span class="sxs-lookup"><span data-stu-id="d7f55-107">This mode is also useful for managing a memory dispenser or for a resource that is difficult to inventory because there are too many different types.</span></span>

<span data-ttu-id="d7f55-108">В режиме "только трассировка" распределитель ресурсов непосредственно создает запрошенный ресурс, вместо того чтобы запрашивать от менеджера распределителя распределение одного из запасов.</span><span class="sxs-lookup"><span data-stu-id="d7f55-108">In track-only mode, a resource dispenser directly creates a requested resource instead of asking the dispenser manager to allocate one from inventory.</span></span> <span data-ttu-id="d7f55-109">Перед возвращением этого ресурса в компонент запрашивающего приложения распределитель ресурсов сообщает диспетчеру распределителя, что он отслеживает ресурс, что гарантирует, что даже если компонент не сможет освободить ресурс, диспетчер распределителя будет делать это, когда время существования компонента превышено.</span><span class="sxs-lookup"><span data-stu-id="d7f55-109">Before returning this resource to the requesting application component, the resource dispenser tells the dispenser manager to track the resource, which ensures that even if the component neglects to free the resource, the dispenser manager will do so when the component's lifetime is over.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7f55-110">См. также</span><span class="sxs-lookup"><span data-stu-id="d7f55-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7f55-111">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="d7f55-111">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



