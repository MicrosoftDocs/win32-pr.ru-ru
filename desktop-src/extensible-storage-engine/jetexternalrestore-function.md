---
description: Дополнительные сведения о функции Жетекстерналресторе
title: Функция Жетекстерналресторе
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105704037"
---
# <a name="jetexternalrestore-function"></a><span data-ttu-id="96836-103">Функция Жетекстерналресторе</span><span class="sxs-lookup"><span data-stu-id="96836-103">JetExternalRestore Function</span></span>


<span data-ttu-id="96836-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="96836-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore-function"></a><span data-ttu-id="96836-105">Функция Жетекстерналресторе</span><span class="sxs-lookup"><span data-stu-id="96836-105">JetExternalRestore Function</span></span>

<span data-ttu-id="96836-106">Функция **жетекстерналресторе** восстанавливает внешнюю резервную копию, созданную с помощью внешних API-интерфейсов резервного копирования, и указывает диапазон номеров файлов журнала для воспроизведения в процессе восстановления.</span><span class="sxs-lookup"><span data-stu-id="96836-106">The **JetExternalRestore** function restores an external backup that was taken with the external backup APIs and specifies a range of log file numbers to replay during the restore process.</span></span> <span data-ttu-id="96836-107">Это называется жесткое восстановление, которое аналогично, но отличается от программного восстановления, выполняемого функцией [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="96836-107">This is known as hard recovery, which is similar to but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="96836-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96836-108">Parameters</span></span>

<span data-ttu-id="96836-109">*сзчеккпоинтфилепас*</span><span class="sxs-lookup"><span data-stu-id="96836-109">*szCheckpointFilePath*</span></span>

<span data-ttu-id="96836-110">Путь к файлу контрольных точек, используемому во время восстановления, если *сзтаржетинстанцечеккпоинтпас* не указан или уже имеет активный или запущенный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="96836-110">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or already has an active or running instance.</span></span>

<span data-ttu-id="96836-111">*сзлогпас*</span><span class="sxs-lookup"><span data-stu-id="96836-111">*szLogPath*</span></span>

<span data-ttu-id="96836-112">Путь или каталог журналов для последнего этапа (отмены) восстановления и, возможно, для журналов наката.</span><span class="sxs-lookup"><span data-stu-id="96836-112">The path or directory for the logs for the final phase (undo) of recovery, and possibly for the roll forward logs.</span></span> <span data-ttu-id="96836-113">Этот путь может быть таким же, как и *сзбаккуплогпас*.</span><span class="sxs-lookup"><span data-stu-id="96836-113">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="96836-114">*ргрстмап*</span><span class="sxs-lookup"><span data-stu-id="96836-114">*rgrstmap*</span></span>

<span data-ttu-id="96836-115">Это массив структур [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="96836-115">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="96836-116">Это схема старых и новых путей к базам данных или имен файлов.</span><span class="sxs-lookup"><span data-stu-id="96836-116">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="96836-117">Это используется, так как базы данных могут быть восстановлены в расположении, отличном от расположения, из которого они были созданы.</span><span class="sxs-lookup"><span data-stu-id="96836-117">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="96836-118">В случае, когда несколько баз данных присоединены к одному набору журналов, на карте восстановления можно указать подмножество баз данных для восстановления.</span><span class="sxs-lookup"><span data-stu-id="96836-118">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of databases to restore.</span></span>

<span data-ttu-id="96836-119">*крстфилемап*</span><span class="sxs-lookup"><span data-stu-id="96836-119">*crstfilemap*</span></span>

<span data-ttu-id="96836-120">Число записей в параметре массива *ргрстмап* .</span><span class="sxs-lookup"><span data-stu-id="96836-120">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="96836-121">*сзбаккуплогпас*</span><span class="sxs-lookup"><span data-stu-id="96836-121">*szBackupLogPath*</span></span>

<span data-ttu-id="96836-122">Путь к каталогу, в который восстанавливаются файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="96836-122">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="96836-123">Это журналы, которые были считаны во время внешней последовательности резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="96836-123">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="96836-124">Этот путь может быть таким же, как и Сзлогпас.</span><span class="sxs-lookup"><span data-stu-id="96836-124">This path may be the same as the szLogPath.</span></span>

<span data-ttu-id="96836-125">*женлов*</span><span class="sxs-lookup"><span data-stu-id="96836-125">*genLow*</span></span>

<span data-ttu-id="96836-126">Минимальный номер файла журнала, который будет воспроизводиться из *сзбаккуплогпас*.</span><span class="sxs-lookup"><span data-stu-id="96836-126">The lowest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="96836-127">Необходимо сохранить полную достоверность беззнакового типа Long, но в текущей версии подсистемы это число является шестнадцатеричным числом в диапазоне от 0x00000 до 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="96836-127">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="96836-128">Это может измениться в будущих версиях.</span><span class="sxs-lookup"><span data-stu-id="96836-128">This may change in future versions.</span></span>

<span data-ttu-id="96836-129">*женхигх*</span><span class="sxs-lookup"><span data-stu-id="96836-129">*genHigh*</span></span>

<span data-ttu-id="96836-130">Максимальный номер файла журнала, который будет воспроизводиться из *сзбаккуплогпас*.</span><span class="sxs-lookup"><span data-stu-id="96836-130">The highest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="96836-131">Необходимо сохранить полную достоверность беззнакового типа Long, но в текущей версии подсистемы это число является шестнадцатеричным числом в диапазоне от 0x00000 до 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="96836-131">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="96836-132">Это может измениться в будущих версиях.</span><span class="sxs-lookup"><span data-stu-id="96836-132">This may change in future versions.</span></span>

<span data-ttu-id="96836-133">*PFN*</span><span class="sxs-lookup"><span data-stu-id="96836-133">*pfn*</span></span>

<span data-ttu-id="96836-134">Обратный вызов состояния, сообщающий о ходе восстановления.</span><span class="sxs-lookup"><span data-stu-id="96836-134">The status callback, to report progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="96836-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96836-135">Return Value</span></span>

<span data-ttu-id="96836-136">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="96836-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="96836-137">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="96836-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96836-138">Код возврата</span><span class="sxs-lookup"><span data-stu-id="96836-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="96836-139">Описание</span><span class="sxs-lookup"><span data-stu-id="96836-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96836-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="96836-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="96836-141">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="96836-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96836-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="96836-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="96836-143">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="96836-143">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96836-144">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="96836-144">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="96836-145">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="96836-145">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="96836-146">Это может произойти для <strong>жетекстерналресторе</strong>и т. д., если <em>сзтаржетчеккпоинтпас</em> и <em>сзтаржетинстанцелогпас</em> либо не указаны одновременно, либо не указаны одновременно.</span><span class="sxs-lookup"><span data-stu-id="96836-146">This can happen for <strong>JetExternalRestore</strong>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="96836-147">То есть они должны сопоставляться и быть одновременно указаны, либо не указаны одновременно.</span><span class="sxs-lookup"><span data-stu-id="96836-147">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96836-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="96836-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="96836-149">Это указывает, что база данных повреждена или нераспознанный файл.</span><span class="sxs-lookup"><span data-stu-id="96836-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96836-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="96836-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="96836-151">Не удалось выполнить операцию, так как не удалось открыть запрошенный файл, так как он не найден по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="96836-151">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96836-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="96836-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="96836-153">Не удалось выполнить операцию, так как не удалось найти указанный путь.</span><span class="sxs-lookup"><span data-stu-id="96836-153">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96836-154">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="96836-154">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="96836-155">Эта ошибка возвращается, если файл базы данных, указанный во время восстановления, не является базой данных, для которой была создана резервная копия с внешней резервной копией.</span><span class="sxs-lookup"><span data-stu-id="96836-155">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96836-156">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="96836-156">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="96836-157">Эта ошибка возвращается, если один из файлов журнала в <em>сзбаккуплогпас</em>имеет следующее создание журнала, заданное <em>женлов</em> или <em>плогинфо. улженлов</em>.</span><span class="sxs-lookup"><span data-stu-id="96836-157">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96836-158">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="96836-158">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="96836-159">Эта ошибка возвращается, если одна из файлов журнала в <em>сзбаккуплогпас</em>имеет более позднюю версию журнала, указанную в <em>женхигх</em> или <em>плогинфо. улженхигх</em>.</span><span class="sxs-lookup"><span data-stu-id="96836-159">This error is returned if one fo the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96836-160">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="96836-160">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="96836-161">Указанный <em>сзтаржетинстанцелогпас</em> не принадлежит инициализированному экземпляру.</span><span class="sxs-lookup"><span data-stu-id="96836-161">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="96836-162">Эта ошибка будет возвращена только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="96836-162">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96836-163">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="96836-163">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="96836-164">Ядру СУБД не удается выполнить внешнее восстановление или принудительное восстановление в режиме одиночного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="96836-164">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="96836-165">Эта ошибка будет возвращена только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="96836-165">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96836-166">При успешном выполнении все базы данных из *ргрстмап* полностью восстанавливаются, а в состоянии чистого или устойчивого состояния.</span><span class="sxs-lookup"><span data-stu-id="96836-166">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="96836-167">На этом этапе базу данных можно повторно подключить к существующему экземпляру.</span><span class="sxs-lookup"><span data-stu-id="96836-167">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="96836-168">В случае сбоя подсистема не смогла восстановить базу данных.</span><span class="sxs-lookup"><span data-stu-id="96836-168">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="96836-169">База данных находится в недопустимом состоянии, и для повторного восстановления необходимо восстановить всю базу данных.</span><span class="sxs-lookup"><span data-stu-id="96836-169">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="96836-170">Как правило, источником такой ситуации является повреждение диска или журнала, а также другой вид непостоянного управления журналом или ненепрерывный набор журналов.</span><span class="sxs-lookup"><span data-stu-id="96836-170">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="96836-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96836-171">Remarks</span></span>

<span data-ttu-id="96836-172">Чтобы понять, как работает «жесткое» восстановление, необходимо понимать, что существует три этапа восстановления, а второй этап может содержать две части.</span><span class="sxs-lookup"><span data-stu-id="96836-172">To understand how a "hard" recovery works, you must understand that there are three phases of recovery, and the second phase can have two parts.</span></span> <span data-ttu-id="96836-173">На этапе I журналы необходимы для обеспечения согласованности резервной копии базы данных (или можно использовать начальный набор добавочных журналов).</span><span class="sxs-lookup"><span data-stu-id="96836-173">In Phase I, logs are required to bring a backed up database to consistency (or an initial set of incremental logs can be used).</span></span> <span data-ttu-id="96836-174">В фазе II для обеспечения соответствия базы данных используются все дополнительные журналы наката.</span><span class="sxs-lookup"><span data-stu-id="96836-174">In Phase II, any additional roll forward logs that are available are consumed to make the database consistent.</span></span> <span data-ttu-id="96836-175">Кроме того, существует также воспроизведение дополнительных журналов наката.</span><span class="sxs-lookup"><span data-stu-id="96836-175">There is also a replay of the additional roll forward logs.</span></span> <span data-ttu-id="96836-176">Этап III является стадией отката процесса восстановления.</span><span class="sxs-lookup"><span data-stu-id="96836-176">Phase III is the undo phase of recovery.</span></span>

<span data-ttu-id="96836-177">Этап I. Воспроизведение набора журналов, которые необходимо восстановить для базы данных, в целостное состояние (или начальный набор файлов журнала).</span><span class="sxs-lookup"><span data-stu-id="96836-177">Phase I: The replay of the set of logs that must be restored for the database to be brought to a consistent state (or an initial set of log files) is performed.</span></span> <span data-ttu-id="96836-178">По сути, это воспроизведение набора файлов журнала, которые не являются необязательными для восстанавливаемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="96836-178">Basically, this is the replay of the set of log files that are not optional for the databases being restored.</span></span> <span data-ttu-id="96836-179">Если журналы из этого диапазона журналов отсутствуют, восстановление завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="96836-179">If there are missing logs from this range of logs then the restore will fail.</span></span> <span data-ttu-id="96836-180">Эти журналы должны размещаться в каталоге, указанном в параметре *сзбаккуплогпас* .</span><span class="sxs-lookup"><span data-stu-id="96836-180">These logs should be put in the directory specified in the *szBackupLogPath* parameter.</span></span>

<span data-ttu-id="96836-181">Этап II. при необходимости могут существовать некоторые наборы файлов журналов, которые направляют файлы журналов, полученные из добавочных или разностных резервных копий, а также из файлов журнала активного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="96836-181">Phase II: Optionally, there may be some sets of log files that are roll forward log files that come from incremental or differential backups and from the log files of an active instance.</span></span> <span data-ttu-id="96836-182">В случае файлов журналов из добавочных или разностных резервных копий файлы журнала можно поместить в каталоги, указанные в параметрах *сзбаккуплогпас* или *сзтаржетинстанцелогпас* , где первым является рекомендуемый каталог.</span><span class="sxs-lookup"><span data-stu-id="96836-182">In the case of log files from incremental or differential backups, the log files can be placed in the directories specified in either the *szBackupLogPath* or the *szTargetInstanceLogPath* parameters, with the former being the recommended directory.</span></span> <span data-ttu-id="96836-183">Журналы, используемые для этапа наката (этап II), должны поступать из одной серии журналов, воспроизводимых на этапе I, и должны постоянно увеличивать номера журналов без промежутков с этапа, который я записывает.</span><span class="sxs-lookup"><span data-stu-id="96836-183">The logs used for the roll forward phase (phase II) should come from the same series of logs played during Phase I and should have continuously incrementing log numbers with no gaps from the Phase I logs.</span></span> <span data-ttu-id="96836-184">Чтобы обеспечить полную актуальность базы данных с файлами журнала, используемыми в настоящий момент активным экземпляром, необходимо указать параметры *сзтаржетинстанцелогпас* и *сзтаржетинстанцечеккпоинтпас* .</span><span class="sxs-lookup"><span data-stu-id="96836-184">To play a database to be fully up to date with the log files currently being used by an active instance, the *szTargetInstanceLogPath* and *szTargetInstanceCheckpointPath* parameters must be specified.</span></span> <span data-ttu-id="96836-185">Это можно сделать даже в том случае, если к этому набору журналов присоединены другие базы данных.</span><span class="sxs-lookup"><span data-stu-id="96836-185">This can be done even while other databases are attached to that log set.</span></span>

<span data-ttu-id="96836-186">Этап III. на последнем этапе восстановления выполняется откат всех незафиксированных транзакций, для чего требуется создание новых файлов журнала и обновление файла контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="96836-186">Phase III: In the final phase of recovery, any uncommitted transactions are rolled back, which requires generating new log files and updating the checkpoint file.</span></span> <span data-ttu-id="96836-187">Этот этап иногда называют "отменой".</span><span class="sxs-lookup"><span data-stu-id="96836-187">This phase is sometimes referred to as "undo".</span></span> <span data-ttu-id="96836-188">Путь к файлу контрольной точки, используемый на этом этапе, — это путь, аналогичный расположению журнала Phase III, то есть если *сзлогпас* используется для этапа III, будет использоваться *Сзчеккпоинтфилепас* , если *сзтаржетинстанцелогпас* используется для фазы III Recovery *сзтаржетинстанцечеккпоинтпас* .</span><span class="sxs-lookup"><span data-stu-id="96836-188">The checkpoint file path to use during this phase is the path analogous to the phase III log location, that is, if *szLogPath* is used for Phase III, *szCheckpointFilePath* will be used, if *szTargetInstanceLogPath* is used for phase III of recovery *szTargetInstanceCheckpointPath* will be used.</span></span>

<span data-ttu-id="96836-189">Чтобы понять, как работают пути, используйте следующую диаграмму потока:</span><span class="sxs-lookup"><span data-stu-id="96836-189">To understand how the paths work, use this flow chart:</span></span>

<span data-ttu-id="96836-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span><span class="sxs-lookup"><span data-stu-id="96836-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span></span>

#### <a name="requirements"></a><span data-ttu-id="96836-191">Требования</span><span class="sxs-lookup"><span data-stu-id="96836-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96836-192"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="96836-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="96836-193">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="96836-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96836-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="96836-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="96836-195">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="96836-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96836-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="96836-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="96836-197">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="96836-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96836-198"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="96836-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="96836-199">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="96836-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96836-200"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="96836-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="96836-201">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="96836-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96836-202"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="96836-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="96836-203">Реализуется как <strong>жетекстерналресторев</strong> (Юникод) и <strong>жетекстерналрестореа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="96836-203">Implemented as <strong>JetExternalRestoreW</strong> (Unicode) and <strong>JetExternalRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="96836-204">См. также:</span><span class="sxs-lookup"><span data-stu-id="96836-204">See Also</span></span>

[<span data-ttu-id="96836-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="96836-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="96836-206">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="96836-206">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="96836-207">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="96836-207">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="96836-208">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="96836-208">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="96836-209">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="96836-209">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="96836-210">жетинит</span><span class="sxs-lookup"><span data-stu-id="96836-210">JetInit</span></span>](./jetinit-function.md)
