---
description: Дополнительные сведения о функции Жетбаккупинстанце
title: Функция JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143540"
---
# <a name="jetbackupinstance-function"></a><span data-ttu-id="eb0f4-103">Функция JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="eb0f4-103">JetBackupInstance Function</span></span>


<span data-ttu-id="eb0f4-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="eb0f4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackupinstance-function"></a><span data-ttu-id="eb0f4-105">Функция JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="eb0f4-105">JetBackupInstance Function</span></span>

<span data-ttu-id="eb0f4-106">Функция **жетбаккупинстанце** выполняет потоковую архивацию экземпляра, включая все подключенные базы данных, в каталог.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-106">The **JetBackupInstance** function performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="eb0f4-107">При наличии нескольких методов резервного копирования, поддерживаемых ядром, это самая простая и наиболее Инкапсулированная функция.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-107">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="eb0f4-108">**Windows XP: жетбаккупинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-108">**Windows XP:  JetBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="eb0f4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb0f4-109">Parameters</span></span>

<span data-ttu-id="eb0f4-110">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="eb0f4-110">*instance*</span></span>

<span data-ttu-id="eb0f4-111">Экземпляр базы данных для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-111">The instance of the database to backup.</span></span>

<span data-ttu-id="eb0f4-112">*сзбаккуппас*</span><span class="sxs-lookup"><span data-stu-id="eb0f4-112">*szBackupPath*</span></span>

<span data-ttu-id="eb0f4-113">Каталог, в котором хранится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-113">The directory where the backup is stored.</span></span> <span data-ttu-id="eb0f4-114">Если путь резервного копирования имеет значение NULL для использования функции, по возможности будет усекать журналы.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-114">If the backup path is NULL to use the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="eb0f4-115">*грбит*</span><span class="sxs-lookup"><span data-stu-id="eb0f4-115">*grbit*</span></span>

<span data-ttu-id="eb0f4-116">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb0f4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eb0f4-117">Value</span></span></p></th>
<th><p><span data-ttu-id="eb0f4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="eb0f4-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="eb0f4-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-120">Создает полную резервную копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-120">Creates a full backup of the database.</span></span> <span data-ttu-id="eb0f4-121">Это позволяет сохранять существующую резервную копию в том же каталоге в случае сбоя новой резервной копии.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-121">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="eb0f4-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-123">Создает добавочное резервное копирование, а не полное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="eb0f4-124">Это означает, что резервное копирование выполняется только для файлов журнала, созданных с момента последнего полного или добавочного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-124">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="eb0f4-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-126">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-126">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb0f4-127">*пфнстатус*</span><span class="sxs-lookup"><span data-stu-id="eb0f4-127">*pfnStatus*</span></span>

