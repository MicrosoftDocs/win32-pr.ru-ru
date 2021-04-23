---
description: 'Дополнительные сведения: параметры журнала транзакций'
title: Параметры журнала транзакций
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693344"
---
# <a name="transaction-log-parameters"></a><span data-ttu-id="faa5c-103">Параметры журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="faa5c-103">Transaction Log Parameters</span></span>


<span data-ttu-id="faa5c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="faa5c-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="faa5c-105">**В этой статье:**</span><span class="sxs-lookup"><span data-stu-id="faa5c-105">**In this article**</span></span>  
<span data-ttu-id="faa5c-106">Параметры журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="faa5c-106">Transaction Log Parameters</span></span>  
<span data-ttu-id="faa5c-107">Требования</span><span class="sxs-lookup"><span data-stu-id="faa5c-107">Requirements</span></span>  
<span data-ttu-id="faa5c-108">См. также:</span><span class="sxs-lookup"><span data-stu-id="faa5c-108">See Also</span></span>  

## <a name="transaction-log-parameters"></a><span data-ttu-id="faa5c-109">Параметры журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="faa5c-109">Transaction Log Parameters</span></span>

<span data-ttu-id="faa5c-110">Этот раздел содержит параметры, используемые для журналов транзакций.</span><span class="sxs-lookup"><span data-stu-id="faa5c-110">This topic contains parameters that are used for transaction logs.</span></span>

<span data-ttu-id="faa5c-111">*JET_paramBaseName*</span><span class="sxs-lookup"><span data-stu-id="faa5c-111">*JET_paramBaseName*</span></span>  
<span data-ttu-id="faa5c-112">3</span><span class="sxs-lookup"><span data-stu-id="faa5c-112">3</span></span>  

<span data-ttu-id="faa5c-113">Этот параметр задает три префикса буквы, используемые для многих файлов, используемых ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-113">This parameter sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="faa5c-114">Например, файл контрольных точек называется EDB. CHK по умолчанию, так как EDB является базовым именем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="faa5c-114">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span> <span data-ttu-id="faa5c-115">Базовое имя можно использовать для простого различения наборов файлов, принадлежащих разным экземплярам или различным приложениям.</span><span class="sxs-lookup"><span data-stu-id="faa5c-115">The base name can be used to easily distinguish between sets of files that belong to different instances or to different applications.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-116">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-116">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-117">&quot;EDB&quot;</span><span class="sxs-lookup"><span data-stu-id="faa5c-117">&quot;edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-118">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-118">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-119">Строка</span><span class="sxs-lookup"><span data-stu-id="faa5c-119">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-120">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-120">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-121">3 символа</span><span class="sxs-lookup"><span data-stu-id="faa5c-121">3 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-122">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-122">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-123">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-123">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-124">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-124">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-125">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-125">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-126">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-126">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-127">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-128">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-128">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-129">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-130">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-130">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-131">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-132">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-132">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-133">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-134">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-134">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-135">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-136">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-136">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-137">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-137">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-138">*JET_paramCircularLog*</span><span class="sxs-lookup"><span data-stu-id="faa5c-138">*JET_paramCircularLog*</span></span>  
<span data-ttu-id="faa5c-139">17</span><span class="sxs-lookup"><span data-stu-id="faa5c-139">17</span></span>  

<span data-ttu-id="faa5c-140">Этот параметр позволяет настроить управление файлами журнала транзакций ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-140">This parameter configures how transaction log files are managed by the database engine.</span></span>

<span data-ttu-id="faa5c-141">Если циклическое ведение журнала отключено, все созданные файлы журнала транзакций сохраняются на диске до тех пор, пока они больше не нужны, так как была выполнена полная резервная копия базы данных.</span><span class="sxs-lookup"><span data-stu-id="faa5c-141">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="faa5c-142">В этом режиме можно выполнить восстановление из более старой резервной копии и воспроизвести все хранящиеся файлы журнала транзакций таким образом, чтобы в результате аварии, которая была принудительно восстановлена, не были потеряны данные.</span><span class="sxs-lookup"><span data-stu-id="faa5c-142">In this mode, it is possible to restore from an older backup and play forward through all the retained transaction log files such that no data is lost as a result of the disaster that forced the restore.</span></span> <span data-ttu-id="faa5c-143">Для предотвращения переполнения диска файлами журнала транзакций необходимо регулярное полное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="faa5c-143">Regular full backups are required to prevent the disk from filling up with transaction log files.</span></span>

