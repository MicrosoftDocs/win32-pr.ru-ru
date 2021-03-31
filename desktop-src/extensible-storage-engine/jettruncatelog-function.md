---
description: Дополнительные сведения о функции Жеттрункателог
title: Функция Жеттрункателог
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e196a1570f769d8ae2619e962521bb181d506d63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809010"
---
# <a name="jettruncatelog-function"></a><span data-ttu-id="189b1-103">Функция Жеттрункателог</span><span class="sxs-lookup"><span data-stu-id="189b1-103">JetTruncateLog Function</span></span>


<span data-ttu-id="189b1-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="189b1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncatelog-function"></a><span data-ttu-id="189b1-105">Функция Жеттрункателог</span><span class="sxs-lookup"><span data-stu-id="189b1-105">JetTruncateLog Function</span></span>

<span data-ttu-id="189b1-106">Функция **жеттрункателог** используется во время резервного копирования, инициированного [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) , чтобы удалить все файлы журнала транзакций, которые больше не понадобятся после успешного завершения текущего резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="189b1-106">The **JetTruncateLog** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a><span data-ttu-id="189b1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="189b1-107">Parameters</span></span>

<span data-ttu-id="189b1-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="189b1-108">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="189b1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="189b1-109">Return Value</span></span>

<span data-ttu-id="189b1-110">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="189b1-110">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="189b1-111">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="189b1-111">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="189b1-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="189b1-112">Return code</span></span></p></th>
<th><p><span data-ttu-id="189b1-113">Описание</span><span class="sxs-lookup"><span data-stu-id="189b1-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="189b1-114">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="189b1-114">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="189b1-115">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="189b1-115">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="189b1-116">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="189b1-116">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="189b1-117">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="189b1-117">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="189b1-118"><strong>Windows Server 2003:</strong>  Это возвращаемое значение представлено в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="189b1-118"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="189b1-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="189b1-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="189b1-120">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="189b1-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="189b1-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="189b1-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="189b1-122">Операция не может быть завершена, поскольку в экземпляре, связанном с сеансом, произошла неустранимая ошибка, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="189b1-122">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="189b1-123"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="189b1-123"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="189b1-124">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="189b1-124">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="189b1-125">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="189b1-125">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="189b1-126"><strong>Жеттрункателог</strong> возвращает эту ошибку, если имеются необработанные дескрипторы файлов, созданные с помощью <a href="gg269249(v=exchg.10).md">жетопенфиле</a> для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="189b1-126"><strong>JetTruncateLog</strong> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="189b1-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="189b1-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="189b1-128">Один из указанных параметров содержал непредвиденное значение, или сочетание нескольких параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="189b1-128">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="189b1-129">Это может произойти для <strong>жеттрункателог</strong> , если указанный экземпляр является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="189b1-129">This can happen for <strong>JetTruncateLog</strong> when the specified instance handle is invalid.</span></span></p>
<p><span data-ttu-id="189b1-130"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="189b1-130"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="189b1-131">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="189b1-131">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="189b1-132">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="189b1-132">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="189b1-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="189b1-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="189b1-134">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="189b1-134">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="189b1-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="189b1-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="189b1-136">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="189b1-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="189b1-137">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="189b1-137">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="189b1-138">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, когда в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="189b1-138">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="189b1-139">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="189b1-139">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="189b1-140">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="189b1-140">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="189b1-141">Если эта функция завершается успешно, набор файлов журнала транзакций, который больше не потребуется после успешного завершения текущего резервного копирования, удаляется.</span><span class="sxs-lookup"><span data-stu-id="189b1-141">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="189b1-142">Конечный автомат резервного копирования будет дополнительно таким, что резервная копия файлов базы данных больше не разрешается.</span><span class="sxs-lookup"><span data-stu-id="189b1-142">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="189b1-143">Только файлы исправления базы данных и файлы журнала транзакций могут быть открыты для резервного копирования за пределами этой точки.</span><span class="sxs-lookup"><span data-stu-id="189b1-143">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="189b1-144">Если эта функция завершается с ошибкой, резервный автомат может быть расширен таким, что резервная копия файлов базы данных больше не разрешается.</span><span class="sxs-lookup"><span data-stu-id="189b1-144">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="189b1-145">Может быть удалено некоторое количество файлов журнала транзакций, которое меньше требуемого числа, но они всегда будут удаляться от старых к самым старым.</span><span class="sxs-lookup"><span data-stu-id="189b1-145">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="189b1-146">Требования</span><span class="sxs-lookup"><span data-stu-id="189b1-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="189b1-147"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="189b1-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="189b1-148">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="189b1-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="189b1-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="189b1-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="189b1-150">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="189b1-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="189b1-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="189b1-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="189b1-152">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="189b1-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="189b1-153"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="189b1-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="189b1-154">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="189b1-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="189b1-155"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="189b1-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="189b1-156">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="189b1-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="189b1-157">См. также:</span><span class="sxs-lookup"><span data-stu-id="189b1-157">See Also</span></span>

[<span data-ttu-id="189b1-158">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="189b1-158">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="189b1-159">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="189b1-159">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="189b1-160">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="189b1-160">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="189b1-161">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="189b1-161">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="189b1-162">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="189b1-162">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="189b1-163">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="189b1-163">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="189b1-164">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="189b1-164">JetStopService</span></span>](./jetstopservice-function.md)
