---
description: Группирование приложений в секции
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Группирование приложений в секции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673149"
---
# <a name="grouping-applications-into-partitions"></a><span data-ttu-id="343f6-103">Группирование приложений в секции</span><span class="sxs-lookup"><span data-stu-id="343f6-103">Grouping Applications into Partitions</span></span>

<span data-ttu-id="343f6-104">При принятии решения о группировании приложений на разделы администраторам необходимо учитывать определенные правила и ограничения, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="343f6-104">When deciding how to group applications into partitions, administrators need to be aware of certain rules and restrictions, including the following:</span></span>

-   <span data-ttu-id="343f6-105">Приложение можно установить в одну или несколько секций.</span><span class="sxs-lookup"><span data-stu-id="343f6-105">An application can be installed into one or more partitions.</span></span>
-   <span data-ttu-id="343f6-106">В приложении может существовать только один экземпляр данного компонента.</span><span class="sxs-lookup"><span data-stu-id="343f6-106">Only one instance of a given component can exist in an application.</span></span>

## <a name="public-and-private-components"></a><span data-ttu-id="343f6-107">Общедоступные и частные компоненты</span><span class="sxs-lookup"><span data-stu-id="343f6-107">Public and Private Components</span></span>

<span data-ttu-id="343f6-108">При принятии решения о группировании приложений COM+ существуют другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="343f6-108">Other restrictions exist when deciding how to group COM+ applications.</span></span> <span data-ttu-id="343f6-109">Эти ограничения относятся к общедоступным и частным компонентам в приложении.</span><span class="sxs-lookup"><span data-stu-id="343f6-109">These restrictions pertain to public versus private components within an application.</span></span> <span data-ttu-id="343f6-110">Как правило, компоненты приложения могут быть общедоступными или частными.</span><span class="sxs-lookup"><span data-stu-id="343f6-110">Application components can generally be either public or private.</span></span> <span data-ttu-id="343f6-111">Однако при группировании приложений на разделы администраторам следует помнить о некоторых ограничениях, связанных с общими и частными компонентами.</span><span class="sxs-lookup"><span data-stu-id="343f6-111">However, when grouping applications into partitions, administrators should be aware of some restrictions around public and private components.</span></span> <span data-ttu-id="343f6-112">Эти ограничения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="343f6-112">The following table lists these restrictions.</span></span>



| <span data-ttu-id="343f6-113">Если приложение:</span><span class="sxs-lookup"><span data-stu-id="343f6-113">If an application is:</span></span>              | <span data-ttu-id="343f6-114">Затем компоненты в разделе могут быть:</span><span class="sxs-lookup"><span data-stu-id="343f6-114">Then components in a partition can be:</span></span>                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="343f6-115">Серверное приложение</span><span class="sxs-lookup"><span data-stu-id="343f6-115">A server application</span></span><br/>    | <span data-ttu-id="343f6-116">Общедоступные и частные.</span><span class="sxs-lookup"><span data-stu-id="343f6-116">Public and private.</span></span><br/>                                                                                           |
| <span data-ttu-id="343f6-117">Приложение библиотеки</span><span class="sxs-lookup"><span data-stu-id="343f6-117">A library application</span></span><br/>   | <span data-ttu-id="343f6-118">Только общедоступные.</span><span class="sxs-lookup"><span data-stu-id="343f6-118">Public only.</span></span> <span data-ttu-id="343f6-119">В противном случае приложение вызывающих объектов может иметь те же компоненты, что привело бы к неоднозначности.</span><span class="sxs-lookup"><span data-stu-id="343f6-119">Otherwise, the callers application could have the same components, which would create ambiguity.</span></span><br/> |
| <span data-ttu-id="343f6-120">В глобальном разделе</span><span class="sxs-lookup"><span data-stu-id="343f6-120">In the global partition</span></span><br/> | <span data-ttu-id="343f6-121">Только общедоступные.</span><span class="sxs-lookup"><span data-stu-id="343f6-121">Public only.</span></span> <span data-ttu-id="343f6-122">Это обеспечивает обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="343f6-122">This ensures backward compatibility.</span></span><br/>                                                             |



 

## <a name="application-ids"></a><span data-ttu-id="343f6-123">Идентификаторы приложений</span><span class="sxs-lookup"><span data-stu-id="343f6-123">Application IDs</span></span>

<span data-ttu-id="343f6-124">Каждое приложение COM+, установленное на компьютере, имеет уникальный идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="343f6-124">Every COM+ application installed on a computer has a unique application ID.</span></span> <span data-ttu-id="343f6-125">Однако имена приложений должны быть уникальными только в пределах одной секции, а не на всем компьютере.</span><span class="sxs-lookup"><span data-stu-id="343f6-125">However, application names need only be unique within a single partition and not on the entire computer.</span></span>

<span data-ttu-id="343f6-126">В следующей таблице показано, что происходит с ИДЕНТИФИКАТОРом приложения, когда приложение импортируется в секцию или экспортируется из секции.</span><span class="sxs-lookup"><span data-stu-id="343f6-126">The following table shows what happens to the application ID when an application is imported into a partition or exported from a partition.</span></span>



| <span data-ttu-id="343f6-127">Если приложение:</span><span class="sxs-lookup"><span data-stu-id="343f6-127">If an application is:</span></span>                                              | <span data-ttu-id="343f6-128">Идентификатор приложения:</span><span class="sxs-lookup"><span data-stu-id="343f6-128">Then the application ID:</span></span>                    |
|--------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="343f6-129">Импортировано в глобальный раздел</span><span class="sxs-lookup"><span data-stu-id="343f6-129">Imported to the global partition</span></span><br/>                        | <span data-ttu-id="343f6-130">Остается тем же</span><span class="sxs-lookup"><span data-stu-id="343f6-130">Remains the same</span></span><br/>                 |
| <span data-ttu-id="343f6-131">Импортировано в секцию, отличную от глобальной секции</span><span class="sxs-lookup"><span data-stu-id="343f6-131">Imported to a partition other than the global partition</span></span><br/> | <span data-ttu-id="343f6-132">Изменяется</span><span class="sxs-lookup"><span data-stu-id="343f6-132">Is changed</span></span><br/>                       |
| <span data-ttu-id="343f6-133">Экспортированный сертификат</span><span class="sxs-lookup"><span data-stu-id="343f6-133">Exported</span></span><br/>                                                | <span data-ttu-id="343f6-134">Входит в экспортируемый файл</span><span class="sxs-lookup"><span data-stu-id="343f6-134">Is included in the exported file</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="343f6-135">См. также</span><span class="sxs-lookup"><span data-stu-id="343f6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343f6-136">Сбор метрик секции</span><span class="sxs-lookup"><span data-stu-id="343f6-136">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="343f6-137">Настройка кэша секций</span><span class="sxs-lookup"><span data-stu-id="343f6-137">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="343f6-138">Управление локальными секциями</span><span class="sxs-lookup"><span data-stu-id="343f6-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="343f6-139">Управление секциями в Active Directory</span><span class="sxs-lookup"><span data-stu-id="343f6-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="343f6-140">Установка прав администратора для секции</span><span class="sxs-lookup"><span data-stu-id="343f6-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




