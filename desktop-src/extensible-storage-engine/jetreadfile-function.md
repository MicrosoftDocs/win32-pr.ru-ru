---
description: Дополнительные сведения о функции Жетреадфиле
title: Функция Жетреадфиле
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265530"
---
# <a name="jetreadfile-function"></a><span data-ttu-id="1617d-103">Функция Жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="1617d-103">JetReadFile Function</span></span>


<span data-ttu-id="1617d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1617d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfile-function"></a><span data-ttu-id="1617d-105">Функция Жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="1617d-105">JetReadFile Function</span></span>

<span data-ttu-id="1617d-106">Функция **жетреадфиле** извлекает содержимое файла, открытого с помощью [жетопенфиле](./jetopenfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="1617d-106">The **JetReadFile** function retrieves the contents of a file opened with [JetOpenFile](./jetopenfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="1617d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1617d-107">Parameters</span></span>

<span data-ttu-id="1617d-108">*хффиле*</span><span class="sxs-lookup"><span data-stu-id="1617d-108">*hfFile*</span></span>

<span data-ttu-id="1617d-109">Описатель файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="1617d-109">The handle of the file to be read.</span></span>

<span data-ttu-id="1617d-110">*PV*</span><span class="sxs-lookup"><span data-stu-id="1617d-110">*pv*</span></span>

<span data-ttu-id="1617d-111">Выходной буфер, который будет принимать данные файла.</span><span class="sxs-lookup"><span data-stu-id="1617d-111">Output buffer that will receive the file data.</span></span>

<span data-ttu-id="1617d-112">*CB*</span><span class="sxs-lookup"><span data-stu-id="1617d-112">*cb*</span></span>

<span data-ttu-id="1617d-113">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="1617d-113">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="1617d-114">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="1617d-114">*pcbActual*</span></span>

<span data-ttu-id="1617d-115">Получает фактический объем извлекаемых файловых данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-115">Receives the actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="1617d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1617d-116">Return Value</span></span>

<span data-ttu-id="1617d-117">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="1617d-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1617d-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1617d-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1617d-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1617d-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="1617d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1617d-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1617d-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1617d-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1617d-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1617d-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1617d-123">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="1617d-123">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="1617d-124">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="1617d-124">The operation failed because the current external backup has been aborted by a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span> <span data-ttu-id="1617d-125">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="1617d-125">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1617d-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1617d-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1617d-127">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="1617d-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1617d-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1617d-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1617d-129">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="1617d-130">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="1617d-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1617d-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1617d-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1617d-132">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="1617d-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="1617d-133">Это может произойти для <strong>жетреадфиле</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="1617d-133">This can happen for <strong>JetReadFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="1617d-134">Указан недопустимый обработчик экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1617d-134">The specified instance handle is invalid.</span></span> <span data-ttu-id="1617d-135">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1617d-135">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="1617d-136">Размер выходного буфера не кратен размеру страницы базы данных (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="1617d-136">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="1617d-137">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1617d-137">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="1617d-138">Размер выходного буфера меньше трех страниц базы данных (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), и это первый вызов <strong>жетреадфиле</strong> для указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="1617d-138">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) and this is the first call to <strong>JetReadFile</strong> for the specified handle.</span></span> <span data-ttu-id="1617d-139">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1617d-139">Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1617d-140">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="1617d-140">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="1617d-141">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="1617d-141">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1617d-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1617d-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1617d-143">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="1617d-143">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1617d-144">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1617d-144">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="1617d-145">Не удалось выполнить операцию, так как при чтении страницы базы данных из файла базы данных или файла исправления базы данные обнаружено неустранимое повреждение данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-145">The operation failed because non-recoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1617d-146">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1617d-146">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="1617d-147">Не удалось выполнить операцию, поскольку при чтении файла журнала транзакций обнаружено неустранимое повреждение данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-147">The operation failed because non-recoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="1617d-148">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="1617d-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1617d-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1617d-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1617d-150">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="1617d-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1617d-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="1617d-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="1617d-152">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="1617d-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1617d-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1617d-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1617d-154">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="1617d-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1617d-155">При успешном выполнении следующий фрагмент данных из файла будет считан в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="1617d-155">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="1617d-156">Также будет возвращено фактическое число полученных байтов.</span><span class="sxs-lookup"><span data-stu-id="1617d-156">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="1617d-157">Смещение файла, на котором будет выполняться следующее считывание, будет расширено этим объемом.</span><span class="sxs-lookup"><span data-stu-id="1617d-157">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="1617d-158">В случае сбоя состояние выходного буфера не определено.</span><span class="sxs-lookup"><span data-stu-id="1617d-158">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="1617d-159">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1617d-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="1617d-160">В Windows XP и более поздних версиях резервная копия не будет отменена, если при чтении файла базы данных произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="1617d-160">On Windows XP and later releases, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="1617d-161">Однако резервная копия этого файла базы данных по-прежнему будет отменена, и соответствующий маркер будет автоматически закрыт.</span><span class="sxs-lookup"><span data-stu-id="1617d-161">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1617d-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1617d-162">Remarks</span></span>

<span data-ttu-id="1617d-163">Любой вызов **жетреадфиле** с помощью маркера, который уже вернул все данные в базовом файле (например, предыдущий вызов вернул меньше байт, чем размер выходного буфера), всегда будет успешно выполнен, но возвращать нулевые байты данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-163">Any call to **JetReadFile** using a handle that has already returned all the data in the underlying file (such as a previous call returned less bytes than the size of the output buffer) will always succeed but return zero bytes of data.</span></span>

<span data-ttu-id="1617d-164">Для повышения производительности резервного копирования следует использовать большой выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="1617d-164">A large output buffer should be used to maximize backup performance.</span></span> <span data-ttu-id="1617d-165">Для поиска правильного компромисса между потреблением ресурсов и пропускной способностью в данной ситуации может потребоваться некоторое экспериментирование.</span><span class="sxs-lookup"><span data-stu-id="1617d-165">Some experimentation may be required to find the right tradeoff between resource consumption and throughput for a given situation.</span></span> <span data-ttu-id="1617d-166">В любом случае выходной буфер должен иметь размер не меньше 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="1617d-166">The output buffer should be no smaller than 64KB in any case.</span></span>

<span data-ttu-id="1617d-167">Несколько одновременных вызовов **жетреадфиле** , использующих один и тот же файловый обработчик, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1617d-167">Multiple concurrent calls to **JetReadFile** using the same file handle are not supported.</span></span> <span data-ttu-id="1617d-168">Это означает, что невозможно поставить в очередь несколько буферов для чтения одновременно для одного и того же файла, чтобы добиться высокой последовательной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="1617d-168">This means that it is not possible to queue several buffers for read concurrently against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="1617d-169">Вместо этого следует использовать один большой буфер.</span><span class="sxs-lookup"><span data-stu-id="1617d-169">A single large buffer should be used instead.</span></span>

<span data-ttu-id="1617d-170">Если экземпляр настроен таким образом, что включена очистка страниц базы данных (см. раздел JET_paramZeroDatabaseDuringBackup в параметрах системы), удаленные данные будут удалены из базы данных как побочный результат вызова **жетреадфиле** по отношению к файлу базы данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-170">If the instance is configured such that database page scrubbing is enabled (see JET_paramZeroDatabaseDuringBackup in System Parameters) then deleted data will be removed from the database as a side effect of a call to **JetReadFile** against the database file.</span></span>

<span data-ttu-id="1617d-171">Очень важно понимать, как взаимодействуют резервные копии и повреждения данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-171">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="1617d-172">Если ядро СУБД обнаружит повреждение данных во время резервного копирования, то произойдет сбой резервного копирования затронутой базы данных или всего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1617d-172">If the database engine detects data corruption during a backup then it will either fail the backup of the affected database or of the entire instance.</span></span> <span data-ttu-id="1617d-173">Это осознанное решение по проектированию, предназначенное для защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-173">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="1617d-174">Если ядро СУБД допускало успешное резервное копирование при наличии повреждений данных, возможно, что в результате может быть отклонено старое, неповрежденное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="1617d-174">If the database engine allowed a backup to succeed where data corruption was present then it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="1617d-175">Это было бы неудачно, так как было бы возможным исправить повреждение данных на динамическом экземпляре, восстановив эту резервную копию и воспроизводящую все файлы журнала транзакций для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-175">This would be unfortunate because it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="1617d-176">В этом сценарии с нулевой потерей данных предполагается, что циклическое ведение журнала не включено (см. [JET_paramCircularLog](./transaction-log-parameters.md) в разделе [системные параметры](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="1617d-176">This zero data loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="1617d-177">Также важно понимать, что в случае повреждения данных потоковая резервная копия будет наиболее вероятным местом, что она сначала будет обнаружена.</span><span class="sxs-lookup"><span data-stu-id="1617d-177">It is also important to understand that when data corruption is present streaming backup will be the most likely place that it will first be detected.</span></span> <span data-ttu-id="1617d-178">Это происходит потому, что потоковая Архивация — единственный процесс, который обычно сканирует каждую отдельную страницу файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-178">This is the case because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="1617d-179">Также вполне вероятно, что потоковая Архивация будет первым процессом для обнаружения ранних нарушений аппаратного сбоя, как при нерегулярном повреждении данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-179">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors.</span></span> <span data-ttu-id="1617d-180">Это связано с объемом данных, получаемых резервной копией, а также скоростью их получения.</span><span class="sxs-lookup"><span data-stu-id="1617d-180">This is due to the amount of data retrieved by backup as well as the speed at which it is retrieved.</span></span>

<span data-ttu-id="1617d-181">Повреждение данных обнаруживается ядром СУБД с помощью блочных контрольных сумм.</span><span class="sxs-lookup"><span data-stu-id="1617d-181">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="1617d-182">Эти контрольные суммы задаются непосредственно перед записью страницы базы данных и проверяются на прочитанной странице базы данных.</span><span class="sxs-lookup"><span data-stu-id="1617d-182">These checksums are set just prior to a database page write and are verified on a database page read.</span></span> <span data-ttu-id="1617d-183">Эта схема позволяет ядру СУБД определить, что данные повреждены в некоторый момент, но не позволяют ядру СУБД определить источник этого повреждения.</span><span class="sxs-lookup"><span data-stu-id="1617d-183">This scheme enables the database engine to determine that data has been corrupted at some point but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="1617d-184">Исторически, основная причина такого повреждения была обнаружена из источников, отличных от самого ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="1617d-184">Historically, the predominant cause of such corruption has been found to come from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1617d-185">Требования</span><span class="sxs-lookup"><span data-stu-id="1617d-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1617d-186"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1617d-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1617d-187">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1617d-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1617d-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1617d-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1617d-189">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1617d-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1617d-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1617d-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1617d-191">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1617d-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1617d-192"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="1617d-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1617d-193">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1617d-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1617d-194"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="1617d-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1617d-195">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1617d-195">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1617d-196">См. также:</span><span class="sxs-lookup"><span data-stu-id="1617d-196">See Also</span></span>

[<span data-ttu-id="1617d-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1617d-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1617d-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="1617d-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="1617d-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1617d-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="1617d-200">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="1617d-200">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="1617d-201">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="1617d-201">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="1617d-202">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="1617d-202">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
