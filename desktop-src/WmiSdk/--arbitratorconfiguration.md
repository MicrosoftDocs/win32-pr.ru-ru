---
description: Ограничивает внутренние ресурсы, используемые операциями, инициированными клиентами WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: Класс __ArbitratorConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 906164d6d715ed70bccecf61fba767ada622c74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265187"
---
# <a name="__arbitratorconfiguration-class"></a><span data-ttu-id="231e7-103">\_\_Класс Арбитраторконфигуратион</span><span class="sxs-lookup"><span data-stu-id="231e7-103">\_\_ArbitratorConfiguration class</span></span>

<span data-ttu-id="231e7-104">Класс **\_ \_ арбитраторконфигуратион** — это класс конфигурации, который ограничивает внутренние ресурсы, используемые операциями, инициированными клиентами WMI.</span><span class="sxs-lookup"><span data-stu-id="231e7-104">The **\_\_ArbitratorConfiguration** class is a configuration class that limits the internal resources that are used by operations initiated by WMI clients.</span></span> <span data-ttu-id="231e7-105">Это одноэлементный класс, находящийся в \\ корневом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="231e7-105">This is a singleton class that resides in the \\root namespace.</span></span> <span data-ttu-id="231e7-106">Класс создается внутренним образом, поэтому для него не существует MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="231e7-106">The class is internally generated so there is no MOF file for it.</span></span>

<span data-ttu-id="231e7-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="231e7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="231e7-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="231e7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="231e7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="231e7-109">Syntax</span></span>

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a><span data-ttu-id="231e7-110">Члены</span><span class="sxs-lookup"><span data-stu-id="231e7-110">Members</span></span>

<span data-ttu-id="231e7-111">Класс **\_ \_ арбитраторконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="231e7-111">The **\_\_ArbitratorConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="231e7-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="231e7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="231e7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="231e7-113">Properties</span></span>

