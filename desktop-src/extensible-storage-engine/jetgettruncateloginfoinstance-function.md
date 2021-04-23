---
description: Дополнительные сведения о функции Жетжеттрункателогинфоинстанце
title: Функция Жетжеттрункателогинфоинстанце
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703092"
---
# <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="f698c-103">Функция Жетжеттрункателогинфоинстанце</span><span class="sxs-lookup"><span data-stu-id="f698c-103">JetGetTruncateLogInfoInstance Function</span></span>


<span data-ttu-id="f698c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f698c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="f698c-105">Функция Жетжеттрункателогинфоинстанце</span><span class="sxs-lookup"><span data-stu-id="f698c-105">JetGetTruncateLogInfoInstance Function</span></span>

<span data-ttu-id="f698c-106">Функция **жетжеттрункателогинфоинстанце** используется во время резервного копирования, которое инициируется [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) для запроса экземпляров имен файлов журнала транзакций, которые можно безопасно удалить после успешного завершения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f698c-106">The **JetGetTruncateLogInfoInstance** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="f698c-107">**Windows XP:**  **Жетжеттрункателогинфоинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f698c-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="f698c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f698c-108">Parameters</span></span>

<span data-ttu-id="f698c-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="f698c-109">*instance*</span></span>

<span data-ttu-id="f698c-110">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f698c-110">The instance to use for this call.</span></span>

<span data-ttu-id="f698c-111">*сзз*</span><span class="sxs-lookup"><span data-stu-id="f698c-111">*szz*</span></span>

<span data-ttu-id="f698c-112">Выходной буфер, который получает список строк, заканчивающихся нулем, описывающих набор файлов журнала транзакций, которые можно безопасно удалить после успешного завершения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f698c-112">The output buffer that receives the list of null-terminated strings describing the set of transaction log files that can be safely deleted after the backup has been completed successfully.</span></span>

<span data-ttu-id="f698c-113">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="f698c-113">The list of strings that are returned in this buffer is in the same format as a multi-string that is used by the registry.</span></span> <span data-ttu-id="f698c-114">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="f698c-114">Each null-terminated string is returned in sequence and followed by a final null terminator.</span></span>

<span data-ttu-id="f698c-115">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="f698c-115">*cbMax*</span></span>

<span data-ttu-id="f698c-116">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="f698c-116">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="f698c-117">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="f698c-117">*pcbActual*</span></span>

<span data-ttu-id="f698c-118">Указатель на выходной буфер, который получает фактический объем строковых данных.</span><span class="sxs-lookup"><span data-stu-id="f698c-118">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="f698c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f698c-119">Return Value</span></span>

<span data-ttu-id="f698c-120">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="f698c-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f698c-121">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f698c-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f698c-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f698c-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="f698c-123">Описание</span><span class="sxs-lookup"><span data-stu-id="f698c-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f698c-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f698c-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f698c-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f698c-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f698c-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f698c-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f698c-127">Один из указанных параметров содержал непредвиденное значение или сочетание нескольких значений параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="f698c-127">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="f698c-128"><strong>Windows XP и более поздние версии:</strong>  Это может произойти для <strong>жетжеттрункателогинфоинстанце</strong> , если указанный экземпляр является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="f698c-128"><strong>Windows XP and later:</strong>  This can happen for <strong>JetGetTruncateLogInfoInstance</strong> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f698c-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f698c-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f698c-130">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="f698c-130">The operation cannot complete because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f698c-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f698c-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f698c-132">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="f698c-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f698c-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f698c-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f698c-134">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="f698c-134">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="f698c-135"><strong>Windows XP:</strong>  Это возвращаемое значение было введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f698c-135"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f698c-136">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="f698c-136">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="f698c-137">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="f698c-137">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="f698c-138"><strong>Windows XP:</strong>  Это возвращаемое значение было введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f698c-138"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f698c-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="f698c-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="f698c-140">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="f698c-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f698c-141">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="f698c-141">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="f698c-142">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="f698c-142">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f698c-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f698c-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f698c-144">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="f698c-144">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f698c-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f698c-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f698c-146">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="f698c-146">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f698c-147"><strong>жетжеттрункателогинфоинстанце</strong></span><span class="sxs-lookup"><span data-stu-id="f698c-147"><strong>JetGetTruncateLogInfoInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="f698c-148">Существуют необработанные дескрипторы файлов, созданные с помощью <a href="gg269249(v=exchg.10).md">жетопенфиле</a> для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f698c-148">There are outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f698c-149">Если эта функция завершается успешно, запрашиваемые сведения о наборе файлов журнала транзакций, которые можно безопасно удалить после успешного завершения резервного копирования, помещаются в выходные буферы, где они указаны.</span><span class="sxs-lookup"><span data-stu-id="f698c-149">If this function succeeds, the requested information about the set of transaction log files that can be safely deleted after the backup has been completed successfully will be placed in the output buffers where they are provided.</span></span> <span data-ttu-id="f698c-150">Конечный автомат резервного копирования будет дополнительно таким, что резервная копия файлов базы данных больше не разрешается.</span><span class="sxs-lookup"><span data-stu-id="f698c-150">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="f698c-151">Только файлы исправления базы данных и файлы журнала транзакций могут быть открыты для резервного копирования за этот момент.</span><span class="sxs-lookup"><span data-stu-id="f698c-151">Only database patch files and transaction log files can be opened for backup beyond this point.</span></span>

<span data-ttu-id="f698c-152">Если эта функция завершается ошибкой, состояние буферов вывода не определено.</span><span class="sxs-lookup"><span data-stu-id="f698c-152">If this function fails, the state of the output buffers is undefined.</span></span> <span data-ttu-id="f698c-153">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f698c-153">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f698c-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f698c-154">Remarks</span></span>

<span data-ttu-id="f698c-155">Этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f698c-155">This API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="f698c-156">Приложение всегда должно предоставлять буфер для получения фактического размера этого списка и использовать эти сведения для определения усечения списка.</span><span class="sxs-lookup"><span data-stu-id="f698c-156">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f698c-157">Требования</span><span class="sxs-lookup"><span data-stu-id="f698c-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f698c-158"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f698c-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f698c-159">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f698c-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f698c-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f698c-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f698c-161">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f698c-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f698c-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f698c-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f698c-163">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f698c-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f698c-164"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="f698c-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f698c-165">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f698c-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f698c-166"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="f698c-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f698c-167">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f698c-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f698c-168"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="f698c-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f698c-169">Реализуется как <strong>жетжеттрункателогинфоинстанцев</strong> (Юникод) и <strong>жетжеттрункателогинфоинстанцеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f698c-169">Implemented as <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) and <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f698c-170">См. также:</span><span class="sxs-lookup"><span data-stu-id="f698c-170">See Also</span></span>

[<span data-ttu-id="f698c-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f698c-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f698c-172">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f698c-172">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f698c-173">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="f698c-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="f698c-174">жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="f698c-174">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="f698c-175">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="f698c-175">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="f698c-176">жетендсессион</span><span class="sxs-lookup"><span data-stu-id="f698c-176">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="f698c-177">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="f698c-177">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="f698c-178">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="f698c-178">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="f698c-179">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="f698c-179">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="f698c-180">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="f698c-180">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="f698c-181">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="f698c-181">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="f698c-182">жеттерм</span><span class="sxs-lookup"><span data-stu-id="f698c-182">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="f698c-183">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="f698c-183">JetTerm2</span></span>](./jetterm2-function.md)
