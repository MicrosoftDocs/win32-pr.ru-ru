---
description: Дополнительные сведения о функции Жетресторе
title: Функция JetRestore
TOCTitle: JetRestore Function
ms:assetid: cdfb8823-6260-46f2-adfc-77e2512a68fd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294093(v=EXCHG.10)
ms:contentKeyID: 32765708
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore
- JetRestoreW
- JetRestoreA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ed164bb6775150f9745cb0e6d9b158a5f03f146
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104000549"
---
# <a name="jetrestore-function"></a><span data-ttu-id="dc79c-103">Функция JetRestore</span><span class="sxs-lookup"><span data-stu-id="dc79c-103">JetRestore Function</span></span>


<span data-ttu-id="dc79c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dc79c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore-function"></a><span data-ttu-id="dc79c-105">Функция JetRestore</span><span class="sxs-lookup"><span data-stu-id="dc79c-105">JetRestore Function</span></span>

<span data-ttu-id="dc79c-106">Функция **жетресторе** восстанавливает и восстанавливает потоковую передачу резервной копии экземпляра, включая все подключенные базы данных.</span><span class="sxs-lookup"><span data-stu-id="dc79c-106">The **JetRestore** function restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="dc79c-107">Эта функция предназначена в первую очередь для обеспечения обратной совместимости с Windows 2000 и более ранними ядрами СУБД, в которых разрешен только один экземпляр базы данных.</span><span class="sxs-lookup"><span data-stu-id="dc79c-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="dc79c-108">В этом случае активный экземпляр — это восстанавливаемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="dc79c-108">In this case, the active instance is the instance that is restored.</span></span> <span data-ttu-id="dc79c-109">При использовании **жетресторе** расположение восстановленных баз данных указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="dc79c-109">With **JetRestore**, the location for the restored databases cannot be specified.</span></span>

