---
description: 'Дополнительные сведения: параметры резервного копирования и восстановления'
title: Параметры резервного копирования и восстановления
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546847"
---
# <a name="backup-and-restore-parameters"></a><span data-ttu-id="6a7ab-103">Параметры резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="6a7ab-103">Backup and Restore Parameters</span></span>


<span data-ttu-id="6a7ab-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6a7ab-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="backup-and-restore-parameters"></a><span data-ttu-id="6a7ab-105">Параметры резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="6a7ab-105">Backup and Restore Parameters</span></span>

<span data-ttu-id="6a7ab-106">Этот раздел содержит параметры, используемые для резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-106">This topic contains parameters that are used for backup and restore.</span></span>

<span data-ttu-id="6a7ab-107">*JET_paramAlternateDatabaseRecoveryPath*</span><span class="sxs-lookup"><span data-stu-id="6a7ab-107">*JET_paramAlternateDatabaseRecoveryPath*</span></span>  
<span data-ttu-id="6a7ab-108">113</span><span class="sxs-lookup"><span data-stu-id="6a7ab-108">113</span></span>  

<span data-ttu-id="6a7ab-109">Полный путь к каждой базе данных сохраняется в журналах транзакций во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-109">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="6a7ab-110">Обычно эти базы данных должны оставаться в исходном расположении для правильной работы воспроизведения транзакций.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-110">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="6a7ab-111">Этот параметр можно использовать для принудительного восстановления после сбоя или операции восстановления, чтобы найти базы данных, упоминаемые в журнале транзакций в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-111">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-112">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-112">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-114">Путь к папке (строка)</span><span class="sxs-lookup"><span data-stu-id="6a7ab-114">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-115">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-116">0 – 246 символов</span><span class="sxs-lookup"><span data-stu-id="6a7ab-116">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-117">Область.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-118">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="6a7ab-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-119">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-120">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-121">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-122">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-123">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-124">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-125">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-126">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-127">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-128">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-129">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-130">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-131">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="6a7ab-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-132">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="6a7ab-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a7ab-133">*JET_paramCleanupMismatchedLogFiles*</span><span class="sxs-lookup"><span data-stu-id="6a7ab-133">*JET_paramCleanupMismatchedLogFiles*</span></span>  
<span data-ttu-id="6a7ab-134">77</span><span class="sxs-lookup"><span data-stu-id="6a7ab-134">77</span></span>  

<span data-ttu-id="6a7ab-135">Этот параметр управляет результатом [жетинит](./jetinit-function.md) , когда ядро СУБД настроено для начала использования файлов журнала транзакций на диске, размер которых отличается от настроенного.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-135">This parameter controls the outcome of [JetInit](./jetinit-function.md) when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="6a7ab-136">Обычно [жетинит](./jetinit-function.md) успешно восстановит базы данных, но завершится сбоем с JET_errLogFileSizeMismatchDatabasesConsistent, чтобы указать, что размер файла журнала настроен неправильно.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-136">Normally, [JetInit](./jetinit-function.md) will successfully recover the databases but will fail with JET_errLogFileSizeMismatchDatabasesConsistent to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="6a7ab-137">Однако если этот параметр имеет значение true, то ядро СУБД автоматически удалит все старые файлы журналов, запустит новый набор файлов журнала транзакций, используя настроенный размер файла журнала, и возвратит JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-137">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size, and return JET_errSuccess.</span></span>

<span data-ttu-id="6a7ab-138">Этот параметр полезен, когда приложению требуется прозрачно изменить размер файла журнала транзакций, но все равно работать прозрачно в сценариях обновления и восстановления.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-138">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-139">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="6a7ab-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-141">Тип:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-142">Логическое</span><span class="sxs-lookup"><span data-stu-id="6a7ab-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-143">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-144">False, true</span><span class="sxs-lookup"><span data-stu-id="6a7ab-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-145">Область.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-146">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="6a7ab-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-147">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-148">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-149">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-150">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-151">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-152">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-153">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-154">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-155">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-156">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-157">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-158">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-159">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="6a7ab-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-160">Все</span><span class="sxs-lookup"><span data-stu-id="6a7ab-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a7ab-161">*JET_paramDeleteOutOfRangeLogs*</span><span class="sxs-lookup"><span data-stu-id="6a7ab-161">*JET_paramDeleteOutOfRangeLogs*</span></span>  
<span data-ttu-id="6a7ab-162">52</span><span class="sxs-lookup"><span data-stu-id="6a7ab-162">52</span></span>  

