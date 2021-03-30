---
description: Дополнительные сведения о функции JetExternalRestore2
title: Функция JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998957"
---
# <a name="jetexternalrestore2-function"></a><span data-ttu-id="05818-103">Функция JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="05818-103">JetExternalRestore2 Function</span></span>


<span data-ttu-id="05818-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="05818-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore2-function"></a><span data-ttu-id="05818-105">Функция JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="05818-105">JetExternalRestore2 Function</span></span>

<span data-ttu-id="05818-106">Функция **JetExternalRestore2** восстанавливает внешнюю резервную копию, созданную с помощью внешних API-интерфейсов резервного копирования, и предоставляет контрольные точки, используемые для циклического ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="05818-106">The **JetExternalRestore2** function restores an external backup that was taken with the external backup APIs and provides checkpoints to use for circular logging operations.</span></span> <span data-ttu-id="05818-107">Это называется жесткое восстановление, которое аналогично, но отличается от программного восстановления, выполняемого функцией [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="05818-107">This is known as hard recovery, which is similar but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

<span data-ttu-id="05818-108">**Windows XP: JetExternalRestore2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="05818-108">**Windows XP:  JetExternalRestore2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="05818-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="05818-109">Parameters</span></span>

<span data-ttu-id="05818-110">*сзчеккпоинтфилепас*</span><span class="sxs-lookup"><span data-stu-id="05818-110">*szCheckpointFilePath*</span></span>

<span data-ttu-id="05818-111">Путь к файлу контрольных точек, который будет использоваться во время восстановления, если *сзтаржетинстанцечеккпоинтпас* не указан или этот путь имеет активный или выполняющийся экземпляр.</span><span class="sxs-lookup"><span data-stu-id="05818-111">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or that path has an active or running instance.</span></span>

<span data-ttu-id="05818-112">*сзлогпас*</span><span class="sxs-lookup"><span data-stu-id="05818-112">*szLogPath*</span></span>

<span data-ttu-id="05818-113">Путь или каталог журналов для последнего этапа (отмены) восстановления и, возможно, для журналов наката.</span><span class="sxs-lookup"><span data-stu-id="05818-113">The path or directory for the logs for the final phase (undo) of the recovery and possibly for the roll forward logs.</span></span> <span data-ttu-id="05818-114">Этот путь может быть таким же, как и *сзбаккуплогпас*.</span><span class="sxs-lookup"><span data-stu-id="05818-114">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="05818-115">*ргрстмап*</span><span class="sxs-lookup"><span data-stu-id="05818-115">*rgrstmap*</span></span>

<span data-ttu-id="05818-116">Это массив структур [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="05818-116">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="05818-117">Это схема старых и новых путей к базам данных или имен файлов.</span><span class="sxs-lookup"><span data-stu-id="05818-117">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="05818-118">Это используется, так как базы данных могут быть восстановлены в расположении, отличном от расположения, из которого они были созданы.</span><span class="sxs-lookup"><span data-stu-id="05818-118">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="05818-119">В случае, когда несколько баз данных присоединены к одному набору журналов, на карте восстановления можно указать подмножество восстанавливаемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="05818-119">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of the databases to restore.</span></span>

<span data-ttu-id="05818-120">*крстфилемап*</span><span class="sxs-lookup"><span data-stu-id="05818-120">*crstfilemap*</span></span>

<span data-ttu-id="05818-121">Число записей в параметре массива *ргрстмап* .</span><span class="sxs-lookup"><span data-stu-id="05818-121">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="05818-122">*сзбаккуплогпас*</span><span class="sxs-lookup"><span data-stu-id="05818-122">*szBackupLogPath*</span></span>

<span data-ttu-id="05818-123">Путь к каталогу, в который восстанавливаются файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="05818-123">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="05818-124">Это журналы, которые были считаны во время внешней последовательности резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="05818-124">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="05818-125">Этот путь может быть таким же, как и *сзлогпас*.</span><span class="sxs-lookup"><span data-stu-id="05818-125">This path may be the same as the *szLogPath*.</span></span>

<span data-ttu-id="05818-126">*плогинфо*</span><span class="sxs-lookup"><span data-stu-id="05818-126">*pLogInfo*</span></span>

<span data-ttu-id="05818-127">*Плогинфо* описывает несколько аспектов восстановления журналов резервного копирования. Этот параметр позволяет **JetExternalRestore2** использовать явные параметры *женлов* и *женхигх* , которые имеют **JetExternalRestore2** , а также базовое имя журнала вместо предполагаемого базового имени журнала "edb".</span><span class="sxs-lookup"><span data-stu-id="05818-127">The *pLogInfo* describes several aspects of the backup logs to recovery, this parameter allows **JetExternalRestore2** to take the explicit *genLow* and *genHigh* parameters that **JetExternalRestore2** has, as well as the base log name, instead of a presumed log base name of "edb".</span></span>

<span data-ttu-id="05818-128">*сзтаржетинстанценаме*</span><span class="sxs-lookup"><span data-stu-id="05818-128">*szTargetInstanceName*</span></span>

<span data-ttu-id="05818-129">Этот параметр является устаревшим и не может использоваться в приложении.</span><span class="sxs-lookup"><span data-stu-id="05818-129">This parameter is deprecated and cannot be used in your application.</span></span>

<span data-ttu-id="05818-130">*сзтаржетинстанцелогпас*</span><span class="sxs-lookup"><span data-stu-id="05818-130">*szTargetInstanceLogPath*</span></span>

<span data-ttu-id="05818-131">Путь для наката журналов, если расположение журналов для наката находится в активном наборе или экземпляре ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="05818-131">The path for the roll forward logs if the location of the logs you would like to roll forward are in an active logging set or instance.</span></span> <span data-ttu-id="05818-132">Не следует указывать, если целевой экземпляр использует циклическое ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="05818-132">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="05818-133">*сзтаржетинстанцечеккпоинтпас*</span><span class="sxs-lookup"><span data-stu-id="05818-133">*szTargetInstanceCheckpointPath*</span></span>

<span data-ttu-id="05818-134">Путь для контрольной точки во время восстановления, если на этом целевом объекте не работает активный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="05818-134">The path for the checkpoint during recovery if there is no active instance running at this target.</span></span> <span data-ttu-id="05818-135">Не следует указывать, если целевой экземпляр использует циклическое ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="05818-135">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="05818-136">*PFN*</span><span class="sxs-lookup"><span data-stu-id="05818-136">*pfn*</span></span>

<span data-ttu-id="05818-137">Обратный вызов состояния, который сообщает о ходе восстановления.</span><span class="sxs-lookup"><span data-stu-id="05818-137">The status callback, which reports the progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="05818-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05818-138">Return Value</span></span>

<span data-ttu-id="05818-139">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="05818-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="05818-140">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="05818-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05818-141">Код возврата</span><span class="sxs-lookup"><span data-stu-id="05818-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="05818-142">Описание</span><span class="sxs-lookup"><span data-stu-id="05818-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05818-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="05818-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="05818-144">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="05818-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05818-145">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="05818-145">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="05818-146">Указанный <em>сзтаржетинстанцелогпас</em> не принадлежит инициализированному экземпляру.</span><span class="sxs-lookup"><span data-stu-id="05818-146">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="05818-147">Эта ошибка будет возвращена только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="05818-147">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05818-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="05818-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="05818-149">Это указывает, что база данных повреждена или нераспознанный файл.</span><span class="sxs-lookup"><span data-stu-id="05818-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05818-150">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="05818-150">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="05818-151">Эта ошибка возвращается, если одна из файлов журнала в <em>сзбаккуплогпас</em>имеет более позднюю версию журнала, указанную в <em>женхигх</em> или <em>плогинфо. улженхигх</em>.</span><span class="sxs-lookup"><span data-stu-id="05818-151">This error is returned if one for the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05818-152">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="05818-152">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="05818-153">Не удалось выполнить операцию, так как не удалось открыть запрошенный файл, так как он не найден по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="05818-153">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05818-154">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="05818-154">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="05818-155">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="05818-155">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="05818-156">Это может произойти для <a href="gg294088(v=exchg.10).md">жетекстерналресторе</a>и т. д., если <em>сзтаржетчеккпоинтпас</em> и <em>сзтаржетинстанцелогпас</em> либо не указаны одновременно, либо не указаны одновременно.</span><span class="sxs-lookup"><span data-stu-id="05818-156">This can happen for <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="05818-157">То есть они должны сопоставляться и быть одновременно указаны, либо не указаны одновременно.</span><span class="sxs-lookup"><span data-stu-id="05818-157">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05818-158">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="05818-158">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="05818-159">Не удалось выполнить операцию, так как не удалось найти указанный путь.</span><span class="sxs-lookup"><span data-stu-id="05818-159">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05818-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="05818-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="05818-161">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="05818-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05818-162">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="05818-162">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="05818-163">Эта ошибка возвращается, если файл базы данных, указанный во время восстановления, не является базой данных, для которой была создана резервная копия с внешней резервной копией.</span><span class="sxs-lookup"><span data-stu-id="05818-163">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05818-164">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="05818-164">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="05818-165">Ядру СУБД не удается выполнить внешнее восстановление или принудительное восстановление в режиме одиночного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="05818-165">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="05818-166">Эта ошибка будет возвращена только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="05818-166">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05818-167">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="05818-167">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="05818-168">Эта ошибка возвращается, если один из файлов журнала в <em>сзбаккуплогпас</em>имеет следующее создание журнала, заданное <em>женлов</em> или <em>плогинфо. улженлов</em>.</span><span class="sxs-lookup"><span data-stu-id="05818-168">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05818-169">При успешном выполнении все базы данных из *ргрстмап* полностью восстанавливаются, а в состоянии чистого или устойчивого состояния.</span><span class="sxs-lookup"><span data-stu-id="05818-169">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="05818-170">На этом этапе базу данных можно повторно подключить к существующему экземпляру.</span><span class="sxs-lookup"><span data-stu-id="05818-170">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="05818-171">В случае сбоя подсистема не смогла восстановить базу данных.</span><span class="sxs-lookup"><span data-stu-id="05818-171">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="05818-172">База данных находится в недопустимом состоянии, и для повторного восстановления необходимо восстановить всю базу данных.</span><span class="sxs-lookup"><span data-stu-id="05818-172">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="05818-173">Как правило, источником такой ситуации является повреждение диска или журнала, а также другой вид непостоянного управления журналом или ненепрерывный набор журналов.</span><span class="sxs-lookup"><span data-stu-id="05818-173">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="05818-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05818-174">Remarks</span></span>

<span data-ttu-id="05818-175">См. [жетекстерналресторе](./jetexternalrestore-function.md).</span><span class="sxs-lookup"><span data-stu-id="05818-175">See [JetExternalRestore](./jetexternalrestore-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="05818-176">Требования</span><span class="sxs-lookup"><span data-stu-id="05818-176">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05818-177"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="05818-177"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="05818-178">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="05818-178">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05818-179"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="05818-179"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="05818-180">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="05818-180">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05818-181"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="05818-181"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="05818-182">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="05818-182">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05818-183"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="05818-183"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="05818-184">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="05818-184">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05818-185"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="05818-185"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="05818-186">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="05818-186">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05818-187"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="05818-187"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="05818-188">Реализуется как <strong>JetExternalRestore2W</strong> (Юникод) и <strong>JetExternalRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="05818-188">Implemented as <strong>JetExternalRestore2W</strong> (Unicode) and <strong>JetExternalRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="05818-189">См. также:</span><span class="sxs-lookup"><span data-stu-id="05818-189">See Also</span></span>

[<span data-ttu-id="05818-190">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="05818-190">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="05818-191">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="05818-191">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="05818-192">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="05818-192">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="05818-193">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="05818-193">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="05818-194">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="05818-194">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="05818-195">жетекстерналресторе</span><span class="sxs-lookup"><span data-stu-id="05818-195">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="05818-196">жетинит</span><span class="sxs-lookup"><span data-stu-id="05818-196">JetInit</span></span>](./jetinit-function.md)