<span data-ttu-id="faa5c-144">Если циклическое ведение журнала включено, на диске сохраняются только файлы журнала транзакций, которые являются моложе текущей контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="faa5c-144">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="faa5c-145">Преимущество этого режима заключается в том, что для снятия старых файлов журнала транзакций резервные копии не требуются.</span><span class="sxs-lookup"><span data-stu-id="faa5c-145">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span> <span data-ttu-id="faa5c-146">Компромисс заключается в том, что восстановление без потери данных уже невозможно.</span><span class="sxs-lookup"><span data-stu-id="faa5c-146">The tradeoff is that a zero data loss restore is no longer possible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-147">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-147">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="faa5c-148">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-149">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-149">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-150">Логическое</span><span class="sxs-lookup"><span data-stu-id="faa5c-150">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-151">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-151">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-152">False, true</span><span class="sxs-lookup"><span data-stu-id="faa5c-152">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-153">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-153">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-154">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-154">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-155">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-155">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-156">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-156">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-157">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-157">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-158">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-159">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-160">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-160">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-161">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-162">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-163">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-164">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-165">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-166">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-167">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-168">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-168">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-169">*JET_paramCommitDefault*</span><span class="sxs-lookup"><span data-stu-id="faa5c-169">*JET_paramCommitDefault*</span></span>  
<span data-ttu-id="faa5c-170">16</span><span class="sxs-lookup"><span data-stu-id="faa5c-170">16</span></span>  

