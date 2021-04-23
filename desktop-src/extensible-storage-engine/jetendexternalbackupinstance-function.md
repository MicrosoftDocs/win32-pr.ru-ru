---
description: Дополнительные сведения о функции Жетендекстерналбаккупинстанце
title: Функция Жетендекстерналбаккупинстанце
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081182"
---
# <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="70daf-103">Функция Жетендекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="70daf-103">JetEndExternalBackupInstance Function</span></span>


<span data-ttu-id="70daf-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="70daf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="70daf-105">Функция Жетендекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="70daf-105">JetEndExternalBackupInstance Function</span></span>

<span data-ttu-id="70daf-106">Функция **жетендекстерналбаккупинстанце** завершает внешний сеанс резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="70daf-106">The **JetEndExternalBackupInstance** function ends an external backup session.</span></span> <span data-ttu-id="70daf-107">Этот API является последним в серии API-интерфейсов, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).</span><span class="sxs-lookup"><span data-stu-id="70daf-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="70daf-108">**Windows XP: жетендекстерналбаккупинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70daf-108">**Windows XP:  JetEndExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="70daf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="70daf-109">Parameters</span></span>

<span data-ttu-id="70daf-110">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="70daf-110">*instance*</span></span>

<span data-ttu-id="70daf-111">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="70daf-111">The instance to use for this call.</span></span>

<span data-ttu-id="70daf-112">**Windows 2000:** Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="70daf-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="70daf-113">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="70daf-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="70daf-114">**Windows XP:** Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="70daf-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="70daf-115">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="70daf-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="70daf-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70daf-116">Return Value</span></span>

<span data-ttu-id="70daf-117">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="70daf-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="70daf-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="70daf-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70daf-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="70daf-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="70daf-120">Описание</span><span class="sxs-lookup"><span data-stu-id="70daf-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70daf-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="70daf-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="70daf-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="70daf-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70daf-123">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="70daf-123">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="70daf-124"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70daf-124"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="70daf-125">Вызывающий объект прервал резервную копию в середине последовательности резервного копирования, не указывая намерения <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="70daf-125">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="70daf-126">Эта ошибка возникает в результате ошибки в клиенте резервного копирования в Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="70daf-126">This error is the result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="70daf-127">В Windows XP эта ошибка возвращается для преднамеренного завершения внешней последовательности резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="70daf-127">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70daf-128">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="70daf-128">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="70daf-129"><strong>Windows Server 2003:  </strong> Это возвращаемое значение представлено в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70daf-129"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="70daf-130">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="70daf-130">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70daf-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="70daf-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="70daf-132">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="70daf-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70daf-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="70daf-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="70daf-134"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70daf-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="70daf-135">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="70daf-135">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70daf-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="70daf-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="70daf-137">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="70daf-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70daf-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="70daf-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="70daf-139">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="70daf-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70daf-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="70daf-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="70daf-141">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="70daf-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70daf-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="70daf-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="70daf-143">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, когда в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="70daf-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70daf-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="70daf-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="70daf-145">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="70daf-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70daf-146">Если функция завершается успешно, Внешняя резервная копия была успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="70daf-146">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="70daf-147">Успешное завершение означает, что все файлы (например, базы данных и журналы), подходящие для типа резервной копии (указанной в [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)), были получены из модуля резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="70daf-147">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="70daf-148">Резервные копии файлов можно восстановить с помощью жесткого восстановления ([жетекстерналресторе](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="70daf-148">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="70daf-149">В случае сбоя этой функции внешнее резервное копирование обычно завершается.</span><span class="sxs-lookup"><span data-stu-id="70daf-149">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="70daf-150">Сбой означает, что резервная копия является недопустимой из-за ошибки использования клиента или приложения.</span><span class="sxs-lookup"><span data-stu-id="70daf-150">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="70daf-151">Важно проверить код возврата для этого API, чтобы убедиться, что последовательность резервного копирования прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="70daf-151">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="70daf-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70daf-152">Remarks</span></span>

<span data-ttu-id="70daf-153">Если для модуля настроено ведение журнала событий, в журнал заносится событие, указывающее на разрешение внешней резервной копии.</span><span class="sxs-lookup"><span data-stu-id="70daf-153">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="70daf-154">Если последовательность резервного копирования не завершена по порядку и при успешном вызове [жетендекстерналбаккуп](./jetendexternalbackup-function.md), последующие добавочные резервные копии могут содержать больше данных, чем ожидалось приложением.</span><span class="sxs-lookup"><span data-stu-id="70daf-154">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="70daf-155">Дополнительные сведения о последовательности API внешней резервной копии см. в разделе [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="70daf-155">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="70daf-156">До Windows Vista, если усечение журнала не выполнялось, подсистема считалась резервной копией копии.</span><span class="sxs-lookup"><span data-stu-id="70daf-156">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="70daf-157">Однако резервное копирование может быть обычной резервной копией, для которой не выполнялось усечение (например, при наличии отсоединенных баз данных).</span><span class="sxs-lookup"><span data-stu-id="70daf-157">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="70daf-158">Параметр JET_bitBackupTruncateDone можно использовать для информирования ядра об этом и предоставления правильных изменений заголовка базы данных.</span><span class="sxs-lookup"><span data-stu-id="70daf-158">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow proper database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="70daf-159">Требования</span><span class="sxs-lookup"><span data-stu-id="70daf-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70daf-160"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="70daf-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="70daf-161">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70daf-161">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70daf-162"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="70daf-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="70daf-163">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70daf-163">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70daf-164"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="70daf-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="70daf-165">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="70daf-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70daf-166"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="70daf-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="70daf-167">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="70daf-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70daf-168"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="70daf-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="70daf-169">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="70daf-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="70daf-170">См. также:</span><span class="sxs-lookup"><span data-stu-id="70daf-170">See Also</span></span>

[<span data-ttu-id="70daf-171">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="70daf-171">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="70daf-172">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="70daf-172">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="70daf-173">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="70daf-173">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="70daf-174">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="70daf-174">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="70daf-175">жетбегинекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="70daf-175">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="70daf-176">жетклосефиле</span><span class="sxs-lookup"><span data-stu-id="70daf-176">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="70daf-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="70daf-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="70daf-178">жетекстерналресторе</span><span class="sxs-lookup"><span data-stu-id="70daf-178">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="70daf-179">жетжетаттачинфо</span><span class="sxs-lookup"><span data-stu-id="70daf-179">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="70daf-180">жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="70daf-180">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="70daf-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="70daf-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="70daf-182">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="70daf-182">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="70daf-183">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="70daf-183">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="70daf-184">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="70daf-184">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="70daf-185">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="70daf-185">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="70daf-186">жеттрункателог</span><span class="sxs-lookup"><span data-stu-id="70daf-186">JetTruncateLog</span></span>](./jettruncatelog-function.md)
