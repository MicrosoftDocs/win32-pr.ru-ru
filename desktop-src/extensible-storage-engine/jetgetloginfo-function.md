---
description: Дополнительные сведения о функции Жетжетлогинфо
title: Функция Жетжетлогинфо
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c96827be0ac62502e7545a9acb1fe157f3b28fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816337"
---
# <a name="jetgetloginfo-function"></a><span data-ttu-id="60840-103">Функция Жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="60840-103">JetGetLogInfo Function</span></span>


<span data-ttu-id="60840-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60840-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfo-function"></a><span data-ttu-id="60840-105">Функция Жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="60840-105">JetGetLogInfo Function</span></span>

<span data-ttu-id="60840-106">Функция **жетжетлогинфо** используется во время резервного копирования, инициированного [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) , для запроса экземпляра имен файлов исправления базы данных и файлов журнала транзакций, которые должны стать частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="60840-106">The **JetGetLogInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="60840-107">Эти файлы впоследствии можно открыть с помощью [жетопенфиле](./jetopenfile-function.md) и прочитать с помощью [жетреадфиле](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="60840-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="60840-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="60840-108">Parameters</span></span>

<span data-ttu-id="60840-109">*сзз*</span><span class="sxs-lookup"><span data-stu-id="60840-109">*szz*</span></span>

<span data-ttu-id="60840-110">Выходной буфер, который получит список строк, заканчивающихся нулем, описывающих набор файлов исправления базы данных и файлов журнала транзакций, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="60840-110">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="60840-111">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="60840-111">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="60840-112">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="60840-112">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="60840-113">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="60840-113">*cbMax*</span></span>

<span data-ttu-id="60840-114">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="60840-114">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="60840-115">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="60840-115">*pcbActual*</span></span>

<span data-ttu-id="60840-116">Получает фактический объем строковых данных, полученных в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="60840-116">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="60840-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60840-117">Return Value</span></span>

<span data-ttu-id="60840-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="60840-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="60840-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="60840-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60840-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="60840-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="60840-121">Описание</span><span class="sxs-lookup"><span data-stu-id="60840-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60840-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="60840-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="60840-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="60840-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60840-124">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="60840-124">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="60840-125">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="60840-125">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="60840-126">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="60840-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60840-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="60840-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="60840-128">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="60840-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60840-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="60840-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="60840-130">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="60840-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="60840-131">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="60840-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60840-132">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="60840-132">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="60840-133">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="60840-133">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="60840-134"><strong>Жетжетлогинфо</strong> возвращает эту ошибку, если в экземпляре имеются необработанные дескрипторы файлов, созданные с помощью <a href="gg269249(v=exchg.10).md">жетопенфиле</a> .</span><span class="sxs-lookup"><span data-stu-id="60840-134"><strong>JetGetLogInfo</strong> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60840-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="60840-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="60840-136">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="60840-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="60840-137">Это может произойти для <strong>жетжетлогинфо</strong> , если указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="60840-137">This can happen for <strong>JetGetLogInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60840-138">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="60840-138">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="60840-139">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="60840-139">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60840-140">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="60840-140">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="60840-141">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="60840-141">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60840-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="60840-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="60840-143">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="60840-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60840-144">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="60840-144">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="60840-145">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="60840-145">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60840-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="60840-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="60840-147">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="60840-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60840-148">При успешном выполнении запрошенные сведения о наборе файлов исправления базы данных и журналов транзакций, которые должны быть частью набора файлов резервной копии, помещаются в выходные буферы там, где они предоставлены.</span><span class="sxs-lookup"><span data-stu-id="60840-148">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="60840-149">Конечный автомат резервного копирования будет дополнительно таким, что резервная копия файлов базы данных больше не разрешается.</span><span class="sxs-lookup"><span data-stu-id="60840-149">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="60840-150">Только файлы исправления базы данных и файлы журнала транзакций могут быть открыты для резервного копирования за пределами этой точки.</span><span class="sxs-lookup"><span data-stu-id="60840-150">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="60840-151">В случае сбоя состояние выходных буферов не определено.</span><span class="sxs-lookup"><span data-stu-id="60840-151">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="60840-152">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="60840-152">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="60840-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60840-153">Remarks</span></span>

<span data-ttu-id="60840-154">Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="60840-154">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="60840-155">Приложение всегда должно предоставлять буфер для получения фактического размера этого списка и использовать эти сведения для определения усечения списка.</span><span class="sxs-lookup"><span data-stu-id="60840-155">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="60840-156">Требования</span><span class="sxs-lookup"><span data-stu-id="60840-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60840-157"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="60840-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="60840-158">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="60840-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60840-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="60840-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="60840-160">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="60840-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60840-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="60840-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="60840-162">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="60840-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60840-163"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="60840-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="60840-164">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="60840-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60840-165"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="60840-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="60840-166">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="60840-166">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60840-167"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="60840-167"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="60840-168">Реализуется как <strong>жетжетлогинфов</strong> (Юникод) и <strong>жетжетлогинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="60840-168">Implemented as <strong>JetGetLogInfoW</strong> (Unicode) and <strong>JetGetLogInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="60840-169">См. также:</span><span class="sxs-lookup"><span data-stu-id="60840-169">See Also</span></span>

[<span data-ttu-id="60840-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="60840-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="60840-171">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="60840-171">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="60840-172">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="60840-172">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="60840-173">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="60840-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="60840-174">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="60840-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="60840-175">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="60840-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="60840-176">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="60840-176">JetStopBackup</span></span>](./jetstopbackup-function.md)
