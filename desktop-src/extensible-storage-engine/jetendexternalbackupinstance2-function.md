---
description: Дополнительные сведения о функции JetEndExternalBackupInstance2
title: Функция JetEndExternalBackupInstance2
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e719885cc61ff3f3193046b632e9969b8d660f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702617"
---
# <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="bf269-103">Функция JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="bf269-103">JetEndExternalBackupInstance2 Function</span></span>


<span data-ttu-id="bf269-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bf269-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="bf269-105">Функция JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="bf269-105">JetEndExternalBackupInstance2 Function</span></span>

<span data-ttu-id="bf269-106">Функция **JetEndExternalBackupInstance2** завершает внешний сеанс резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bf269-106">The **JetEndExternalBackupInstance2** function ends an external backup session.</span></span> <span data-ttu-id="bf269-107">Этот API является последним в серии API-интерфейсов, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).</span><span class="sxs-lookup"><span data-stu-id="bf269-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="bf269-108">**Windows XP: JetEndExternalBackupInstance2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf269-108">**Windows XP:  JetEndExternalBackupInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="bf269-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf269-109">Parameters</span></span>

<span data-ttu-id="bf269-110">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="bf269-110">*instance*</span></span>

<span data-ttu-id="bf269-111">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="bf269-111">The instance to use for this call.</span></span>

<span data-ttu-id="bf269-112">**Windows 2000:** Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="bf269-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="bf269-113">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bf269-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="bf269-114">**Windows XP:** Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="bf269-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="bf269-115">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="bf269-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="bf269-116">*грбит*</span><span class="sxs-lookup"><span data-stu-id="bf269-116">*grbit*</span></span>

<span data-ttu-id="bf269-117">Группа битов, которая задает ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="bf269-117">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf269-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bf269-118">Value</span></span></p></th>
<th><p><span data-ttu-id="bf269-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bf269-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf269-120">JET_bitBackupEndAbort</span><span class="sxs-lookup"><span data-stu-id="bf269-120">JET_bitBackupEndAbort</span></span><br />
<span data-ttu-id="bf269-121">0x0002</span><span class="sxs-lookup"><span data-stu-id="bf269-121">0x0002</span></span></p></td>
<td><p><span data-ttu-id="bf269-122">Клиентское приложение прерывает резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="bf269-122">The client application is aborting the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf269-123">JET_bitBackupEndNormal</span><span class="sxs-lookup"><span data-stu-id="bf269-123">JET_bitBackupEndNormal</span></span><br />
<span data-ttu-id="bf269-124">0x0001</span><span class="sxs-lookup"><span data-stu-id="bf269-124">0x0001</span></span></p></td>
<td><p><span data-ttu-id="bf269-125">Клиентское приложение полностью завершило резервное копирование и завершается нормально.</span><span class="sxs-lookup"><span data-stu-id="bf269-125">The client application finished the backup completely, and is ending normally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf269-126">JET_bitBackupTruncateDone</span><span class="sxs-lookup"><span data-stu-id="bf269-126">JET_bitBackupTruncateDone</span></span><br />
<span data-ttu-id="bf269-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="bf269-127">0x0100</span></span></p></td>
<td><p><span data-ttu-id="bf269-128"><strong>Windows Vista:  </strong> JET_bitBackupTruncateDone введен в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bf269-128"><strong>Windows Vista:  </strong>JET_bitBackupTruncateDone is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="bf269-129">Подсистема может пометить заголовки базы данных соответствующим образом (например, завершить полное резервное копирование), даже если вызов truncate не был завершен.</span><span class="sxs-lookup"><span data-stu-id="bf269-129">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="bf269-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf269-130">Return Value</span></span>

