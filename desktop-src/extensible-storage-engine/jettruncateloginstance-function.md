---
description: Дополнительные сведения о функции Жеттрункателогинстанце
title: Функция Жеттрункателогинстанце
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711199"
---
# <a name="jettruncateloginstance-function"></a><span data-ttu-id="123d5-103">Функция Жеттрункателогинстанце</span><span class="sxs-lookup"><span data-stu-id="123d5-103">JetTruncateLogInstance Function</span></span>


<span data-ttu-id="123d5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="123d5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncateloginstance-function"></a><span data-ttu-id="123d5-105">Функция Жеттрункателогинстанце</span><span class="sxs-lookup"><span data-stu-id="123d5-105">JetTruncateLogInstance Function</span></span>

<span data-ttu-id="123d5-106">Функция **жеттрункателогинстанце** используется во время резервного копирования, инициированного [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) , чтобы удалить все файлы журнала транзакций, которые больше не понадобятся после успешного завершения текущей резервной копии.</span><span class="sxs-lookup"><span data-stu-id="123d5-106">The **JetTruncateLogInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="123d5-107">**Windows XP:**  **Жеттрункателогинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="123d5-107">**Windows XP:**  **JetTruncateLogInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="123d5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="123d5-108">Parameters</span></span>

<span data-ttu-id="123d5-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="123d5-109">*instance*</span></span>

<span data-ttu-id="123d5-110">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="123d5-110">The instance to use for this call.</span></span>

<span data-ttu-id="123d5-111">Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="123d5-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="123d5-112">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="123d5-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="123d5-113">Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="123d5-113">For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="123d5-114">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="123d5-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="123d5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="123d5-115">Return Value</span></span>

<span data-ttu-id="123d5-116">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="123d5-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="123d5-117">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="123d5-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="123d5-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="123d5-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="123d5-119">Описание</span><span class="sxs-lookup"><span data-stu-id="123d5-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="123d5-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="123d5-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="123d5-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="123d5-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="123d5-122">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="123d5-122">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="123d5-123"><strong>Windows Server 2003:</strong>  Это возвращаемое значение представлено в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="123d5-123"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="123d5-124">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="123d5-124">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="123d5-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="123d5-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="123d5-126">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="123d5-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="123d5-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="123d5-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="123d5-128">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="123d5-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="123d5-129">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="123d5-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="123d5-130">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="123d5-130">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="123d5-131">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="123d5-131">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="123d5-132"><a href="gg269263(v=exchg.10).md">Жеттрункателог</a> возвращает эту ошибку, если имеются необработанные дескрипторы файлов, созданные с помощью <a href="gg269249(v=exchg.10).md">жетопенфиле</a> для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="123d5-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="123d5-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="123d5-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="123d5-134">Один из указанных параметров содержал непредвиденное значение, или сочетание нескольких параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="123d5-134">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="123d5-135">Это может произойти для <a href="gg269263(v=exchg.10).md">жеттрункателог</a> , если указанный экземпляр является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="123d5-135">This can happen for <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="123d5-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="123d5-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="123d5-137">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="123d5-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="123d5-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="123d5-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="123d5-139">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="123d5-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="123d5-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="123d5-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="123d5-141">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="123d5-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="123d5-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="123d5-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="123d5-143">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="123d5-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="123d5-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="123d5-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="123d5-145">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="123d5-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="123d5-146">Если эта функция завершается успешно, набор файлов журнала транзакций, который больше не потребуется после успешного завершения текущего резервного копирования, удаляется.</span><span class="sxs-lookup"><span data-stu-id="123d5-146">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="123d5-147">Конечный автомат резервного копирования будет дополнительно таким, что резервная копия файлов базы данных больше не разрешается.</span><span class="sxs-lookup"><span data-stu-id="123d5-147">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="123d5-148">Только файлы исправления базы данных и файлы журнала транзакций могут быть открыты для резервного копирования за пределами этой точки.</span><span class="sxs-lookup"><span data-stu-id="123d5-148">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="123d5-149">Если эта функция завершается с ошибкой, резервный автомат может быть расширен таким, что резервная копия файлов базы данных больше не разрешается.</span><span class="sxs-lookup"><span data-stu-id="123d5-149">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="123d5-150">Может быть удалено некоторое количество файлов журнала транзакций, которое меньше требуемого числа, но они всегда будут удаляться от старых к самым старым.</span><span class="sxs-lookup"><span data-stu-id="123d5-150">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="123d5-151">Требования</span><span class="sxs-lookup"><span data-stu-id="123d5-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="123d5-152"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="123d5-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="123d5-153">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="123d5-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="123d5-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="123d5-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="123d5-155">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="123d5-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="123d5-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="123d5-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="123d5-157">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="123d5-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="123d5-158"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="123d5-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="123d5-159">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="123d5-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="123d5-160"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="123d5-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="123d5-161">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="123d5-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="123d5-162">См. также:</span><span class="sxs-lookup"><span data-stu-id="123d5-162">See Also</span></span>

[<span data-ttu-id="123d5-163">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="123d5-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="123d5-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="123d5-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="123d5-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="123d5-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="123d5-166">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="123d5-166">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="123d5-167">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="123d5-167">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="123d5-168">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="123d5-168">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="123d5-169">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="123d5-169">JetStopService</span></span>](./jetstopservice-function.md)
