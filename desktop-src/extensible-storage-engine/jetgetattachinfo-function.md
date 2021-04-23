---
description: Дополнительные сведения о функции Жетжетаттачинфо
title: Функция JetGetAttachInfo
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa1e51931c11e0fce0b18c0c102c4d54c0b47976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647635"
---
# <a name="jetgetattachinfo-function"></a><span data-ttu-id="ce662-103">Функция JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="ce662-103">JetGetAttachInfo Function</span></span>


<span data-ttu-id="ce662-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ce662-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfo-function"></a><span data-ttu-id="ce662-105">Функция JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="ce662-105">JetGetAttachInfo Function</span></span>

<span data-ttu-id="ce662-106">Функция **жетжетаттачинфо** используется во время резервного копирования, инициированного [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) , чтобы запросить экземпляр для имен файлов базы данных, которые должны стать частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ce662-106">The **JetGetAttachInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="ce662-107">Будут рассматриваться только те базы данных, которые в данный момент подключены к экземпляру с помощью [жетаттачдатабасе](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ce662-107">Only databases currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="ce662-108">Эти файлы впоследствии можно открыть с помощью [жетопенфиле](./jetopenfile-function.md) и прочитать с помощью [жетреадфиле](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="ce662-108">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="ce662-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce662-109">Parameters</span></span>

<span data-ttu-id="ce662-110">*сзз*</span><span class="sxs-lookup"><span data-stu-id="ce662-110">*szz*</span></span>

<span data-ttu-id="ce662-111">Выходной буфер, который получает список строк, заканчивающихся нулем, описывающих набор файлов базы данных, который должен быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ce662-111">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="ce662-112">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="ce662-112">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="ce662-113">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="ce662-113">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="ce662-114">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="ce662-114">*cbMax*</span></span>

<span data-ttu-id="ce662-115">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="ce662-115">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="ce662-116">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="ce662-116">*pcbActual*</span></span>

<span data-ttu-id="ce662-117">Указатель на выходной буфер, который получил фактический объем строковых данных.</span><span class="sxs-lookup"><span data-stu-id="ce662-117">Pointer to the output buffer that received the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="ce662-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce662-118">Return Value</span></span>

<span data-ttu-id="ce662-119">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="ce662-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ce662-120">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ce662-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce662-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ce662-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="ce662-122">Описание</span><span class="sxs-lookup"><span data-stu-id="ce662-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce662-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ce662-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ce662-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ce662-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce662-125">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="ce662-125">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="ce662-126">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="ce662-126">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="ce662-127">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="ce662-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce662-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ce662-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ce662-129">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="ce662-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce662-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ce662-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ce662-131">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="ce662-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ce662-132">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="ce662-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce662-133">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="ce662-133">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="ce662-134">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="ce662-134">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="ce662-135"><strong>Жетжетаттачинфо</strong> возвращает эту ошибку, если текущая резервная копия не является полной резервной копией.</span><span class="sxs-lookup"><span data-stu-id="ce662-135"><strong>JetGetAttachInfo</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce662-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ce662-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ce662-137">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="ce662-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="ce662-138">Это может произойти для <strong>жетжетаттачинфо</strong> , если указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="ce662-138">This can happen for <strong>JetGetAttachInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce662-139">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="ce662-139">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="ce662-140">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="ce662-140">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce662-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ce662-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ce662-142">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="ce662-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce662-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ce662-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ce662-144">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="ce662-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce662-145">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="ce662-145">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="ce662-146">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="ce662-146">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce662-147">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ce662-147">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ce662-148">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="ce662-148">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ce662-149">При успешном выполнении запрошенные сведения о наборе файлов базы данных, которые должны быть частью набора файлов резервной копии, будут помещены в выходные буферы там, где они предоставлены.</span><span class="sxs-lookup"><span data-stu-id="ce662-149">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="ce662-150">В случае сбоя состояние выходных буферов не определено.</span><span class="sxs-lookup"><span data-stu-id="ce662-150">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="ce662-151">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ce662-151">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ce662-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce662-152">Remarks</span></span>

<span data-ttu-id="ce662-153">Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ce662-153">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="ce662-154">Приложение всегда должно предоставлять буфер для получения фактического размера этого списка и использовать эти сведения для определения усечения списка.</span><span class="sxs-lookup"><span data-stu-id="ce662-154">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ce662-155">Требования</span><span class="sxs-lookup"><span data-stu-id="ce662-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce662-156"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="ce662-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ce662-157">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ce662-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce662-158"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ce662-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ce662-159">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ce662-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce662-160"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ce662-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ce662-161">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ce662-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce662-162"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="ce662-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ce662-163">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ce662-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce662-164"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="ce662-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ce662-165">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ce662-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce662-166"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="ce662-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ce662-167">Реализуется как <strong>жетжетаттачинфов</strong> (Юникод) и <strong>жетжетаттачинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ce662-167">Implemented as <strong>JetGetAttachInfoW</strong> (Unicode) and <strong>JetGetAttachInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ce662-168">См. также:</span><span class="sxs-lookup"><span data-stu-id="ce662-168">See Also</span></span>

[<span data-ttu-id="ce662-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ce662-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ce662-170">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ce662-170">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ce662-171">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="ce662-171">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="ce662-172">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="ce662-172">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="ce662-173">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="ce662-173">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="ce662-174">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="ce662-174">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="ce662-175">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="ce662-175">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="ce662-176">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="ce662-176">JetStopService</span></span>](./jetstopservice-function.md)