```cpp
JET_ERR JET_API JetRestore(
  __in          JET_PCSTR sz,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="dc79c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc79c-110">Parameters</span></span>

<span data-ttu-id="dc79c-111">*SZ*</span><span class="sxs-lookup"><span data-stu-id="dc79c-111">*sz*</span></span>

<span data-ttu-id="dc79c-112">Папка, в которой находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="dc79c-112">The folder where the backup is located.</span></span> <span data-ttu-id="dc79c-113">Резервная копия должна быть создана с помощью функции [жетбаккуп](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="dc79c-113">The backup should have been generated using the [JetBackup](./jetbackup-function.md) function.</span></span>

<span data-ttu-id="dc79c-114">*PFN*</span><span class="sxs-lookup"><span data-stu-id="dc79c-114">*pfn*</span></span>

<span data-ttu-id="dc79c-115">Необязательный указатель на функцию, которая будет вызываться как уведомление о ходе выполнения операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="dc79c-115">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="dc79c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc79c-116">Return Value</span></span>

<span data-ttu-id="dc79c-117">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="dc79c-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="dc79c-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dc79c-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc79c-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dc79c-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="dc79c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="dc79c-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc79c-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dc79c-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dc79c-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dc79c-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc79c-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="dc79c-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="dc79c-124">Не удалось выполнить операцию, так как модуль уже инициализирован для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dc79c-124">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc79c-125">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="dc79c-125">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="dc79c-126">Набор файлов журнала из резервного набора данных и из текущего пути к журналу не совпадают.</span><span class="sxs-lookup"><span data-stu-id="dc79c-126">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc79c-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="dc79c-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="dc79c-128">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="dc79c-128">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc79c-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="dc79c-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="dc79c-130">Не удалось выполнить операцию, так как некоторые из указанных путей являются недопустимыми (путь резервной копии, путь назначения, журнал или системный путь для экземпляра).</span><span class="sxs-lookup"><span data-stu-id="dc79c-130">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc79c-131">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="dc79c-131">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="dc79c-132">Операция завершилась сбоем, так как модуль настроен на использование размера страницы базы данных (с использованием <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> для <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), который не соответствует размеру страницы базы данных, используемому для создания файлов журнала транзакций, или баз данных, связанных с файлами журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="dc79c-132">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc79c-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="dc79c-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="dc79c-134">Операция завершилась с ошибкой, так как параметры явно заданный режим одиночного экземпляра (режим совместимости Windows 2000) и модуль уже находятся в режиме с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="dc79c-134">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc79c-135">В случае успеха файлы базы данных из набора резервных копий будут восстановлены в своем расположении, а восстановление будет выполняться таким, что базы данных будут находиться в состоянии чистой согласованности транзакций.</span><span class="sxs-lookup"><span data-stu-id="dc79c-135">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="dc79c-136">Восстановление приведет к воспроизведению файлов журналов из резервного набора данных и файлов журналов из пути к журналу, если такие файлы существуют.</span><span class="sxs-lookup"><span data-stu-id="dc79c-136">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="dc79c-137">Это восстановление приведет к изменению файла контрольных точек, файлов журнала транзакций и любых баз данных, на которые ссылаются эти файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="dc79c-137">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="dc79c-138">При сбое экземпляр остается в неинициализированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="dc79c-138">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="dc79c-139">Состояние файлов журнала транзакций и всех баз данных, на которые ссылаются эти файлы журнала транзакций, скорее всего, будет изменено при попытке инициализации восстановления и восстановления баз данных.</span><span class="sxs-lookup"><span data-stu-id="dc79c-139">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="dc79c-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc79c-140">Remarks</span></span>

<span data-ttu-id="dc79c-141">Процесс восстановления воссоздаст базы данных, присоединенные к экземпляру во время резервного копирования, и сохранит изменения в файлах базы данных.</span><span class="sxs-lookup"><span data-stu-id="dc79c-141">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="dc79c-142">Результатом будут базы данных с одинаковыми транзакциями.</span><span class="sxs-lookup"><span data-stu-id="dc79c-142">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="dc79c-143">По возможности он также сохраняет в базе данных изменения, выполненные с момента создания резервной копии до тех пор, пока в журналах транзакций не найдется Последнее изменение.</span><span class="sxs-lookup"><span data-stu-id="dc79c-143">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="dc79c-144">Это могло быть возможно, если журналы транзакций, созданные с момента создания резервной копии, все еще находятся в каталоге журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="dc79c-144">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="dc79c-145">Обратите внимание, что если для экземпляра было включено циклическое ведение журнала, то созданные журналы транзакций повторно используются, так что восстановление сможет сохранить изменения, которые были выполнены в момент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="dc79c-145">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="dc79c-146">В любом случае этот процесс может занять довольно много времени, если количество файлов журнала транзакций, воспроизводимых с базами данных, велико.</span><span class="sxs-lookup"><span data-stu-id="dc79c-146">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="dc79c-147">Функции **жетресторе** должны вызываться для экземпляра до вызова [жетинит](./jetinit-function.md) для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dc79c-147">**JetRestore** functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="dc79c-148">Так как во время восстановления будет использоваться значительное количество страниц базы данных и журналов транзакций, то для этих функций может возвращаться вся последовательность ошибок.</span><span class="sxs-lookup"><span data-stu-id="dc79c-148">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="dc79c-149">Такие ошибки могут воздержаться во временных сбоях выделения ресурсов, таких как Jet_errOutOfMemory к ошибкам, представляющим физические повреждения, такие как JET_errReadVerifyFailure, JET_errLogFileCorrupt или JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="dc79c-149">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="dc79c-150">Эти ошибки почти всегда вызываются аппаратными проблемами, поэтому их нельзя избежать.</span><span class="sxs-lookup"><span data-stu-id="dc79c-150">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="dc79c-151">Необычное Управление файлами будет самим манифестом JET_errMissingLogFile или JET_errAttachedDatabaseMismatch или JET_errDatabaseSharingViolation или JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="dc79c-151">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="dc79c-152">Эти ошибки предотвращаются приложением.</span><span class="sxs-lookup"><span data-stu-id="dc79c-152">These errors are preventable by the application.</span></span> <span data-ttu-id="dc79c-153">Приложение должно быть аккуратным, чтобы защитить репозиторий этих файлов от манипуляции извне, такими как пользователь или другие приложения.</span><span class="sxs-lookup"><span data-stu-id="dc79c-153">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="dc79c-154">Если приложение должно полностью уничтожить экземпляр, необходимо удалить все файлы, связанные с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="dc79c-154">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="dc79c-155">К ним относятся файл контрольных точек, файлы журнала транзакций и все файлы базы данных, присоединенные к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="dc79c-155">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="dc79c-156">На различных этапах восстановления будут созданы записи журнала событий, включая ход воспроизведения журнала транзакций и окончательный результат восстановления.</span><span class="sxs-lookup"><span data-stu-id="dc79c-156">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dc79c-157">Требования</span><span class="sxs-lookup"><span data-stu-id="dc79c-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc79c-158"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="dc79c-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dc79c-159">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="dc79c-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc79c-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dc79c-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dc79c-161">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="dc79c-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc79c-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dc79c-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dc79c-163">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="dc79c-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc79c-164"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="dc79c-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dc79c-165">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dc79c-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc79c-166"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="dc79c-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dc79c-167">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dc79c-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc79c-168"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="dc79c-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="dc79c-169">Реализуется как <strong>жетресторев</strong> (Юникод) и <strong>жетрестореа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="dc79c-169">Implemented as <strong>JetRestoreW</strong> (Unicode) and <strong>JetRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dc79c-170">См. также:</span><span class="sxs-lookup"><span data-stu-id="dc79c-170">See Also</span></span>

[<span data-ttu-id="dc79c-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dc79c-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dc79c-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="dc79c-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="dc79c-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="dc79c-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="dc79c-174">жетбаккуп</span><span class="sxs-lookup"><span data-stu-id="dc79c-174">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="dc79c-175">жетбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="dc79c-175">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="dc79c-176">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="dc79c-176">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="dc79c-177">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="dc79c-177">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
