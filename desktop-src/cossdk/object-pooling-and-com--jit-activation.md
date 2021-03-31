---
description: JIT-активация COM+, по сути, дает компромисс между жадными клиентами и жадными серверами для обеспечения оптимальной производительности. Клиенты получают ссылку на сохранение ссылок на объекты, а серверы могут более точно управлять использованием памяти.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Объединение объектов в пул и JIT-активация COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423490"
---
# <a name="object-pooling-and-com-jit-activation"></a><span data-ttu-id="87f4c-104">Объединение объектов в пул и JIT-активация COM+</span><span class="sxs-lookup"><span data-stu-id="87f4c-104">Object Pooling and COM+ JIT Activation</span></span>

<span data-ttu-id="87f4c-105">JIT-активация COM+, по сути, дает компромисс между жадными клиентами и жадными серверами для обеспечения оптимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="87f4c-105">COM+ JIT activation essentially strikes a compromise between greedy clients and greedy servers for the sake of getting optimal performance.</span></span> <span data-ttu-id="87f4c-106">Клиенты получают ссылку на сохранение ссылок на объекты, а серверы могут более точно управлять использованием памяти.</span><span class="sxs-lookup"><span data-stu-id="87f4c-106">Clients get to keep object references, while servers can more closely manage memory utilization.</span></span>

<span data-ttu-id="87f4c-107">Это можно уточнить, используя [пул объектов COM+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="87f4c-107">You can refine this further by using [COM+ Object Pooling](com--object-pooling.md).</span></span> <span data-ttu-id="87f4c-108">При помощи пулов объектов, активируемых JIT-активацией, можно выделить определенный объем памяти для хранения определенного числа объектов, активных в памяти, готовых к немедленному повторному использованию.</span><span class="sxs-lookup"><span data-stu-id="87f4c-108">By pooling objects that are JIT activated, you can dedicate a certain amount of memory to hold a certain number of objects active in memory, ready for immediate reuse.</span></span> <span data-ttu-id="87f4c-109">Это лучше всего подходит для создания объектов, как в случае, когда они хранят несколько ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87f4c-109">This makes the most sense when objects are expensive to create, as in the case where they hold multiple resources.</span></span>

<span data-ttu-id="87f4c-110">Таким образом, для создания пулов JIT-активируемых объектов можно получить следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="87f4c-110">Pooling JIT-activated objects in this manner, you can achieve the following benefits:</span></span>

-   <span data-ttu-id="87f4c-111">Значительно ускорить повторную активацию объектов.</span><span class="sxs-lookup"><span data-stu-id="87f4c-111">Greatly accelerated object reactivation times.</span></span>
-   <span data-ttu-id="87f4c-112">Повторное использование любых ресурсоемких ресурсов, хранящихся в объектах.</span><span class="sxs-lookup"><span data-stu-id="87f4c-112">Reuse of any expensive resources the objects are holding.</span></span>
-   <span data-ttu-id="87f4c-113">Более точное управление использованием памяти и ресурсов для объектов в составе пула.</span><span class="sxs-lookup"><span data-stu-id="87f4c-113">More precise governing of memory and resource use for the pooled objects.</span></span>
-   <span data-ttu-id="87f4c-114">Хранение административной гибкости, благодаря которой приложение может масштабироваться для использования доступных ресурсов и адаптироваться к изменяющимся требованиям к производительности.</span><span class="sxs-lookup"><span data-stu-id="87f4c-114">Retention of administrative flexibility so that your application can scale to use available resources and adapt to changing performance requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87f4c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="87f4c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87f4c-116">Основные понятия JIT-активации COM+</span><span class="sxs-lookup"><span data-stu-id="87f4c-116">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="87f4c-117">Группирование объектов COM+</span><span class="sxs-lookup"><span data-stu-id="87f4c-117">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="87f4c-118">Включение JIT-активации для компонента</span><span class="sxs-lookup"><span data-stu-id="87f4c-118">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="87f4c-119">Транзакции и JIT-активация COM+</span><span class="sxs-lookup"><span data-stu-id="87f4c-119">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



