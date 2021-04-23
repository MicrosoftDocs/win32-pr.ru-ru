---
description: Дополнительные сведения о функции Жетбаккуп
title: Функция JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713075"
---
# <a name="jetbackup-function"></a><span data-ttu-id="7e8f4-103">Функция JetBackup</span><span class="sxs-lookup"><span data-stu-id="7e8f4-103">JetBackup Function</span></span>


<span data-ttu-id="7e8f4-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7e8f4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackup-function"></a><span data-ttu-id="7e8f4-105">Функция JetBackup</span><span class="sxs-lookup"><span data-stu-id="7e8f4-105">JetBackup Function</span></span>

<span data-ttu-id="7e8f4-106">Функция **жетбаккуп** создает резервную копию базы данных, пока база данных находится в режиме «в сети».</span><span class="sxs-lookup"><span data-stu-id="7e8f4-106">The **JetBackup** function creates a backup of the database while the database is online.</span></span> <span data-ttu-id="7e8f4-107">Эта функция предназначена в первую очередь для обеспечения обратной совместимости с Windows 2000 и более ранними ядрами СУБД, в которых разрешен только один экземпляр базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="7e8f4-108">В этом случае активный экземпляр — это экземпляр, для которого создается резервная копия.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-108">In this case, the active instance is the instance that is backed up.</span></span>

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="7e8f4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e8f4-109">Parameters</span></span>

<span data-ttu-id="7e8f4-110">*сзбаккуппас*</span><span class="sxs-lookup"><span data-stu-id="7e8f4-110">*szBackupPath*</span></span>

<span data-ttu-id="7e8f4-111">Каталог, в котором хранится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-111">The directory where the backup is stored.</span></span> <span data-ttu-id="7e8f4-112">Если путь резервного копирования равен NULL, функция усекает журналы, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-112">If the backup path is NULL, the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="7e8f4-113">*грбит*</span><span class="sxs-lookup"><span data-stu-id="7e8f4-113">*grbit*</span></span>

<span data-ttu-id="7e8f4-114">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-114">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e8f4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7e8f4-115">Value</span></span></p></th>
<th><p><span data-ttu-id="7e8f4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7e8f4-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-117">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="7e8f4-117">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-118">Создает полную резервную копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-118">Creates a full backup of the database.</span></span> <span data-ttu-id="7e8f4-119">Это позволяет сохранять существующую резервную копию в том же каталоге в случае сбоя новой резервной копии.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-120">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="7e8f4-120">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-121">Создает добавочное резервное копирование, а не полное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-121">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="7e8f4-122">Это означает, что резервное копирование выполняется только для файлов журнала с момента последнего полного или добавочного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-122">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e8f4-123">*пфнстатус*</span><span class="sxs-lookup"><span data-stu-id="7e8f4-123">*pfnStatus*</span></span>