<span data-ttu-id="6a7ab-163">Если этот параметр имеет значение true, то все файлы журнала транзакций, находящиеся на диске, не являющиеся частью текущей последовательности файлов журнала, будут удалены с помощью [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="6a7ab-163">When this parameter is true, then any transaction log files found on disk that are not part of the current sequence of log files will be deleted by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="6a7ab-164">Это может использоваться для автоматической очистки лишних файлов журнала после операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-164">This may be used to automatically clean up extraneous log files after a restore operation.</span></span>

<span data-ttu-id="6a7ab-165">**Windows XP:**  Впервые появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-165">**Windows XP:**  Introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-166">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-166">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="6a7ab-167">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-168">Тип:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-168">Type:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-169">Логическое</span><span class="sxs-lookup"><span data-stu-id="6a7ab-169">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-170">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-170">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-171">False, true</span><span class="sxs-lookup"><span data-stu-id="6a7ab-171">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-172">Область.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-173">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="6a7ab-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-174">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-175">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-176">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-177">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-178">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-179">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-179">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-180">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-181">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-182">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-183">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-183">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-184">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-185">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-185">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-186">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="6a7ab-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-187">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="6a7ab-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a7ab-188">*JET_paramOSSnapshotTimeout*</span><span class="sxs-lookup"><span data-stu-id="6a7ab-188">*JET_paramOSSnapshotTimeout*</span></span>  
<span data-ttu-id="6a7ab-189">82</span><span class="sxs-lookup"><span data-stu-id="6a7ab-189">82</span></span>  

<span data-ttu-id="6a7ab-190">Этот параметр позволяет настроить период времени между вызовом [жетосснапшотфризе](./jetossnapshotfreeze-function.md) и [жетосснапшотсав](./jetossnapshotthaw-function.md) до наступления времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-190">This parameter configures the amount of time allowed between a call to [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) before a timeout occurs.</span></span> <span data-ttu-id="6a7ab-191">Дополнительные сведения см. в разделе [жетосснапшотфризе](./jetossnapshotfreeze-function.md) и [жетосснапшотсав](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6a7ab-191">Please see [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) for more information.</span></span> <span data-ttu-id="6a7ab-192">Время ожидания задается в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-192">The timeout is in milliseconds.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-193">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-193">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-194">20000 (Windows XP и Windows Server 2003);</span><span class="sxs-lookup"><span data-stu-id="6a7ab-194">20000 (Windows XP and Windows Server 2003);</span></span></p>
<p><span data-ttu-id="6a7ab-195">70000 (пакет обновления 1 (SP1) для Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="6a7ab-195">70000 (Windows Server 2003 SP1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-196">Тип:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-197">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="6a7ab-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-198">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-199">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="6a7ab-199">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-200">Область.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-200">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-201">Глобальный</span><span class="sxs-lookup"><span data-stu-id="6a7ab-201">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-202">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-202">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-203">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-204">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-204">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-205">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-206">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-206">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-207">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-207">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-208">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-208">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-209">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-209">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-210">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-210">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-211">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-212">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-212">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-213">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-213">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-214">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="6a7ab-214">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-215">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="6a7ab-215">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a7ab-216">*JET_paramZeroDatabaseDuringBackup*</span><span class="sxs-lookup"><span data-stu-id="6a7ab-216">*JET_paramZeroDatabaseDuringBackup*</span></span>  
<span data-ttu-id="6a7ab-217">71</span><span class="sxs-lookup"><span data-stu-id="6a7ab-217">71</span></span>  

<span data-ttu-id="6a7ab-218">Если этот параметр имеет значение true, то каждая страница в базе данных, для которой выполняется потоковая архивация, будет очищена от удаленных данных.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-218">When this parameter is true then every page in a database that is undergoing a streaming backup will be scrubbed of deleted data.</span></span> <span data-ttu-id="6a7ab-219">Важно отметить, что страницы базы данных, для которых выполняется очистка, находятся на диске.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-219">It is important to note that the database pages that are being scrubbed are on disk.</span></span> <span data-ttu-id="6a7ab-220">Перед процессом очистки создается резервная копия полного набора данных.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-220">The full data set is backed up prior to the scrub process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-221">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="6a7ab-222">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-223">Тип:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-224">Логическое</span><span class="sxs-lookup"><span data-stu-id="6a7ab-224">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-225">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-226">False, true</span><span class="sxs-lookup"><span data-stu-id="6a7ab-226">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-227">Область.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-228">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="6a7ab-228">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-229">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-230">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-230">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-231">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-232">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-233">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-234">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-235">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-236">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-237">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-238">Да</span><span class="sxs-lookup"><span data-stu-id="6a7ab-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-239">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-240">Нет</span><span class="sxs-lookup"><span data-stu-id="6a7ab-240">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-241">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="6a7ab-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6a7ab-242">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="6a7ab-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="6a7ab-243">Требования</span><span class="sxs-lookup"><span data-stu-id="6a7ab-243">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-244"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="6a7ab-244"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6a7ab-245">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-245">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a7ab-246"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6a7ab-246"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6a7ab-247">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-247">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a7ab-248"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6a7ab-248"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6a7ab-249">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6a7ab-249">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6a7ab-250">См. также:</span><span class="sxs-lookup"><span data-stu-id="6a7ab-250">See Also</span></span>

[<span data-ttu-id="6a7ab-251">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="6a7ab-251">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="6a7ab-252">жетинит</span><span class="sxs-lookup"><span data-stu-id="6a7ab-252">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="6a7ab-253">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="6a7ab-253">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="6a7ab-254">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="6a7ab-254">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