<span data-ttu-id="231e7-114">Класс **\_ \_ арбитраторконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="231e7-114">The **\_\_ArbitratorConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="231e7-115">**аутстандингтасксперусер**</span><span class="sxs-lookup"><span data-stu-id="231e7-115">**OutstandingTasksPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-116">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-118">Unused.</span></span> <span data-ttu-id="231e7-119">Число невыполненных задач, инициированных пользователем, в любое время.</span><span class="sxs-lookup"><span data-stu-id="231e7-119">Number of outstanding user initiated tasks at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-120">**аутстандингтаскстотал**</span><span class="sxs-lookup"><span data-stu-id="231e7-120">**OutstandingTasksTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-121">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-123">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-123">Unused.</span></span> <span data-ttu-id="231e7-124">Общее число невыполненных задач в любое время.</span><span class="sxs-lookup"><span data-stu-id="231e7-124">Total number of outstanding tasks at any time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-125">**перманентсубскриптионсперусер**</span><span class="sxs-lookup"><span data-stu-id="231e7-125">**PermanentSubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-128">Количество постоянных подписок, разрешенных для конкретного пользователя в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="231e7-128">Number of permanent subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-129">**перманентсубскриптионстотал**</span><span class="sxs-lookup"><span data-stu-id="231e7-129">**PermanentSubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-132">Общее число постоянных подписок, разрешенных для всех пользователей за один раз.</span><span class="sxs-lookup"><span data-stu-id="231e7-132">Total number of permanent subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-133">**поллингинструктионсперусер**</span><span class="sxs-lookup"><span data-stu-id="231e7-133">**PollingInstructionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-136">Количество запросов событий опроса, разрешенных для конкретного пользователя в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="231e7-136">Number of polling event queries allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-137">**поллингинструктионстотал**</span><span class="sxs-lookup"><span data-stu-id="231e7-137">**PollingInstructionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-140">Общее количество инструкций опроса, разрешенных для всех пользователей за один раз.</span><span class="sxs-lookup"><span data-stu-id="231e7-140">Total number of polling instructions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-141">**поллингмемориперусер**</span><span class="sxs-lookup"><span data-stu-id="231e7-141">**PollingMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-144">Количество запросов событий опроса памяти, выданных определенным пользователем, может использоваться в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="231e7-144">Amount of memory polling event queries, issued by a particular user, can consume at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-145">**поллингмеморитотал**</span><span class="sxs-lookup"><span data-stu-id="231e7-145">**PollingMemoryTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-148">Общий объем памяти, который опрашивает запросы событий для всех пользователей, может быть потребителем в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="231e7-148">Total amount of memory that polling event queries, for all users combined, can consumer at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-149">**куотаретрикаунт**</span><span class="sxs-lookup"><span data-stu-id="231e7-149">**QuotaRetryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-152">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-152">Unused.</span></span> <span data-ttu-id="231e7-153">Число нарушений квоты, разрешенных до отмены задачи.</span><span class="sxs-lookup"><span data-stu-id="231e7-153">Number of quota violations permitted before a task is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-154">**куотаретриваитинтервал**</span><span class="sxs-lookup"><span data-stu-id="231e7-154">**QuotaRetryWaitInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-155">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-157">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-157">Unused.</span></span> <span data-ttu-id="231e7-158">Задержка, появившаяся в выполнении задачи при каждом нарушении квоты.</span><span class="sxs-lookup"><span data-stu-id="231e7-158">Delay introduced into the task execution on each quota violation.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-159">**тасксреадсперусер**</span><span class="sxs-lookup"><span data-stu-id="231e7-159">**TaskThreadsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-162">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-162">Unused.</span></span> <span data-ttu-id="231e7-163">Максимальное число потоков задач, связанных с определенным пользователем в один раз.</span><span class="sxs-lookup"><span data-stu-id="231e7-163">Maximum number of task threads associated with a particular user t any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-164">**тасксреадстотал**</span><span class="sxs-lookup"><span data-stu-id="231e7-164">**TaskThreadsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-167">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-167">Unused.</span></span> <span data-ttu-id="231e7-168">Максимальное число потоков задач.</span><span class="sxs-lookup"><span data-stu-id="231e7-168">Maximum number of task threads.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-169">**темпорарисубскриптионсперусер**</span><span class="sxs-lookup"><span data-stu-id="231e7-169">**TemporarySubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-172">Количество временных подписок, разрешенных для конкретного пользователя в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="231e7-172">Number of temporary subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-173">**темпорарисубскриптионстотал**</span><span class="sxs-lookup"><span data-stu-id="231e7-173">**TemporarySubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-174">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-176">Общее количество временных подписок, разрешенных для всех пользователей за один раз.</span><span class="sxs-lookup"><span data-stu-id="231e7-176">Total number of temporary subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-177">**тоталкачедиск**</span><span class="sxs-lookup"><span data-stu-id="231e7-177">**TotalCacheDisk**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-178">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-180">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-180">Unused.</span></span> <span data-ttu-id="231e7-181">Общий кэш диска, связанный со всеми пользователями за один раз.</span><span class="sxs-lookup"><span data-stu-id="231e7-181">Total disk cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-182">**тоталкачедискпертаск**</span><span class="sxs-lookup"><span data-stu-id="231e7-182">**TotalCacheDiskPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-183">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-185">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-185">Unused.</span></span> <span data-ttu-id="231e7-186">Общий кэш диска, связанный с определенной задачей в любое время.</span><span class="sxs-lookup"><span data-stu-id="231e7-186">Total disk cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-187">**тоталкачедискперусер**</span><span class="sxs-lookup"><span data-stu-id="231e7-187">**TotalCacheDiskPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-188">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-190">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-190">Unused.</span></span> <span data-ttu-id="231e7-191">Общий кэш диска, связанный с определенным пользователем в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="231e7-191">Total disk cache associated with a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-192">**тоталкачемемори**</span><span class="sxs-lookup"><span data-stu-id="231e7-192">**TotalCacheMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-193">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-195">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-195">Unused.</span></span> <span data-ttu-id="231e7-196">Общий кэш памяти, связанный со всеми пользователями за один раз.</span><span class="sxs-lookup"><span data-stu-id="231e7-196">Total memory cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-197">**тоталкачемеморипертаск**</span><span class="sxs-lookup"><span data-stu-id="231e7-197">**TotalCacheMemoryPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-198">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-200">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-200">Unused.</span></span> <span data-ttu-id="231e7-201">Общий кэш памяти, связанный с определенной задачей в любое время.</span><span class="sxs-lookup"><span data-stu-id="231e7-201">Total memory cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-202">**тоталкачемемориперусер**</span><span class="sxs-lookup"><span data-stu-id="231e7-202">**TotalCacheMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-203">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-205">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-205">Unused.</span></span> <span data-ttu-id="231e7-206">Общий кэш памяти, связанный с определенным пользователем в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="231e7-206">Total memory cache associated with a particular user at anyone time.</span></span>

</dd> <dt>

<span data-ttu-id="231e7-207">**тоталусерс**</span><span class="sxs-lookup"><span data-stu-id="231e7-207">**TotalUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231e7-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231e7-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231e7-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231e7-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231e7-210">Не используется.</span><span class="sxs-lookup"><span data-stu-id="231e7-210">Unused.</span></span> <span data-ttu-id="231e7-211">Максимальное число подключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="231e7-211">Maximum number of connected users.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="231e7-212">Комментарии</span><span class="sxs-lookup"><span data-stu-id="231e7-212">Remarks</span></span>

<span data-ttu-id="231e7-213">**\_ \_ Арбитраторконфигуратион** наследуется от [**\_ \_ системкласс**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="231e7-213">**\_\_ArbitratorConfiguration** is inherited from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="231e7-214">Требования</span><span class="sxs-lookup"><span data-stu-id="231e7-214">Requirements</span></span>



| <span data-ttu-id="231e7-215">Требование</span><span class="sxs-lookup"><span data-stu-id="231e7-215">Requirement</span></span> | <span data-ttu-id="231e7-216">Значение</span><span class="sxs-lookup"><span data-stu-id="231e7-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="231e7-217">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="231e7-217">Minimum supported client</span></span><br/> | <span data-ttu-id="231e7-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="231e7-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="231e7-219">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="231e7-219">Minimum supported server</span></span><br/> | <span data-ttu-id="231e7-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="231e7-220">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="231e7-221">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="231e7-221">Namespace</span></span><br/>                | <span data-ttu-id="231e7-222">Root</span><span class="sxs-lookup"><span data-stu-id="231e7-222">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="231e7-223">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="231e7-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231e7-224">**\_\_системкласс**</span><span class="sxs-lookup"><span data-stu-id="231e7-224">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="231e7-225">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="231e7-225">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

