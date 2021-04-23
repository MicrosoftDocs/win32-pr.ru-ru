---
description: Функция разделов COM+ включает кэш секций. В этом кэше хранятся сопоставления пользователей и секций, которые предназначены для предотвращения повторяющихся Active Directoryного доступа.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Настройка кэша секций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701283"
---
# <a name="configuring-the-partition-cache"></a><span data-ttu-id="56a96-104">Настройка кэша секций</span><span class="sxs-lookup"><span data-stu-id="56a96-104">Configuring the Partition Cache</span></span>

<span data-ttu-id="56a96-105">Функция разделов COM+ включает кэш секций.</span><span class="sxs-lookup"><span data-stu-id="56a96-105">The COM+ partitions feature includes a partition cache.</span></span> <span data-ttu-id="56a96-106">В этом кэше хранятся сопоставления пользователей и секций, которые предназначены для предотвращения повторяющихся Active Directoryного доступа.</span><span class="sxs-lookup"><span data-stu-id="56a96-106">This cache stores user-to-partition mappings and is designed to avoid repetitive Active Directory access.</span></span>

## <a name="changing-cache-size"></a><span data-ttu-id="56a96-107">Изменение размера кэша</span><span class="sxs-lookup"><span data-stu-id="56a96-107">Changing Cache Size</span></span>

<span data-ttu-id="56a96-108">Кэш секций состоит из трех таблиц, размер которых можно изменить для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="56a96-108">The partition cache consists of three tables, whose size can be modified to enhance performance.</span></span> <span data-ttu-id="56a96-109">Эти таблицы состоят из числа записей SID в кэше, количества записей подразделения в кэше и количества записей секций в кэше.</span><span class="sxs-lookup"><span data-stu-id="56a96-109">These tables consist of the number of SID entries in the cache, the number of OU entries in the cache, and the number of partition entries in the cache.</span></span>

<span data-ttu-id="56a96-110">Чтобы изменить размеры этих таблиц, администраторы могут изменить значения раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="56a96-110">To change these table sizes, administrators can modify the values of a registry key.</span></span> <span data-ttu-id="56a96-111">Ниже приведен раздел реестра и его значения.</span><span class="sxs-lookup"><span data-stu-id="56a96-111">The registry key and its values are as follows:</span></span>

<span data-ttu-id="56a96-112">**HKLM \\ Software \\ Microsoft \\ COM3 \\ партитионкаче**</span><span class="sxs-lookup"><span data-stu-id="56a96-112">**HKLM\\SOFTWARE\\Microsoft\\COM3\\PartitionCache**</span></span>



| <span data-ttu-id="56a96-113">Значения ключей</span><span class="sxs-lookup"><span data-stu-id="56a96-113">Key values</span></span>                         | <span data-ttu-id="56a96-114">Описание</span><span class="sxs-lookup"><span data-stu-id="56a96-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56a96-115">**нумсидентриес**</span><span class="sxs-lookup"><span data-stu-id="56a96-115">**NumSidEntries**</span></span><br/>       | <span data-ttu-id="56a96-116">Содержит значение REG \_ DWORD для числа записей SID в кэше (по умолчанию — 512).</span><span class="sxs-lookup"><span data-stu-id="56a96-116">Contains the REG\_DWORD value for the number of SID entries in the cache (default=512).</span></span> <span data-ttu-id="56a96-117">Это значение должно быть больше числа уникальных идентификаторов, которые будет обслуживать компьютер в окне "время недействительности кэша".</span><span class="sxs-lookup"><span data-stu-id="56a96-117">This value should be set to a value greater than the number of unique identities that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="56a96-118">**нумнаминтриес**</span><span class="sxs-lookup"><span data-stu-id="56a96-118">**NumNameEntries**</span></span><br/>      | <span data-ttu-id="56a96-119">Содержит значение REG \_ DWORD для числа записей имени подразделения в кэше (по умолчанию — 64).</span><span class="sxs-lookup"><span data-stu-id="56a96-119">Contains the REG\_DWORD value for the number of OU name entries in the cache (default=64).</span></span> <span data-ttu-id="56a96-120">Это значение должно быть больше числа уникальных имен подразделений, которые будет обслуживать компьютер в окне "время недействительности кэша".</span><span class="sxs-lookup"><span data-stu-id="56a96-120">This value should be set to a value greater than the number of unique OU names that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="56a96-121">**нумпартитионентриес**</span><span class="sxs-lookup"><span data-stu-id="56a96-121">**NumPartitionEntries**</span></span><br/> | <span data-ttu-id="56a96-122">Содержит значение REG \_ DWORD для количества записей раздела в кэше (по умолчанию — 1024).</span><span class="sxs-lookup"><span data-stu-id="56a96-122">Contains the REG\_DWORD value for the number of partition entries in the cache (default=1024).</span></span><br/> <span data-ttu-id="56a96-123">В окне время недействительности кэша значение DWORD должно быть больше числа уникальных секций, которые будет обслуживать компьютер.</span><span class="sxs-lookup"><span data-stu-id="56a96-123">In the cache invalidation time window, the DWORD value should be set to a number greater than the number of unique partitions that a machine will be servicing.</span></span> <span data-ttu-id="56a96-124">Это связано с тем, что контекст компонента может включать идентификатор секции для секции, которая не находится на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="56a96-124">This is because a component's context can include a partition ID for a partition that does not reside on that machine.</span></span> <br/> |
| <span data-ttu-id="56a96-125">**ентрекспиратион**</span><span class="sxs-lookup"><span data-stu-id="56a96-125">**EntryExpiration**</span></span><br/>     | <span data-ttu-id="56a96-126">Содержит значение REG \_ DWORD для счетчика тактов (каждый Квант = ~ 7 минут) до тех пор, пока запись в кэше не станет недопустимой (значение по умолчанию — 4 (~ 28 минут)).</span><span class="sxs-lookup"><span data-stu-id="56a96-126">Contains the REG\_DWORD value for the tick count (each tick = ~7 minutes) until a cache entry becomes invalid (default=4 (~28 minutes)).</span></span><br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a><span data-ttu-id="56a96-127">Очистка кэша</span><span class="sxs-lookup"><span data-stu-id="56a96-127">Flushing the Cache</span></span>

<span data-ttu-id="56a96-128">Так как COM+ кэширует секцию по умолчанию для пользователей, можно вызвать этот метод после изменения секции по умолчанию для пользователя в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="56a96-128">Because COM+ caches the default partition for users, you might want to call this method after changing the default partition for a user in the Active Directory.</span></span> <span data-ttu-id="56a96-129">Администраторы могут сделать это программно, вызвав метод [**флушпартитионкаче**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="56a96-129">Administrators can do this programmatically by calling the [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56a96-130">См. также</span><span class="sxs-lookup"><span data-stu-id="56a96-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56a96-131">Сбор метрик секции</span><span class="sxs-lookup"><span data-stu-id="56a96-131">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="56a96-132">Группирование приложений в секции</span><span class="sxs-lookup"><span data-stu-id="56a96-132">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="56a96-133">Управление локальными секциями</span><span class="sxs-lookup"><span data-stu-id="56a96-133">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="56a96-134">Управление секциями в Active Directory</span><span class="sxs-lookup"><span data-stu-id="56a96-134">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="56a96-135">Установка прав администратора для секции</span><span class="sxs-lookup"><span data-stu-id="56a96-135">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