<span data-ttu-id="bf269-131">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="bf269-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bf269-132">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bf269-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf269-133">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bf269-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="bf269-134">Описание</span><span class="sxs-lookup"><span data-stu-id="bf269-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf269-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bf269-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bf269-136">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bf269-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf269-137">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="bf269-137">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="bf269-138"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf269-138"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="bf269-139">Вызывающий объект прервал резервную копию в середине последовательности резервного копирования, не указывая намерения <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="bf269-139">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="bf269-140">Эта ошибка возникает в результате ошибки в клиенте резервного копирования в Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="bf269-140">This error is result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="bf269-141">В Windows XP эта ошибка возвращается для преднамеренного завершения внешней последовательности резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bf269-141">In Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf269-142">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="bf269-142">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="bf269-143"><strong>Windows Server 2003:  </strong> Это возвращаемое значение представлено в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bf269-143"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="bf269-144">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="bf269-144">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf269-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bf269-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bf269-146">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="bf269-146">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf269-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bf269-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bf269-148"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf269-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="bf269-149">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="bf269-149">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf269-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="bf269-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="bf269-151">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="bf269-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf269-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bf269-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bf269-153">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="bf269-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf269-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bf269-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bf269-155">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="bf269-155">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf269-156">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="bf269-156">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="bf269-157">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, когда в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="bf269-157">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf269-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bf269-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bf269-159">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="bf269-159">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf269-160">Если функция завершается успешно, Внешняя резервная копия была успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="bf269-160">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="bf269-161">Успешное завершение означает, что все файлы (например, базы данных и журналы), подходящие для типа резервной копии (указанной в [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)), были получены из модуля резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bf269-161">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="bf269-162">Резервные копии файлов можно восстановить с помощью жесткого восстановления ([жетекстерналресторе](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="bf269-162">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="bf269-163">В случае сбоя этой функции внешнее резервное копирование обычно завершается.</span><span class="sxs-lookup"><span data-stu-id="bf269-163">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="bf269-164">Сбой означает, что резервная копия является недопустимой из-за ошибки использования клиента или приложения.</span><span class="sxs-lookup"><span data-stu-id="bf269-164">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="bf269-165">Важно проверить код возврата для этого API, чтобы убедиться, что последовательность резервного копирования прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="bf269-165">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bf269-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf269-166">Remarks</span></span>

<span data-ttu-id="bf269-167">Если для модуля настроено ведение журнала событий, в журнал заносится событие, указывающее на разрешение внешней резервной копии.</span><span class="sxs-lookup"><span data-stu-id="bf269-167">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="bf269-168">Если последовательность резервного копирования не завершена по порядку и при успешном вызове [жетендекстерналбаккуп](./jetendexternalbackup-function.md), последующие добавочные резервные копии могут содержать больше данных, чем ожидалось приложением.</span><span class="sxs-lookup"><span data-stu-id="bf269-168">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="bf269-169">Дополнительные сведения о последовательности API внешней резервной копии см. в разделе [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf269-169">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="bf269-170">До Windows Vista, если усечение журнала не выполнялось, подсистема считалась резервной копией копии.</span><span class="sxs-lookup"><span data-stu-id="bf269-170">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="bf269-171">Однако резервное копирование может быть обычной резервной копией, для которой не выполнялось усечение (например, при наличии отсоединенных баз данных).</span><span class="sxs-lookup"><span data-stu-id="bf269-171">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="bf269-172">Параметр JET_bitBackupTruncateDone можно использовать для информирования ядра об этом и предоставления соответствующих изменений заголовка базы данных.</span><span class="sxs-lookup"><span data-stu-id="bf269-172">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bf269-173">Требования</span><span class="sxs-lookup"><span data-stu-id="bf269-173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf269-174"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="bf269-174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bf269-175">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf269-175">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf269-176"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bf269-176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bf269-177">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bf269-177">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf269-178"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bf269-178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bf269-179">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bf269-179">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf269-180"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="bf269-180"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bf269-181">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bf269-181">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf269-182"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="bf269-182"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bf269-183">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bf269-183">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bf269-184">См. также:</span><span class="sxs-lookup"><span data-stu-id="bf269-184">See Also</span></span>

[<span data-ttu-id="bf269-185">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="bf269-185">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="bf269-186">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="bf269-186">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="bf269-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bf269-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bf269-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bf269-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bf269-189">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="bf269-189">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="bf269-190">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="bf269-190">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="bf269-191">жетбегинекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="bf269-191">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="bf269-192">жетклосефиле</span><span class="sxs-lookup"><span data-stu-id="bf269-192">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="bf269-193">жетекстерналресторе</span><span class="sxs-lookup"><span data-stu-id="bf269-193">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="bf269-194">жетжетаттачинфо</span><span class="sxs-lookup"><span data-stu-id="bf269-194">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="bf269-195">жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="bf269-195">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="bf269-196">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bf269-196">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="bf269-197">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="bf269-197">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="bf269-198">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="bf269-198">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="bf269-199">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="bf269-199">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="bf269-200">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="bf269-200">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="bf269-201">жеттрункателог</span><span class="sxs-lookup"><span data-stu-id="bf269-201">JetTruncateLog</span></span>](./jettruncatelog-function.md)