<span data-ttu-id="eb0f4-128">Указатель на функцию обратного вызова [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , которая предоставляет сведения о ходе выполнения операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-128">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="eb0f4-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb0f4-129">Return Value</span></span>

<span data-ttu-id="eb0f4-130">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="eb0f4-131">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eb0f4-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb0f4-132">Код возврата</span><span class="sxs-lookup"><span data-stu-id="eb0f4-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="eb0f4-133">Описание</span><span class="sxs-lookup"><span data-stu-id="eb0f4-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="eb0f4-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-135">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-136">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="eb0f4-136">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-137">Для того же экземпляра уже выполняется резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-137">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="eb0f4-138">Одновременно не разрешено несколько резервных копий.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-138">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-139">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="eb0f4-139">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-140">Экземпляр еще не готов для резервного копирования при инициализации.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-140">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="eb0f4-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-142">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg294108(v=exchg.10).md">жетстопсервицеинстанце</a>.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-142">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="eb0f4-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-144">Операция не может быть завершена, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-144">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="eb0f4-145"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-145"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-146">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="eb0f4-146">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-147">Добавочное резервное копирование не разрешено, если включено циклическое ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-147">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-148">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="eb0f4-148">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-149">Указаны недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-149">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="eb0f4-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-151">В API передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-151">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="eb0f4-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-153">Конечный путь не существует.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-153">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-154">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="eb0f4-154">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-155">Экземпляр работает без ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-155">The instance is running without logging.</span></span> <span data-ttu-id="eb0f4-156">Резервное копирование запрещено.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-156">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-157">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="eb0f4-157">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-158">Ошибка проверки контрольной суммы файла журнала.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-158">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-159">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="eb0f4-159">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-160">Ведение журнала для экземпляра является временным или постоянно отключено из-за непредвиденной ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-160">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-161">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="eb0f4-161">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-162">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-162">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-163">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="eb0f4-163">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-164">Ошибка проверки контрольной суммы на странице базы данных.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-164">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="eb0f4-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-166">Операция не может быть завершена, так как выполняется операция восстановления для экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-166">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="eb0f4-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-168">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-168">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="eb0f4-169"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-169"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="eb0f4-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="eb0f4-171">Операция не может быть завершена, так как экземпляр, связанный с сеансом, завершает работу.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-171">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb0f4-172">После того как функция вернет значение Success, в каталоге Backup будут присутствовать все файлы, необходимые для восстановления до момента создания резервной копии.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-172">After the function returns success, in the backup directory all the files needed for a restore up to the moment of the backup will be present.</span></span> <span data-ttu-id="eb0f4-173">Если это полная резервная копия, то файлы будут файлами базы данных и журналами, необходимыми для перевода базы данных в целостное состояние.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-173">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="eb0f4-174">Если это добавочное резервное копирование, в каталоги будут добавлены только файлы журналов, но уже существующие файлы (базы данных и файлы журнала) вместе с новыми файлами журнала будут восстановлены и возвращены в состояние базы данных в момент создания резервной копии.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-174">If this is an incremental backup, only log files will be added to the directories but the already existing files (databases and log files) together with the new log files will be able to be restored and bring the database back to the state at the moment of the backup.</span></span>

<span data-ttu-id="eb0f4-175">В качестве побочного результата резервного копирования файлы журнала, которые больше не нужны, будут обрезаны.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-175">As a side effect of the backup, the log files which are not longer needed will be truncated.</span></span>

<span data-ttu-id="eb0f4-176">В то же время заголовки базы данных будут обновлены с учетом информации, которая была выполнена при последней архивации.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-176">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="eb0f4-177">В случае сбоя в месте назначения каталога резервного копирования не будет файлов, поэтому восстановление будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-177">On failure, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="eb0f4-178">В то же время текущие файлы журнала не будут обрезаны.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-178">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="eb0f4-179">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb0f4-179">Remarks</span></span>

<span data-ttu-id="eb0f4-180">На различных шагах резервного копирования будут созданы записи журнала событий, включая имена файлов, усечение журнала и конечный результат резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-180">The different steps of the backup will have Event Log entries generated including the file names, the log truncation and the final result of the backup.</span></span>

<span data-ttu-id="eb0f4-181">Добавочное резервное копирование возможно только после создания полной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-181">Incremental backup are possible only after a full backup was taken.</span></span> <span data-ttu-id="eb0f4-182">Кроме того, добавочное резервное копирование возможно только в том случае, если циклическое ведение журнала отключено.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-182">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="eb0f4-183">Рекомендуется, чтобы каталог резервного копирования не содержал другие файлы, а затем один из них, участвующий в резервной копии или добавленный предыдущей успешной архивацией.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-183">It is recommended that the backup directory should not contain other files then the one involved in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="eb0f4-184">Каталог резервного копирования должен существовать, если для экземпляра не задан параметр *JET_paramCreatePathIfNotExist* .</span><span class="sxs-lookup"><span data-stu-id="eb0f4-184">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="eb0f4-185">Дополнительные сведения см. в разделе [системные параметры](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eb0f4-185">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="eb0f4-186">Резервная копия выполнит проверку контрольной суммы на всех используемых страницах базы данных и начиная с Windows Server 2003, а также с файлами журналов.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-186">The backup will do checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="eb0f4-187">Это дает возможность оценить работоспособность базы данных даже для страниц, которые не считываются во время нормальной работы.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-187">This gives an opportunity to estimate the health of the database even for pages which are not read during normal operations.</span></span> <span data-ttu-id="eb0f4-188">Если такое повреждение будет обнаружено, произойдет сбой резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-188">If any such corruption will be encountered, the backup will fail.</span></span>

<span data-ttu-id="eb0f4-189">Во время резервного копирования текущий файл журнала будет завершен, и будет запущено новое поколение журнала.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-189">During the backup, the current log file will be finished and we will start a new log generation.</span></span> <span data-ttu-id="eb0f4-190">Это позволит копировать необходимые файлы журналов, так как последний из них больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-190">This will allow copying the needed log files because the last needed one will not be in use anymore.</span></span>

<span data-ttu-id="eb0f4-191">Настоятельно рекомендуется не использовать резервную копию для других целей, а затем резервное копирование и восстановление на уровне ядра.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-191">It is strongly recommended that the backup should not be used for other purposed other then the backup and restored at the engine level.</span></span> <span data-ttu-id="eb0f4-192">Это снизит изменение при получении ошибок во время операций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-192">This will minimize the change of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="eb0f4-193">Требования</span><span class="sxs-lookup"><span data-stu-id="eb0f4-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-194"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="eb0f4-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eb0f4-195">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="eb0f4-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eb0f4-197">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="eb0f4-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eb0f4-199">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-200"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="eb0f4-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="eb0f4-201">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb0f4-202"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="eb0f4-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="eb0f4-203">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="eb0f4-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb0f4-204"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="eb0f4-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="eb0f4-205">Реализуется как <strong>жетбаккупинстанцев</strong> (Юникод) и <strong>жетбаккупинстанцеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="eb0f4-205">Implemented as <strong>JetBackupInstanceW</strong> (Unicode) and <strong>JetBackupInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="eb0f4-206">См. также:</span><span class="sxs-lookup"><span data-stu-id="eb0f4-206">See Also</span></span>

[<span data-ttu-id="eb0f4-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="eb0f4-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="eb0f4-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="eb0f4-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="eb0f4-209">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="eb0f4-209">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="eb0f4-210">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="eb0f4-210">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="eb0f4-211">жетресторе</span><span class="sxs-lookup"><span data-stu-id="eb0f4-211">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="eb0f4-212">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="eb0f4-212">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="eb0f4-213">жетрестореинстанце</span><span class="sxs-lookup"><span data-stu-id="eb0f4-213">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="eb0f4-214">жетстопсервицеинстанце</span><span class="sxs-lookup"><span data-stu-id="eb0f4-214">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)  
[<span data-ttu-id="eb0f4-215">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="eb0f4-215">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
