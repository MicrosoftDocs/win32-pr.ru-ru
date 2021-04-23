---
title: Почему службы домен Active Directory используют эту модель репликации
description: В этом разделе объясняются причины для системы свободной формы, используемой службами домен Active Directory Services для модели репликации.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Active Directory модели репликации, преимущества
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887608"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a><span data-ttu-id="d5cd7-104">Почему службы домен Active Directory используют эту модель репликации</span><span class="sxs-lookup"><span data-stu-id="d5cd7-104">Why Active Directory Domain Services Uses This Replication Model</span></span>

<span data-ttu-id="d5cd7-105">В этом разделе объясняются причины для системы свободной формы, используемой службами домен Active Directory Services для модели репликации.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-105">This topic explains the reasons for the free-form system used by Active Directory Domain Services for a replication model.</span></span>

<span data-ttu-id="d5cd7-106">Домен Active Directory Services — это свободная система по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-106">Active Directory Domain Services are a free-form system for the following reasons:</span></span>

-   <span data-ttu-id="d5cd7-107">Клиентам требуется широко распределенное решение, в котором части каталога могут распределяться по сетям и администрировать их локально.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-107">Customers require a highly distributed solution in which parts of the directory can be spread across their networks and administered locally.</span></span>
-   <span data-ttu-id="d5cd7-108">Крупные клиенты часто растут до миллионов объектов, сотен или тысяч реплик или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-108">Large customers often grow to millions of objects, hundreds or thousands of replicas, or both.</span></span>
-   <span data-ttu-id="d5cd7-109">Многие клиентские сети предоставляют только периодическое подключение к некоторым расположениям. Например, удаленные платформы для перехода на топливо и поставляются в Sea, поэтому система должна быть устойчива к частично подключенным или отключенным операциям.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-109">Many customer networks provide only intermittent connectivity to some locations; for example, remote oil drilling platforms and ships at sea, so the system must be tolerant of partly connected or disconnected operations.</span></span>

<span data-ttu-id="d5cd7-110">Не существует способа гарантировать полноту осведомленности о текущем или будущем состоянии распределенной системы, поскольку знание изменений состояния должно быть распространено, а распространение требует времени, в течение которого могут возникать дополнительные изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-110">There is no way to guarantee complete awareness of the current or future state of a distributed system because knowledge of state changes must be propagated and propagation takes time, during which more state changes may occur.</span></span>

<span data-ttu-id="d5cd7-111">Тесно связанные системы обрабатывали неопределенность, пытаясь удалить его.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-111">Tightly coupled systems handle uncertainty by attempting to eliminate it.</span></span> <span data-ttu-id="d5cd7-112">Это достигается благодаря ограничениям на обновления, требующим, чтобы все узлы или большинство узлов были доступны перед выполнением обновлений, используя распределенные схемы блокировки или единое основное подключение для критически важных ресурсов, ограничивая все узлы как хорошо подключенные или сочетание этих методов.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-112">This is accomplished through constraints on updates, requiring all nodes or some majority of nodes to be available before updates can be performed, using distributed locking schemes or single-mastering for critical resources, constraining all nodes to be well-connected, or some combination of these techniques.</span></span> <span data-ttu-id="d5cd7-113">Чем более тесно связаны вычислительные узлы распределенной системы, тем меньше предельное значение масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-113">The more tightly coupled the computing nodes in a distributed system are, the lower the scaling limit.</span></span>

<span data-ttu-id="d5cd7-114">Системы произвольной формы обрабатывайте неопределенность, допуская его.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-114">Free-form systems handle uncertainty by tolerating it.</span></span> <span data-ttu-id="d5cd7-115">Система произвольной формы позволяет узлам иметь различные представления общего состояния системы и предоставляет алгоритмы для разрешения конфликтов.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-115">A free-form system enables the nodes to have differing views of the overall system state and provides algorithms for resolving conflicts.</span></span>

<span data-ttu-id="d5cd7-116">Тесно связанные решения были отклонены, как непригодные для домен Active Directory Services из-за требований к локальному администрированию, отключению работы и масштабируемости на очень большом количестве узлов.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-116">Tightly coupled solutions were rejected as unsuitable for Active Directory Domain Services because of the requirements for local administration, disconnected operation, and scalability to very large numbers of nodes.</span></span> <span data-ttu-id="d5cd7-117">Выбранная слабо связанная модель, нестрогая согласованность нескольких хозяев с конвергенцией, удовлетворяет всем требованиям.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-117">The loosely coupled model chosen, multi-master loose consistency with convergence, satisfies all requirements.</span></span>

 

 




