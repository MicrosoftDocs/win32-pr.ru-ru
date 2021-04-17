---
description: Дополнительные сведения о функции Жетендекстерналбаккуп
title: Функция JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703341"
---
# <a name="jetendexternalbackup-function"></a><span data-ttu-id="6738d-103">Функция JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="6738d-103">JetEndExternalBackup Function</span></span>


<span data-ttu-id="6738d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6738d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackup-function"></a><span data-ttu-id="6738d-105">Функция JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="6738d-105">JetEndExternalBackup Function</span></span>

<span data-ttu-id="6738d-106">Функция **жетендекстерналбаккуп** завершает внешний сеанс резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6738d-106">The **JetEndExternalBackup** function ends an external backup session.</span></span> <span data-ttu-id="6738d-107">Эта функция является последним элементом API в серии элементов API, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).</span><span class="sxs-lookup"><span data-stu-id="6738d-107">This function is the last API element in a series of API elements that must be called to execute a successful online (non-VSS based) backup.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="6738d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6738d-108">Parameters</span></span>

<span data-ttu-id="6738d-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="6738d-109">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="6738d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6738d-110">Return Value</span></span>

<span data-ttu-id="6738d-111">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="6738d-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6738d-112">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6738d-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6738d-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6738d-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="6738d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6738d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6738d-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6738d-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6738d-116">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6738d-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6738d-117">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6738d-117">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6738d-118">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="6738d-118">The operation cannot complete because the instance that is associated with the session has not been yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6738d-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6738d-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6738d-120">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="6738d-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6738d-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6738d-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6738d-122"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP</span><span class="sxs-lookup"><span data-stu-id="6738d-122"><strong>Windows XP:  </strong>This return value is introduced in Windows XP</span></span></p>
<p><span data-ttu-id="6738d-123">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, для которой необходимо отозвать доступ ко всем данным, чтобы защитить целостность этих данных.</span><span class="sxs-lookup"><span data-stu-id="6738d-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6738d-124">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6738d-124">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6738d-125">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="6738d-125">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6738d-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6738d-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6738d-127">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="6738d-127">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6738d-128">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="6738d-128">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="6738d-129">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="6738d-129">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6738d-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="6738d-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="6738d-131"><strong>Windows Server 2003:  </strong> Это возвращаемое значение представлено в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6738d-131"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="6738d-132">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="6738d-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6738d-133">еррбаккупабортбикаллер</span><span class="sxs-lookup"><span data-stu-id="6738d-133">errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="6738d-134"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6738d-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="6738d-135">Вызывающий объект прервал резервную копию в середине последовательности резервного копирования, не указывая намерения <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="6738d-135">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="6738d-136">Эта ошибка возникает в результате ошибки в клиенте резервного копирования в Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="6738d-136">This error is a result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="6738d-137">В Windows XP эта ошибка возвращается для преднамеренного завершения внешней последовательности резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6738d-137">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6738d-138">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="6738d-138">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="6738d-139">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, когда в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="6738d-139">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6738d-140">Если эта функция завершается успешно, Внешняя резервная копия была успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="6738d-140">If this function succeeds, the external backup was a success.</span></span> <span data-ttu-id="6738d-141">Успешное завершение означает, что все файлы (например, базы данных и журналы), подходящие для типа резервной копии (указанной в [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)), были получены из модуля резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6738d-141">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="6738d-142">Резервные копии файлов можно восстановить с помощью жесткого восстановления ([жетекстерналресторе](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="6738d-142">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="6738d-143">В случае сбоя этой функции внешнее резервное копирование обычно завершается.</span><span class="sxs-lookup"><span data-stu-id="6738d-143">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="6738d-144">Сбой означает, что резервная копия является недопустимой из-за ошибки использования клиента или приложения.</span><span class="sxs-lookup"><span data-stu-id="6738d-144">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="6738d-145">Важно проверить код возврата для этого API, чтобы убедиться, что последовательность резервного копирования прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="6738d-145">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6738d-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6738d-146">Remarks</span></span>

<span data-ttu-id="6738d-147">Если для модуля настроено ведение журнала событий, в журнал заносится событие, указывающее на разрешение внешней резервной копии.</span><span class="sxs-lookup"><span data-stu-id="6738d-147">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="6738d-148">Если последовательность резервного копирования не завершена по порядку и при успешном вызове **жетендекстерналбаккуп**, последующие добавочные резервные копии могут содержать больше данных, чем ожидалось приложением.</span><span class="sxs-lookup"><span data-stu-id="6738d-148">If the backup sequence is not completed in order and with a successful call to **JetEndExternalBackup**, subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="6738d-149">Дополнительные сведения о последовательности API внешней резервной копии см. в разделе [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="6738d-149">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="6738d-150">До Windows Vista, если усечение журнала не выполнялось, подсистема считалась резервной копией копии.</span><span class="sxs-lookup"><span data-stu-id="6738d-150">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="6738d-151">Однако резервное копирование может быть обычной резервной копией, для которой не выполнялось усечение (например, при наличии отсоединенных баз данных).</span><span class="sxs-lookup"><span data-stu-id="6738d-151">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="6738d-152">Параметр JET_bitBackupTruncateDone можно использовать для информирования ядра об этом и предоставления соответствующих изменений заголовка базы данных.</span><span class="sxs-lookup"><span data-stu-id="6738d-152">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6738d-153">Требования</span><span class="sxs-lookup"><span data-stu-id="6738d-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6738d-154"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="6738d-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6738d-155">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6738d-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6738d-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6738d-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6738d-157">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6738d-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6738d-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6738d-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6738d-159">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6738d-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6738d-160"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="6738d-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6738d-161">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6738d-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6738d-162"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="6738d-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6738d-163">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6738d-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6738d-164">См. также:</span><span class="sxs-lookup"><span data-stu-id="6738d-164">See Also</span></span>

[<span data-ttu-id="6738d-165">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="6738d-165">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="6738d-166">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="6738d-166">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="6738d-167">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="6738d-167">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="6738d-168">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="6738d-168">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="6738d-169">жетклосефиле</span><span class="sxs-lookup"><span data-stu-id="6738d-169">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="6738d-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6738d-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6738d-171">жетекстерналресторе</span><span class="sxs-lookup"><span data-stu-id="6738d-171">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="6738d-172">жетжетаттачинфо</span><span class="sxs-lookup"><span data-stu-id="6738d-172">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="6738d-173">жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="6738d-173">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="6738d-174">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="6738d-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="6738d-175">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="6738d-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="6738d-176">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="6738d-176">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="6738d-177">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="6738d-177">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="6738d-178">жеттрункателог</span><span class="sxs-lookup"><span data-stu-id="6738d-178">JetTruncateLog</span></span>](./jettruncatelog-function.md)