<span data-ttu-id="7e8f4-124">Указатель на функцию обратного вызова [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , которая предоставляет сведения о ходе выполнения операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-124">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="7e8f4-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e8f4-125">Return Value</span></span>

<span data-ttu-id="7e8f4-126">Функция возвращает один из [JET_ERR](./jet-err.md) кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-126">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="7e8f4-127">Чаще всего возвращаются следующие.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-127">The following are the most commonly returned.</span></span> <span data-ttu-id="7e8f4-128">(Полный список ошибок для этого API см. в разделе [расширенные коды ошибок подсистемы хранилища](./extensible-storage-engine-error-codes.md).)</span><span class="sxs-lookup"><span data-stu-id="7e8f4-128">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e8f4-129">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7e8f4-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="7e8f4-130">Описание</span><span class="sxs-lookup"><span data-stu-id="7e8f4-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7e8f4-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-132">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-133">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="7e8f4-133">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-134">Для того же экземпляра уже выполняется резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-134">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="7e8f4-135">Одновременно не разрешено несколько резервных копий.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-135">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-136">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="7e8f4-136">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-137">Экземпляр еще не готов для резервного копирования при инициализации.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-137">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-138">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7e8f4-138">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-139">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-139">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7e8f4-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-141">Операция не может быть завершена, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-141">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7e8f4-142"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-142"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-143">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="7e8f4-143">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-144">Добавочное резервное копирование не разрешено, если включено циклическое ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-144">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-145">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="7e8f4-145">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-146">Указаны недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-146">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-147">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7e8f4-147">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-148">В API передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-148">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-149">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="7e8f4-149">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-150">Конечный путь не существует.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-150">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-151">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="7e8f4-151">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-152">Экземпляр работает без ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-152">The instance is running without logging.</span></span> <span data-ttu-id="7e8f4-153">Резервное копирование запрещено.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-153">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-154">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="7e8f4-154">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-155">Ошибка проверки контрольной суммы файла журнала.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-155">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-156">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="7e8f4-156">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-157">Ведение журнала для экземпляра является временным или постоянно отключено из-за непредвиденной ошибки.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-157">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7e8f4-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-159">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-159">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-160">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="7e8f4-160">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-161">Ошибка проверки контрольной суммы на странице базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-161">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7e8f4-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-163">Операция не может быть завершена, так как выполняется операция восстановления для экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7e8f4-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-165">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="7e8f4-166"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-166"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7e8f4-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7e8f4-168">Операция не может быть завершена, так как экземпляр, связанный с сеансом, завершает работу.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-168">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e8f4-169">Если функция выполнена, все файлы, необходимые для восстановления до момента резервного копирования, будут находиться в каталоге резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-169">If the function succeeds, all the files needed for a restore up to the moment of the backup will be contained in the backup directory.</span></span> <span data-ttu-id="7e8f4-170">Если это полная резервная копия, то файлы будут файлами базы данных и журналами, необходимыми для перевода базы данных в целостное состояние.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-170">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="7e8f4-171">Если это добавочное резервное копирование, в каталоги будут добавляться только файлы журналов, но уже существующие файлы (базы данных и файлы журналов) вместе с новыми файлами журналов будут восстановлены, чтобы вернуть базу данных в состояние, в котором она находилась в момент начала резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-171">If this is an incremental backup, only log files will be added to the directories, but the already existing files (databases and log files), together with the new log files, will be able to be restored to bring the database back to the state it was in at the moment that the backup began.</span></span>

<span data-ttu-id="7e8f4-172">В качестве побочного результата резервного копирования файлы журнала, которые больше не нужны, будут обрезаны.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-172">As a side effect of the backup, the log files which are no longer needed will be truncated.</span></span>

<span data-ttu-id="7e8f4-173">В то же время заголовки базы данных будут обновлены с учетом информации, которая была выполнена при последней архивации.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-173">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="7e8f4-174">В случае сбоя функции в месте назначения каталога резервного копирования не будет файлов, поэтому восстановление будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-174">If the function fails, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="7e8f4-175">В то же время текущие файлы журнала не будут обрезаны.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-175">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7e8f4-176">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e8f4-176">Remarks</span></span>

<span data-ttu-id="7e8f4-177">На различных шагах резервного копирования будут созданы записи журнала событий, включая имена файлов, усечение журнала и окончательный результат резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-177">The different steps of the backup will have Event Log entries generated, including the file names, the log truncation, and the final result of the backup.</span></span>

<span data-ttu-id="7e8f4-178">Добавочное резервное копирование возможно только после создания полной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-178">Incremental backups are possible only after a full backup was taken.</span></span> <span data-ttu-id="7e8f4-179">Кроме того, добавочное резервное копирование возможно только в том случае, если циклическое ведение журнала отключено.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-179">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="7e8f4-180">Рекомендуется, чтобы каталог резервного копирования не содержал никаких файлов, кроме тех, которые использовались в резервной копии или были добавлены при предыдущей успешной архивации.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-180">It is recommended that the backup directory should not contain any files other than the one used in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="7e8f4-181">Каталог резервного копирования должен существовать, если для экземпляра не задан параметр *JET_paramCreatePathIfNotExist* .</span><span class="sxs-lookup"><span data-stu-id="7e8f4-181">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="7e8f4-182">Дополнительные сведения см. в разделе [системные параметры](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7e8f4-182">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="7e8f4-183">Резервная копия выполнит проверку контрольной суммы на всех используемых страницах базы данных и начиная с Windows Server 2003, а также с файлами журналов.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-183">The backup will do a checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="7e8f4-184">Это дает возможность оценить работоспособность базы данных даже для страниц, которые не считываются во время нормальной работы.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-184">This gives an opportunity to estimate the health of the database, even for pages which are not read during normal operations.</span></span> <span data-ttu-id="7e8f4-185">Если такое повреждение будет обнаружено, произойдет сбой резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-185">If any such corruption is encountered, the backup will fail.</span></span>

<span data-ttu-id="7e8f4-186">Во время резервного копирования текущий файл журнала будет завершен, и будет создан новый журнал.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-186">During the backup, the current log file will be finished and a new log will be generated.</span></span> <span data-ttu-id="7e8f4-187">Таким образом, все необходимые файлы журнала могут быть скопированы, так как текущий журнал больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-187">This way, all of the necessary log files can be copies, because the current log will not be in use anymore.</span></span>

<span data-ttu-id="7e8f4-188">Настоятельно рекомендуется не использовать резервную копию ни для каких целей, кроме резервного копирования и восстановления на уровне ядра.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-188">It is strongly recommended that the backup not be used for any purpose other than the backup and restore at the engine level.</span></span> <span data-ttu-id="7e8f4-189">Это снизит вероятность получения ошибок во время операций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-189">This will minimize the chance of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7e8f4-190">Требования</span><span class="sxs-lookup"><span data-stu-id="7e8f4-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-191"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f4-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f4-192">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-193"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f4-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f4-194">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-195"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f4-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f4-196">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-197"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f4-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f4-198">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f4-199"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f4-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f4-200">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7e8f4-200">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f4-201"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f4-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f4-202">Реализуется как <strong>жетбаккупв</strong> (Юникод) и <strong>жетбаккупа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7e8f4-202">Implemented as <strong>JetBackupW</strong> (Unicode) and <strong>JetBackupA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7e8f4-203">См. также:</span><span class="sxs-lookup"><span data-stu-id="7e8f4-203">See Also</span></span>

[<span data-ttu-id="7e8f4-204">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="7e8f4-204">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="7e8f4-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7e8f4-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7e8f4-206">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7e8f4-206">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7e8f4-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7e8f4-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7e8f4-208">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="7e8f4-208">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="7e8f4-209">жетресторе</span><span class="sxs-lookup"><span data-stu-id="7e8f4-209">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="7e8f4-210">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="7e8f4-210">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="7e8f4-211">жетрестореинстанце</span><span class="sxs-lookup"><span data-stu-id="7e8f4-211">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="7e8f4-212">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="7e8f4-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="7e8f4-213">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="7e8f4-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
