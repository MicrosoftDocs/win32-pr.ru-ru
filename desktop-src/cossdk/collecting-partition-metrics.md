---
description: Сбор метрик секции
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Сбор метрик секции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141227"
---
# <a name="collecting-partition-metrics"></a><span data-ttu-id="e8f48-103">Сбор метрик секции</span><span class="sxs-lookup"><span data-stu-id="e8f48-103">Collecting Partition Metrics</span></span>

<span data-ttu-id="e8f48-104">В некоторых случаях Организация может захотеть собираются сведения об использовании приложения COM+ в целях мониторинга, планирования загрузки и учета ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8f48-104">In some cases, an organization might want to collect information on COM+ application use for the purposes of monitoring, capacity planning, and resource accounting.</span></span>

<span data-ttu-id="e8f48-105">Например, поставщику службы приложений (ASP) может потребоваться начисление клиента на использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8f48-105">For example, an application service provider (ASP) might want to charge a customer for its resource usage.</span></span> <span data-ttu-id="e8f48-106">Для этого COM+ позволяет получать сведения о событиях и метриках на основе каждого раздела.</span><span class="sxs-lookup"><span data-stu-id="e8f48-106">To do this, COM+ allows you to collect event and metrics information on a per-partition basis.</span></span>

<span data-ttu-id="e8f48-107">Чтобы получить эти сведения для определенной секции, необходимо указать для каждого интерфейса инструментария COM+ элемент идентификатора секции в стандартной структуре событий.</span><span class="sxs-lookup"><span data-stu-id="e8f48-107">The way to collect this information for a specific partition is by specifying, for each COM+ instrumentation interface, the partition ID member within the standard event structure.</span></span> <span data-ttu-id="e8f48-108">Структура событий является первым значением интерфейса инструментария COM+.</span><span class="sxs-lookup"><span data-stu-id="e8f48-108">The event structure is the first value of a COM+ instrumentation interface.</span></span> <span data-ttu-id="e8f48-109">Дополнительные сведения см. в разделе [интерфейсы инструментария com+](com--instrumentation-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="e8f48-109">For more information, see [COM+ Instrumentation Interfaces](com--instrumentation-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8f48-110">См. также</span><span class="sxs-lookup"><span data-stu-id="e8f48-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8f48-111">Настройка кэша секций</span><span class="sxs-lookup"><span data-stu-id="e8f48-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="e8f48-112">Группирование приложений в секции</span><span class="sxs-lookup"><span data-stu-id="e8f48-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="e8f48-113">Управление локальными секциями</span><span class="sxs-lookup"><span data-stu-id="e8f48-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="e8f48-114">Управление секциями в Active Directory</span><span class="sxs-lookup"><span data-stu-id="e8f48-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="e8f48-115">Установка прав администратора для секции</span><span class="sxs-lookup"><span data-stu-id="e8f48-115">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



