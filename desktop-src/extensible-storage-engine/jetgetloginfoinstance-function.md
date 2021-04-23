---
description: Дополнительные сведения о функции Жетжетлогинфоинстанце
title: Функция Жетжетлогинфоинстанце
TOCTitle: JetGetLogInfoInstance Function
ms:assetid: 505500b1-2827-43f1-a0fe-5e84e00b0260
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269246(v=EXCHG.10)
ms:contentKeyID: 32765548
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance
- JetGetLogInfoInstanceW
- JetGetLogInfoInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2056859bdce13dfdc28d4cbbf8716925d5bc1cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703093"
---
# <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="836e5-103">Функция Жетжетлогинфоинстанце</span><span class="sxs-lookup"><span data-stu-id="836e5-103">JetGetLogInfoInstance Function</span></span>


<span data-ttu-id="836e5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="836e5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="836e5-105">Функция Жетжетлогинфоинстанце</span><span class="sxs-lookup"><span data-stu-id="836e5-105">JetGetLogInfoInstance Function</span></span>

<span data-ttu-id="836e5-106">Функция **жетжетлогинфоинстанце** используется во время резервного копирования, инициированного [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) , для запроса экземпляра имен файлов исправления базы данных и файлов журнала транзакций, которые должны стать частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="836e5-106">The **JetGetLogInfoInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="836e5-107">Эти файлы впоследствии можно открыть с помощью [жетопенфиле](./jetopenfile-function.md) и прочитать с помощью [жетреадфиле](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="836e5-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="836e5-108">**Windows XP: жетжетлогинфоинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="836e5-108">**Windows XP:  JetGetLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="836e5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="836e5-109">Parameters</span></span>

<span data-ttu-id="836e5-110">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="836e5-110">*instance*</span></span>

<span data-ttu-id="836e5-111">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="836e5-111">The instance to use for this call.</span></span>

<span data-ttu-id="836e5-112">Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="836e5-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="836e5-113">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="836e5-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="836e5-114">Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="836e5-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="836e5-115">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="836e5-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="836e5-116">*сзз*</span><span class="sxs-lookup"><span data-stu-id="836e5-116">*szz*</span></span>

<span data-ttu-id="836e5-117">Выходной буфер, который получит список строк, заканчивающихся нулем, описывающих набор файлов исправления базы данных и файлов журнала транзакций, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="836e5-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="836e5-118">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="836e5-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="836e5-119">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="836e5-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="836e5-120">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="836e5-120">*cbMax*</span></span>

<span data-ttu-id="836e5-121">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="836e5-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="836e5-122">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="836e5-122">*pcbActual*</span></span>

<span data-ttu-id="836e5-123">Получает фактический объем строковых данных, полученных в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="836e5-123">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="836e5-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="836e5-124">Return Value</span></span>

<span data-ttu-id="836e5-125">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="836e5-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="836e5-126">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="836e5-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="836e5-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="836e5-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="836e5-128">Описание</span><span class="sxs-lookup"><span data-stu-id="836e5-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="836e5-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="836e5-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="836e5-130">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="836e5-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="836e5-131">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="836e5-131">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="836e5-132">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="836e5-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="836e5-133">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="836e5-133">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="836e5-134">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="836e5-134">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="836e5-135">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="836e5-135">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="836e5-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="836e5-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="836e5-137">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="836e5-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="836e5-138">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="836e5-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="836e5-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="836e5-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="836e5-140">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="836e5-140">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="836e5-141"><a href="gg294055(v=exchg.10).md">Жетжетлогинфо</a> возвращает эту ошибку, если в экземпляре имеются необработанные дескрипторы файлов, созданные с помощью <a href="gg269249(v=exchg.10).md">жетопенфиле</a> .</span><span class="sxs-lookup"><span data-stu-id="836e5-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="836e5-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="836e5-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="836e5-143">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="836e5-143">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="836e5-144">Это может произойти для <a href="gg294055(v=exchg.10).md">жетжетлогинфо</a> , если указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="836e5-144">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="836e5-145">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="836e5-145">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="836e5-146">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="836e5-146">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="836e5-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="836e5-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="836e5-148">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="836e5-148">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="836e5-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="836e5-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="836e5-150">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="836e5-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="836e5-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="836e5-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="836e5-152">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="836e5-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="836e5-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="836e5-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="836e5-154">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="836e5-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="836e5-155">При успешном выполнении запрошенные сведения о наборе файлов исправления базы данных и журналов транзакций, которые должны быть частью набора файлов резервной копии, помещаются в выходные буферы там, где они предоставлены.</span><span class="sxs-lookup"><span data-stu-id="836e5-155">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="836e5-156">Конечный автомат резервного копирования будет дополнительно таким, что резервная копия файлов базы данных больше не разрешается.</span><span class="sxs-lookup"><span data-stu-id="836e5-156">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="836e5-157">Только файлы исправления базы данных и файлы журнала транзакций могут быть открыты для резервного копирования за пределами этой точки.</span><span class="sxs-lookup"><span data-stu-id="836e5-157">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="836e5-158">В случае сбоя состояние выходных буферов не определено.</span><span class="sxs-lookup"><span data-stu-id="836e5-158">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="836e5-159">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="836e5-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="836e5-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="836e5-160">Remarks</span></span>

<span data-ttu-id="836e5-161">Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="836e5-161">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="836e5-162">Приложение всегда должно предоставлять буфер для получения фактического размера этого списка и использовать эти сведения для определения усечения списка.</span><span class="sxs-lookup"><span data-stu-id="836e5-162">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="836e5-163">Требования</span><span class="sxs-lookup"><span data-stu-id="836e5-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="836e5-164"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="836e5-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="836e5-165">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="836e5-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="836e5-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="836e5-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="836e5-167">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="836e5-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="836e5-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="836e5-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="836e5-169">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="836e5-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="836e5-170"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="836e5-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="836e5-171">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="836e5-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="836e5-172"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="836e5-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="836e5-173">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="836e5-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="836e5-174"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="836e5-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="836e5-175">Реализуется как <strong>жетжетлогинфоинстанцев</strong> (Юникод) и <strong>жетжетлогинфоинстанцеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="836e5-175">Implemented as <strong>JetGetLogInfoInstanceW</strong> (Unicode) and <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="836e5-176">См. также:</span><span class="sxs-lookup"><span data-stu-id="836e5-176">See Also</span></span>

[<span data-ttu-id="836e5-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="836e5-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="836e5-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="836e5-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="836e5-179">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="836e5-179">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="836e5-180">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="836e5-180">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="836e5-181">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="836e5-181">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="836e5-182">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="836e5-182">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="836e5-183">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="836e5-183">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="836e5-184">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="836e5-184">JetStopService</span></span>](./jetstopservice-function.md)