<span data-ttu-id="faa5c-171">Этот параметр управляет действием по умолчанию, выполняемым при фиксации самой внешней транзакции в сеансе.</span><span class="sxs-lookup"><span data-stu-id="faa5c-171">This parameter controls the default action taken when the outermost transaction is committed on a session.</span></span> <span data-ttu-id="faa5c-172">Любой допустимый параметр, который можно передать в [жеткоммиттрансактион](./jetcommittransaction-function.md) , также может быть установлен по умолчанию для всех сеансов в экземпляре и (или) для конкретного сеанса.</span><span class="sxs-lookup"><span data-stu-id="faa5c-172">Any valid option that can be passed to [JetCommitTransaction](./jetcommittransaction-function.md) can also be made to be the default for all sessions in an instance and/or for a specific session.</span></span> <span data-ttu-id="faa5c-173">Дополнительные сведения об этих параметрах см. в разделе [жеткоммиттрансактион](./jetcommittransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="faa5c-173">See [JetCommitTransaction](./jetcommittransaction-function.md) for more details on these options.</span></span>

<span data-ttu-id="faa5c-174">Этот параметр влияет на надежность и производительность транзакций.</span><span class="sxs-lookup"><span data-stu-id="faa5c-174">This parameter has an impact on the reliability and performance of transactions.</span></span> <span data-ttu-id="faa5c-175">Дополнительные сведения см. в разделе [жеткоммиттрансактион](./jetcommittransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="faa5c-175">Please see [JetCommitTransaction](./jetcommittransaction-function.md) for more details.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-176">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-176">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-177">0</span><span class="sxs-lookup"><span data-stu-id="faa5c-177">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-178">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-179">JET_GRBIT (целое число)</span><span class="sxs-lookup"><span data-stu-id="faa5c-179">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-180">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-181">Допустимый параметр для Жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="faa5c-181">A valid option for JetCommitTransaction</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-182">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-182">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-183">Экземпляр или сеанс</span><span class="sxs-lookup"><span data-stu-id="faa5c-183">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-184">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-184">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-185">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-185">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-186">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-186">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-187">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-187">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-188">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-189">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-190">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-191">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-191">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-192">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-193">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-194">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-195">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-195">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-196">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-197">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-198">*JET_paramDeleteOldLogs*</span><span class="sxs-lookup"><span data-stu-id="faa5c-198">*JET_paramDeleteOldLogs*</span></span>  
<span data-ttu-id="faa5c-199">48</span><span class="sxs-lookup"><span data-stu-id="faa5c-199">48</span></span>  

<span data-ttu-id="faa5c-200">Если этот параметр имеет значение true и файлы журнала транзакций, на которые указывает путь к файлу журнала (**JET_paramLogFilePath**), имеют устаревшую версию, эти файлы журнала транзакций будут автоматически удалены.</span><span class="sxs-lookup"><span data-stu-id="faa5c-200">When this parameter is true and the transaction log files pointed to by the log file path (**JET_paramLogFilePath**) are all of an obsolete version then those transaction log files will be automatically deleted.</span></span>

<span data-ttu-id="faa5c-201">**Windows 2000:**  При обновлении базы данных с Windows NT до Windows 2000 следует соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="faa5c-201">**Windows 2000:**  Care must be taken with the use of this parameter when upgrading a database from Windows NT to Windows 2000.</span></span> <span data-ttu-id="faa5c-202">Если база данных находится в нестабильном состоянии и старые файлы журнала удалены, содержимое базы данных будет потеряно.</span><span class="sxs-lookup"><span data-stu-id="faa5c-202">If the database is not in a consistent state and the old log files are deleted then the contents of the database will be lost.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-203">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-203">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-204"><strong>Windows 2000:</strong>  IsFalse</span><span class="sxs-lookup"><span data-stu-id="faa5c-204"><strong>Windows 2000:</strong>  False</span></span></p>
<p><span data-ttu-id="faa5c-205"><strong>Windows XP:</strong>  Условия</span><span class="sxs-lookup"><span data-stu-id="faa5c-205"><strong>Windows XP:</strong>  True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-206">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-206">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-207">Логическое</span><span class="sxs-lookup"><span data-stu-id="faa5c-207">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-208">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-208">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-209">False, true</span><span class="sxs-lookup"><span data-stu-id="faa5c-209">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-210">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-210">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-211">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-211">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-212">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-212">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-213">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-213">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-214">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-214">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-215">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-215">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-216">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-216">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-217">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-217">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-218">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-218">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-219">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-219">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-220">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-220">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-221">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-221">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-222">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-222">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-223">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-223">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-224">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-224">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-225">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-225">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-226">*JET_paramIgnoreLogVersion*</span><span class="sxs-lookup"><span data-stu-id="faa5c-226">*JET_paramIgnoreLogVersion*</span></span>  
<span data-ttu-id="faa5c-227">47</span><span class="sxs-lookup"><span data-stu-id="faa5c-227">47</span></span>  

<span data-ttu-id="faa5c-228">Если этот параметр имеет значение true, то ядро СУБД не будет проверять номер версии файла журнала транзакций во время [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="faa5c-228">If this parameter is true then the database engine will not validate the transaction log file version number during [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="faa5c-229">**Windows XP:**  Начиная с Windows XP этот параметр устарел и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-229">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-230">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-230">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="faa5c-231">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-232">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-232">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-233">Логическое</span><span class="sxs-lookup"><span data-stu-id="faa5c-233">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-234">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-234">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-235">False, true</span><span class="sxs-lookup"><span data-stu-id="faa5c-235">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-236">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-236">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-237">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-237">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-238">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-238">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-239">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-239">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-240">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-240">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-241">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-242">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-242">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-243">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-243">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-244">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-244">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-245">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-246">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-246">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-247">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-247">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-248">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-248">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-249">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-249">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-250">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-250">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-251">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-251">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-252">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="faa5c-252">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="faa5c-253">136</span><span class="sxs-lookup"><span data-stu-id="faa5c-253">136</span></span>  

<span data-ttu-id="faa5c-254">Этот параметр обеспечивает обратную совместимость с соглашениями об именовании файлов более ранних версий ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-254">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span>

<span data-ttu-id="faa5c-255">В настоящее время поддерживаются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="faa5c-255">The following options are currently supported:</span></span>

<span data-ttu-id="faa5c-256">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="faa5c-256">JET_bitESE98FileNames</span></span>

<span data-ttu-id="faa5c-257">При наличии этого параметра ядро СУБД будет использовать для своих файлов следующие соглашения об именовании:</span><span class="sxs-lookup"><span data-stu-id="faa5c-257">When this option is present then the database engine will use the following naming conventions for its files:</span></span>

  - <span data-ttu-id="faa5c-258">Будут использоваться файлы журнала транзакций. Журнал для расширения файла</span><span class="sxs-lookup"><span data-stu-id="faa5c-258">Transaction Log files will use .LOG for their file extension</span></span>

  - <span data-ttu-id="faa5c-259">Файлы контрольных точек будут использовать. CHK для расширения файла</span><span class="sxs-lookup"><span data-stu-id="faa5c-259">Checkpoint files will use .CHK for their file extension</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-260">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-261">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="faa5c-261">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-262">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-263">JET_GRBIT (целое число)</span><span class="sxs-lookup"><span data-stu-id="faa5c-263">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-264">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-265">0, JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="faa5c-265">0, JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-266">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-267">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-268">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-269">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-270">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-271">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-272">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-273">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-273">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-274">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-275">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-276">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-277">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-278">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-279">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-280">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-281">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="faa5c-281">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-282">*JET_paramLogBuffers*</span><span class="sxs-lookup"><span data-stu-id="faa5c-282">*JET_paramLogBuffers*</span></span>  
<span data-ttu-id="faa5c-283">12</span><span class="sxs-lookup"><span data-stu-id="faa5c-283">12</span></span>  

<span data-ttu-id="faa5c-284">Этот параметр настраивает объем памяти, используемый для кэширования записей журнала, прежде чем они будут записаны в файл журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="faa5c-284">This parameter will configure the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="faa5c-285">Единицей для этого параметра является размер сектора тома, содержащего файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="faa5c-285">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="faa5c-286">Размер сектора почти всегда 512 байт, поэтому можно считать, что размер для единицы является надежным.</span><span class="sxs-lookup"><span data-stu-id="faa5c-286">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span>

<span data-ttu-id="faa5c-287">Этот параметр влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="faa5c-287">This parameter has an impact on performance.</span></span> <span data-ttu-id="faa5c-288">Когда ядро СУБД находится в режиме высокой нагрузки на обновление, этот буфер может быстро стать полностью загруженным.</span><span class="sxs-lookup"><span data-stu-id="faa5c-288">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="faa5c-289">Больший размер кэша для файла журнала транзакций очень важен для хорошего уровня производительности при такой высокой нагрузке.</span><span class="sxs-lookup"><span data-stu-id="faa5c-289">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="faa5c-290">Значение по умолчанию для этого случая известно слишком мало.</span><span class="sxs-lookup"><span data-stu-id="faa5c-290">The default is known to be too small for this case.</span></span>

<span data-ttu-id="faa5c-291">**Windows XP и windows 2000:**  В Windows XP и предыдущих выпусках не рекомендуется задавать для этого параметра количество буферов размером больше половины (в байтах), чем половина размера файла журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="faa5c-291">**Windows XP and Windows 2000:**  On Windows XP and previous releases, it is not recommended to set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-292">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-292">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-293"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  80</span><span class="sxs-lookup"><span data-stu-id="faa5c-293"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80</span></span></p>
<p><span data-ttu-id="faa5c-294"><strong>Windows Vista:</strong>  126</span><span class="sxs-lookup"><span data-stu-id="faa5c-294"><strong>Windows Vista:</strong>  126</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-295">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-295">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-296">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="faa5c-296">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-297">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-297">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-298"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  80 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="faa5c-298"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80 – 2147483647</span></span></p>
<p><span data-ttu-id="faa5c-299"><strong>Windows Vista:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="faa5c-299"><strong>Windows Vista:</strong>  1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-300">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-300">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-301">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-301">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-302">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-302">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-303">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-303">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-304">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-304">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-305">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-305">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-306">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-306">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-307">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-307">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-308">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-308">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-309">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-309">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-310">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-310">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-311">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-311">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-312">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-312">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-313">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-313">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-314">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-314">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-315">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-315">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-316">*JET_paramLogCheckpointPeriod*</span><span class="sxs-lookup"><span data-stu-id="faa5c-316">*JET_paramLogCheckpointPeriod*</span></span>  
<span data-ttu-id="faa5c-317">14</span><span class="sxs-lookup"><span data-stu-id="faa5c-317">14</span></span>  

<span data-ttu-id="faa5c-318">Этот параметр настраивает ядро СУБД на создание контрольной точки при создании указанного числа секторов файла журнала.</span><span class="sxs-lookup"><span data-stu-id="faa5c-318">This parameter configures the database engine to take a checkpoint when the specified number of log file sectors has been generated.</span></span>

<span data-ttu-id="faa5c-319">**Windows XP:**  Начиная с Windows XP этот параметр устарел и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-319">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-320">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-320">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-321">1024</span><span class="sxs-lookup"><span data-stu-id="faa5c-321">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-322">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-322">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-323">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="faa5c-323">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-324">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-324">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-325">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="faa5c-325">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-326">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-327">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-328">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-329">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-330">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-331">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-331">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-332">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-333">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-334">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-335">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-336">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-337">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-338">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-339">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-340">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-341">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-342">*JET_paramLogFileCreateAsynch*</span><span class="sxs-lookup"><span data-stu-id="faa5c-342">*JET_paramLogFileCreateAsynch*</span></span>  
<span data-ttu-id="faa5c-343">69</span><span class="sxs-lookup"><span data-stu-id="faa5c-343">69</span></span>  

<span data-ttu-id="faa5c-344">Если для этого параметра задано значение true, то ядро СУБД создаст следующий файл журнала транзакций по мере использования текущего файла журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="faa5c-344">When this parameter is set to true, the database engine will create the next transaction log file as the current transaction log file is consumed.</span></span> <span data-ttu-id="faa5c-345">Цель заключается в уменьшении времени, затраченного на переключение с одного файла журнала транзакций на следующий при интенсивной нагрузке на обновления.</span><span class="sxs-lookup"><span data-stu-id="faa5c-345">The intent is to minimize the time spent switching from one transaction log file to the next under a heavy update load.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-346">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-347">True</span><span class="sxs-lookup"><span data-stu-id="faa5c-347">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-348">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-349">Логическое</span><span class="sxs-lookup"><span data-stu-id="faa5c-349">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-350">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-351">False, true</span><span class="sxs-lookup"><span data-stu-id="faa5c-351">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-352">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-353">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-354">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-355">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-356">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-357">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-358">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-359">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-359">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-360">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-361">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-362">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-363">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-364">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-365">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-366">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-367">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="faa5c-367">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-368">*JET_paramLogFilePath*</span><span class="sxs-lookup"><span data-stu-id="faa5c-368">*JET_paramLogFilePath*</span></span>  
<span data-ttu-id="faa5c-369">2</span><span class="sxs-lookup"><span data-stu-id="faa5c-369">2</span></span> 

<span data-ttu-id="faa5c-370">Этот параметр указывает относительный или абсолютный путь файловой системы к папке, которая будет содержать журналы транзакций для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="faa5c-370">This parameter indicates the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span> <span data-ttu-id="faa5c-371">Путь должен заканчиваться символом обратной косой черты, который указывает на то, что целевой путь является папкой.</span><span class="sxs-lookup"><span data-stu-id="faa5c-371">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="faa5c-372">Файлы журнала транзакций содержат сведения, необходимые для перевода файлов базы данных в целостное состояние после сбоя.</span><span class="sxs-lookup"><span data-stu-id="faa5c-372">The transaction log files contain the information required to bring the database files to a consistent state after a crash.</span></span> <span data-ttu-id="faa5c-373">Обычно они называются EDB \* . Журналь.</span><span class="sxs-lookup"><span data-stu-id="faa5c-373">They are typically named EDB\*.LOG.</span></span> <span data-ttu-id="faa5c-374">Содержимое файлов журнала транзакций так же важно (если не больше), чем сами файлы базы данных.</span><span class="sxs-lookup"><span data-stu-id="faa5c-374">The contents of the transaction log files are just as important (if not more so) than the database files themselves.</span></span> <span data-ttu-id="faa5c-375">Необходимо выполнить все усилия, чтобы защитить их.</span><span class="sxs-lookup"><span data-stu-id="faa5c-375">Every effort should be made to protect them.</span></span>

<span data-ttu-id="faa5c-376">Также будут использоваться дополнительные резервные файлы журналов с именем RES1. LOG и RES2. Журнал хранится вместе с обычными файлами журнала.</span><span class="sxs-lookup"><span data-stu-id="faa5c-376">There will also be additional reserve log files named RES1.LOG and RES2.LOG stored along with the ordinary log files.</span></span> <span data-ttu-id="faa5c-377">Содержимое этих файлов не имеет значения, так как их единственная цель — резервировать место на диске, чтобы обеспечить корректное завершение работы механизма в сценарии с низким уровнем дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="faa5c-377">The contents of these files are not important as their only purpose is to reserve disk space to allow the engine to shut down gracefully in a low disk scenario.</span></span> <span data-ttu-id="faa5c-378">Они также будут временным файлом журнала, обычно именуемым ЕДБТМП. Выполните вход в эту же папку.</span><span class="sxs-lookup"><span data-stu-id="faa5c-378">These will also be a temporary log file typically named EDBTMP.LOG in this same folder.</span></span> <span data-ttu-id="faa5c-379">Содержимое этого файла не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="faa5c-379">The contents of this file are not important either.</span></span> <span data-ttu-id="faa5c-380">Этот файл является новым файлом журнала, подготовленным для использования.</span><span class="sxs-lookup"><span data-stu-id="faa5c-380">This file is a new log file being prepared for use.</span></span>

<span data-ttu-id="faa5c-381">Свойства тома узла файлов журнала транзакций и их размещение относительно других файлов, используемых ядром СУБД, может существенно повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="faa5c-381">The properties of the host volume of the transaction log files and their placement relative to the other files used by the database engine can dramatically impact performance.</span></span>

<span data-ttu-id="faa5c-382">**Примечание**  .  Если указан относительный путь, он будет относиться к текущему рабочему каталогу процесса, в котором размещается приложение, использующее ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-382">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-383">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-384">&quot;.\& представления</span><span class="sxs-lookup"><span data-stu-id="faa5c-384">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-385">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-386">Путь к папке (строка)</span><span class="sxs-lookup"><span data-stu-id="faa5c-386">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-387">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-388">0 – 246 символов</span><span class="sxs-lookup"><span data-stu-id="faa5c-388">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-389">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-390">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-390">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-391">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-392">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-392">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-393">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-394">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-395">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-396">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-396">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-397">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-398">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-398">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-399">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-400">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-401">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-402">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-403">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-404">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-405">*JET_paramLogFileSize*</span><span class="sxs-lookup"><span data-stu-id="faa5c-405">*JET_paramLogFileSize*</span></span>  
<span data-ttu-id="faa5c-406">11</span><span class="sxs-lookup"><span data-stu-id="faa5c-406">11</span></span>  

<span data-ttu-id="faa5c-407">Этот параметр позволяет настроить размер файлов журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="faa5c-407">This parameter will configure the size of the transaction log files.</span></span> <span data-ttu-id="faa5c-408">Каждый файл журнала транзакций имеет фиксированный размер.</span><span class="sxs-lookup"><span data-stu-id="faa5c-408">Each transaction log file is a fixed size.</span></span> <span data-ttu-id="faa5c-409">Размер равен значению параметра системного параметра в единицах, равных 1024 байт.</span><span class="sxs-lookup"><span data-stu-id="faa5c-409">The size is equal to the setting of this system parameter in units of 1024 bytes.</span></span>

<span data-ttu-id="faa5c-410">Этот параметр влияет на надежность.</span><span class="sxs-lookup"><span data-stu-id="faa5c-410">This parameter has an impact on reliability.</span></span> <span data-ttu-id="faa5c-411">Если параметр слишком мал, максимальное число файлов журнала (1048575) будет достигнуто гораздо быстрее.</span><span class="sxs-lookup"><span data-stu-id="faa5c-411">If the setting is too small then the maximum number of log files (1048575) will be reached much faster.</span></span> <span data-ttu-id="faa5c-412">В этом случае экземпляр должен быть завершен аккуратно, существующие файлы журнала должны быть удалены, а экземпляр должен быть перезапущен.</span><span class="sxs-lookup"><span data-stu-id="faa5c-412">When this happens, the instance must be shutdown cleanly, the existing log files must be deleted, and the instance must be restarted.</span></span> <span data-ttu-id="faa5c-413">Это действие не только снизит доступность приложения, но и сделает все предыдущие резервные копии базы данных приложения недействительными.</span><span class="sxs-lookup"><span data-stu-id="faa5c-413">This action will not only reduce the availability of the application but it will also invalidate any previous backups of the application's database.</span></span>

<span data-ttu-id="faa5c-414">Этот параметр влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="faa5c-414">This parameter has an impact on performance.</span></span> <span data-ttu-id="faa5c-415">Если значение параметра слишком велико, [жетинит](./jetinit-function.md) будет работать слишком долго, так как ядро СУБД должно считывать самый самый самый самый новый файл журнала при инициализации.</span><span class="sxs-lookup"><span data-stu-id="faa5c-415">If the setting is very large then [JetInit](./jetinit-function.md) will be slow because the database engine must read the youngest log file (at a minimum) when it initializes.</span></span> <span data-ttu-id="faa5c-416">Если значение параметра слишком велико, то переключение между файлами журнала также займет больше времени.</span><span class="sxs-lookup"><span data-stu-id="faa5c-416">If the setting is very large then it will also take longer to switch between log files.</span></span> <span data-ttu-id="faa5c-417">Если параметр слишком мал, потребуется создать больше файлов журнала для определенного числа обновлений, что приведет к увеличению затрат.</span><span class="sxs-lookup"><span data-stu-id="faa5c-417">If the setting is very small then more log files will need to be created for a given number of updates which will add more overhead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-418">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-418">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-419">5120</span><span class="sxs-lookup"><span data-stu-id="faa5c-419">5120</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-420">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-420">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-421">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="faa5c-421">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-422">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-422">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-423"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  128 – 32768</span><span class="sxs-lookup"><span data-stu-id="faa5c-423"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  128 – 32768</span></span></p>
<p><span data-ttu-id="faa5c-424"><strong>Windows Vista:</strong>  64 – 32768</span><span class="sxs-lookup"><span data-stu-id="faa5c-424"><strong>Windows Vista:</strong>  64 – 32768</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-425">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-425">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-426">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-426">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-427">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-427">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-428">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-429">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-429">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-430">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-430">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-431">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-431">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-432">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-432">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-433">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-433">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-434">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-434">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-435">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-435">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-436">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-436">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-437">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-437">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-438">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-438">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-439">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-439">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-440">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-440">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-441">*JET_paramLogWaitingUserMax*</span><span class="sxs-lookup"><span data-stu-id="faa5c-441">*JET_paramLogWaitingUserMax*</span></span>  
<span data-ttu-id="faa5c-442">15</span><span class="sxs-lookup"><span data-stu-id="faa5c-442">15</span></span>  

<span data-ttu-id="faa5c-443">Этот параметр пытается оптимизировать очистку буфера журнала из-за длительной фиксации, ожидая указанного числа сеансов ожидать устойчивой фиксации до того, как будет произведена очистка, которая может быть использована другой транзакцией.</span><span class="sxs-lookup"><span data-stu-id="faa5c-443">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified number of sessions to wait for a durable commit prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="faa5c-444">**Windows XP:**  Начиная с Windows XP этот параметр устарел и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-444">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-445">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-445">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-446">3</span><span class="sxs-lookup"><span data-stu-id="faa5c-446">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-447">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-447">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-448">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="faa5c-448">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-449">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-449">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-450">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="faa5c-450">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-451">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-451">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-452">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-452">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-453">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-453">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-454">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-454">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-455">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-455">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-456">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-456">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-457">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-457">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-458">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-458">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-459">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-459">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-460">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-461">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-461">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-462">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-463">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-463">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-464">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-465">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-465">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-466">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-466">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-467">*JET_paramRecovery*</span><span class="sxs-lookup"><span data-stu-id="faa5c-467">*JET_paramRecovery*</span></span>  
<span data-ttu-id="faa5c-468">34</span><span class="sxs-lookup"><span data-stu-id="faa5c-468">34</span></span>  

<span data-ttu-id="faa5c-469">Этот параметр является главным коммутатором, который управляет восстановлением после сбоя для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="faa5c-469">This parameter is the master switch that controls crash recovery for an instance.</span></span> <span data-ttu-id="faa5c-470">Если этот параметр имеет значение "on", Овен-восстановление стиля будет использоваться для перевода всех баз данных в экземпляре в целостное состояние в случае сбоя процесса или компьютера.</span><span class="sxs-lookup"><span data-stu-id="faa5c-470">If this parameter is set to "On" then ARIES style recovery will be used to bring all databases in the instance to a consistent state in the event of a process or machine crash.</span></span> <span data-ttu-id="faa5c-471">Если этот параметр имеет значение OFF, то управление всеми базами данных в экземпляре будет осуществляться без использования аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="faa5c-471">If this parameter is set to "Off" then all databases in the instance will be managed without the benefit of crash recovery.</span></span> <span data-ttu-id="faa5c-472">Это означает, что если экземпляр не завершается чисто с помощью [жеттерм](./jetterm-function.md) до завершения процесса или завершения работы компьютера, содержимое всех баз данных в этом экземпляре будет повреждено.</span><span class="sxs-lookup"><span data-stu-id="faa5c-472">That is to say, that if the instance is not shut down cleanly using [JetTerm](./jetterm-function.md) prior to the process exiting or machine shutdown then the contents of all databases in that instance will be corrupted.</span></span>

<span data-ttu-id="faa5c-473">Отключение восстановления полезно в особых обстоятельствах, когда известно, что содержимое базы данных не полезно в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="faa5c-473">Disabling recovery is useful in special circumstances where it is known that the contents of a database are not useful in the event of a crash.</span></span> <span data-ttu-id="faa5c-474">Во всех остальных случаях необходимо включить восстановление.</span><span class="sxs-lookup"><span data-stu-id="faa5c-474">Recovery should be enabled for all other cases.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-475">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-475">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-476">&quot;Вкл.&quot;</span><span class="sxs-lookup"><span data-stu-id="faa5c-476">&quot;On&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-477">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-477">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-478">Строка</span><span class="sxs-lookup"><span data-stu-id="faa5c-478">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-479">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-479">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-480">0 – 259 символов</span><span class="sxs-lookup"><span data-stu-id="faa5c-480">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-481">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-481">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-482">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-482">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-483">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-483">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-484">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-484">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-485">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-485">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-486">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-486">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-487">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-487">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-488">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-488">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-489">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-489">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-490">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-490">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-491">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-491">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-492">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-492">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-493">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-493">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-494">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-494">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-495">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-495">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-496">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-496">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-497">*JET_paramSystemPath*</span><span class="sxs-lookup"><span data-stu-id="faa5c-497">*JET_paramSystemPath*</span></span>  
<span data-ttu-id="faa5c-498">0</span><span class="sxs-lookup"><span data-stu-id="faa5c-498">0</span></span>  

<span data-ttu-id="faa5c-499">Этот параметр указывает относительный или абсолютный путь файловой системы к папке, которая будет содержать файл контрольных точек для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="faa5c-499">This parameter indicates the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span> <span data-ttu-id="faa5c-500">Путь должен заканчиваться символом обратной косой черты, который указывает на то, что целевой путь является папкой.</span><span class="sxs-lookup"><span data-stu-id="faa5c-500">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="faa5c-501">Файл контрольных точек — это простой файл, поддерживаемый для экземпляра, который запоминает самый старый файл журнала транзакций, который необходимо воспроизвести, чтобы перевести все базы данных в экземпляре в целостное состояние после сбоя.</span><span class="sxs-lookup"><span data-stu-id="faa5c-501">The checkpoint file is a simple file maintained per instance that remembers the oldest transaction log file that must be replayed to bring all databases in that instance to a consistent state after a crash.</span></span> <span data-ttu-id="faa5c-502">Файл контрольных точек обычно называется EDB. CHK.</span><span class="sxs-lookup"><span data-stu-id="faa5c-502">The checkpoint file is typically named EDB.CHK.</span></span>

<span data-ttu-id="faa5c-503">**Примечание**  .  Если указан относительный путь, он будет относиться к текущему рабочему каталогу процесса, в котором размещается приложение, использующее ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-503">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-504">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-504">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-505">&quot;.\& представления</span><span class="sxs-lookup"><span data-stu-id="faa5c-505">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-506">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-506">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-507">Путь к папке (строка)</span><span class="sxs-lookup"><span data-stu-id="faa5c-507">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-508">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-508">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-509">0 – 246 символов</span><span class="sxs-lookup"><span data-stu-id="faa5c-509">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-510">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-510">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-511">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-511">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-512">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-512">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-513">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-513">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-514">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-514">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-515">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-515">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-516">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-516">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-517">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-517">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-518">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-518">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-519">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-519">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-520">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-520">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-521">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-521">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-522">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-522">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-523">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-523">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-524">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-524">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-525">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-525">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-526">*JET_paramWaitLogFlush*</span><span class="sxs-lookup"><span data-stu-id="faa5c-526">*JET_paramWaitLogFlush*</span></span>  
<span data-ttu-id="faa5c-527">13</span><span class="sxs-lookup"><span data-stu-id="faa5c-527">13</span></span> 

<span data-ttu-id="faa5c-528">Этот параметр пытается оптимизировать запись буфера журнала, вызванная устойчивой фиксацией, в ожидании указанного периода времени до выполнения сброса, в результате чего другая транзакция будет совместно использовать эту запись.</span><span class="sxs-lookup"><span data-stu-id="faa5c-528">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified time period prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="faa5c-529">**Windows XP:**  Начиная с Windows XP этот параметр устарел и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="faa5c-529">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-530">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-530">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-531">0</span><span class="sxs-lookup"><span data-stu-id="faa5c-531">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-532">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-532">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-533">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="faa5c-533">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-534">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-534">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-535">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="faa5c-535">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-536">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-536">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-537">Экземпляр или сеанс</span><span class="sxs-lookup"><span data-stu-id="faa5c-537">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-538">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-538">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-539">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-539">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-540">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-540">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-541">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-541">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-542">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-542">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-543">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-543">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-544">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-544">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-545">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-545">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-546">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-546">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-547">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-547">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-548">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-548">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-549">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-549">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-550">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-550">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-551">Все</span><span class="sxs-lookup"><span data-stu-id="faa5c-551">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faa5c-552">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="faa5c-552">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="faa5c-553">136</span><span class="sxs-lookup"><span data-stu-id="faa5c-553">136</span></span>  

<span data-ttu-id="faa5c-554">Этот параметр используется для указания функций совместимости имен файлов, которые должны поддерживаться в Windows Server 2003 и предыдущей схеме именования файлов.</span><span class="sxs-lookup"><span data-stu-id="faa5c-554">This parameter is used to specify the file naming compatibility features to maintain with the Windows Server 2003 and previous file naming scheme.</span></span> <span data-ttu-id="faa5c-555">Дополнительные сведения о различных файлах и их именовании см. в разделе [расширяемые файлы подсистемы хранилища](./extensible-storage-engine-files.md).</span><span class="sxs-lookup"><span data-stu-id="faa5c-555">For more information about the different files and their naming see [Extensible Storage Engine Files](./extensible-storage-engine-files.md).</span></span>

<span data-ttu-id="faa5c-556">JET_bitESE98FileNames гарантирует, что расширение файла, используемое в файлах журнала транзакций и файл контрольных точек, будет таким же, как и в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="faa5c-556">The JET_bitESE98FileNames ensures the file extension used on the transaction log files and the checkpoint file are the same as that used in Windows Server 2003.</span></span> <span data-ttu-id="faa5c-557">Обратите внимание, что при обновлении с Windows Server 2003 этот бит по-прежнему не требуется указывать, так как ядро автоматически обновит расширения файлов, если JET_paramCircularLog имеет значение **true** или если JET_paramCircularLog имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="faa5c-557">Note if upgrading from Windows Server 2003, this bit still need not be specified, as the engine will automatically upgrade the file extensions if JET_paramCircularLog is set to **true**, or maintain the older log extension if JET_paramCircularLog is **false**.</span></span>

<span data-ttu-id="faa5c-558">**Примечание**  .  Чтобы задать бит, необходимо сначала извлечь значение, а затем «или» в нужном бит совместимости.</span><span class="sxs-lookup"><span data-stu-id="faa5c-558">**Note**  To set a bit, the value should first be retrieved, and then "or" in the desired compatibility bit.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-559">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="faa5c-559">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-560">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="faa5c-560">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-561">Тип:</span><span class="sxs-lookup"><span data-stu-id="faa5c-561">Type:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-562">JET_GRBIT (целое число)</span><span class="sxs-lookup"><span data-stu-id="faa5c-562">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-563">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="faa5c-563">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-564">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="faa5c-564">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-565">Область.</span><span class="sxs-lookup"><span data-stu-id="faa5c-565">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-566">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="faa5c-566">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-567">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-567">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-568">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-568">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-569">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="faa5c-569">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-570">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-570">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-571">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="faa5c-571">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-572">Да</span><span class="sxs-lookup"><span data-stu-id="faa5c-572">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-573">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-573">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-574">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-574">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-575">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="faa5c-575">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-576">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-576">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-577">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="faa5c-577">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-578">Нет</span><span class="sxs-lookup"><span data-stu-id="faa5c-578">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-579">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="faa5c-579">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faa5c-580">Начиная с Windows Server 2008 и Windows Vista</span><span class="sxs-lookup"><span data-stu-id="faa5c-580">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a><span data-ttu-id="faa5c-581">Требования</span><span class="sxs-lookup"><span data-stu-id="faa5c-581">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-582"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="faa5c-582"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="faa5c-583">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="faa5c-583">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa5c-584"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="faa5c-584"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="faa5c-585">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="faa5c-585">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa5c-586"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="faa5c-586"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="faa5c-587">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="faa5c-587">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="faa5c-588">См. также:</span><span class="sxs-lookup"><span data-stu-id="faa5c-588">See Also</span></span>

[<span data-ttu-id="faa5c-589">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="faa5c-589">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="faa5c-590">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="faa5c-590">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="faa5c-591">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="faa5c-591">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="faa5c-592">жетинит</span><span class="sxs-lookup"><span data-stu-id="faa5c-592">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="faa5c-593">жеттерм</span><span class="sxs-lookup"><span data-stu-id="faa5c-593">JetTerm</span></span>](./jetterm-function.md)
