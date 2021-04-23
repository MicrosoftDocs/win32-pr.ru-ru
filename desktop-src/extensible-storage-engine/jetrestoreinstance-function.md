---
description: Дополнительные сведения о функции Жетрестореинстанце
title: Функция JetRestoreInstance
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb7af096a63880a88496631999ddbc26a975cac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272394"
---
# <a name="jetrestoreinstance-function"></a><span data-ttu-id="1bc94-103">Функция JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="1bc94-103">JetRestoreInstance Function</span></span>


<span data-ttu-id="1bc94-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1bc94-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestoreinstance-function"></a><span data-ttu-id="1bc94-105">Функция JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="1bc94-105">JetRestoreInstance Function</span></span>

<span data-ttu-id="1bc94-106">Функция **жетрестореинстанце** восстанавливает и восстанавливает потоковую передачу резервной копии экземпляра, включая все подключенные базы данных.</span><span class="sxs-lookup"><span data-stu-id="1bc94-106">The **JetRestoreInstance** function restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="1bc94-107">Он предназначен для работы с резервной копией, созданной с помощью функции [жетбаккупинстанце](./jetbackupinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc94-107">It is designed to work with a backup created with the [JetBackupInstance](./jetbackupinstance-function.md) function.</span></span> <span data-ttu-id="1bc94-108">Это самая простая и Инкапсулированная функция Restore.</span><span class="sxs-lookup"><span data-stu-id="1bc94-108">This is the simplest and most encapsulated one restore function.</span></span>

<span data-ttu-id="1bc94-109">**Windows XP:**  **Жетрестореинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1bc94-109">**Windows XP:**  **JetRestoreInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="1bc94-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bc94-110">Parameters</span></span>

<span data-ttu-id="1bc94-111">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="1bc94-111">*instance*</span></span>

<span data-ttu-id="1bc94-112">Указывает экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="1bc94-112">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="1bc94-113">Для Windows XP и более поздних версий использование этого параметра зависит от режима работы ядра.</span><span class="sxs-lookup"><span data-stu-id="1bc94-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="1bc94-114">Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, то этот параметр может иметь значение NULL или быть установлен в допустимый выходной буфер, содержащий NULL или JET_instanceNil, который будет возвращать глобальный экземпляр, созданный в качестве побочного результата инициализации.</span><span class="sxs-lookup"><span data-stu-id="1bc94-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="1bc94-115">Этот экземпляр можно передать в любой другой API, который принимает экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1bc94-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="1bc94-116">Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть установлен в допустимый входной буфер, содержащий возвращаемый [жеткреатеинстанце](./jetcreateinstance-function.md) экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1bc94-116">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="1bc94-117">*SZ*</span><span class="sxs-lookup"><span data-stu-id="1bc94-117">*sz*</span></span>

<span data-ttu-id="1bc94-118">Папка, в которой находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="1bc94-118">The folder where the backup is located.</span></span> <span data-ttu-id="1bc94-119">Резервная копия должна быть создана с помощью API-интерфейсов [жетбаккуп](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc94-119">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="1bc94-120">*сздест*</span><span class="sxs-lookup"><span data-stu-id="1bc94-120">*szDest*</span></span>

<span data-ttu-id="1bc94-121">Имя папки, в которую будут копироваться и восстанавливаться файлы базы данных из набора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="1bc94-121">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="1bc94-122">Если задано значение NULL (то есть для устаревшей [жетресторе](./jetrestore-function.md)), файлы базы данных будут скопированы и восстановлены в исходном расположении.</span><span class="sxs-lookup"><span data-stu-id="1bc94-122">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="1bc94-123">*PFN*</span><span class="sxs-lookup"><span data-stu-id="1bc94-123">*pfn*</span></span>

<span data-ttu-id="1bc94-124">Необязательный указатель на функцию, которая будет вызываться как уведомление о ходе выполнения операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="1bc94-124">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="1bc94-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bc94-125">Return Value</span></span>

<span data-ttu-id="1bc94-126">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="1bc94-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1bc94-127">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1bc94-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1bc94-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1bc94-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="1bc94-129">Описание</span><span class="sxs-lookup"><span data-stu-id="1bc94-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bc94-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1bc94-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1bc94-131">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1bc94-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bc94-132">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="1bc94-132">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="1bc94-133">Не удалось выполнить операцию, так как модуль уже инициализирован для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1bc94-133">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bc94-134">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="1bc94-134">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="1bc94-135">Набор файлов журнала из резервного набора данных и из текущего пути к журналу не совпадают.</span><span class="sxs-lookup"><span data-stu-id="1bc94-135">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bc94-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1bc94-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1bc94-137">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="1bc94-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="1bc94-138">Эта ошибка будет возвращена <strong>жетрестореинстанце</strong> , когда модуль находится в режиме с несколькими экземплярами, а пинстанце ссылается на недопустимый экземпляр Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="1bc94-138">This error will be returned by <strong>JetRestoreInstance</strong> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bc94-139">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="1bc94-139">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="1bc94-140">Не удалось выполнить операцию, так как некоторые из указанных путей являются недопустимыми (путь резервной копии, путь назначения, журнал или системный путь для экземпляра).</span><span class="sxs-lookup"><span data-stu-id="1bc94-140">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bc94-141">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="1bc94-141">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="1bc94-142">Операция завершилась сбоем, так как модуль настроен на использование размера страницы базы данных (с использованием <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> для <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), который не соответствует размеру страницы базы данных, используемому для создания файлов журнала транзакций, или баз данных, связанных с файлами журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="1bc94-142">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bc94-143">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="1bc94-143">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="1bc94-144">Операция завершилась с ошибкой, так как параметры явно заданный режим одиночного экземпляра (режим совместимости Windows 2000) и модуль уже находятся в режиме с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="1bc94-144">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bc94-145">В случае успеха файлы базы данных из набора резервных копий будут восстановлены в своем расположении, а восстановление будет выполняться таким, что базы данных будут находиться в состоянии чистой согласованности транзакций.</span><span class="sxs-lookup"><span data-stu-id="1bc94-145">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="1bc94-146">Восстановление приведет к воспроизведению файлов журналов из резервного набора данных и файлов журналов из пути к журналу, если такие файлы существуют.</span><span class="sxs-lookup"><span data-stu-id="1bc94-146">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="1bc94-147">Это восстановление приведет к изменению файла контрольных точек, файлов журнала транзакций и любых баз данных, на которые ссылаются эти файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="1bc94-147">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="1bc94-148">При сбое экземпляр остается в неинициализированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1bc94-148">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="1bc94-149">Состояние файлов журнала транзакций и всех баз данных, на которые ссылаются эти файлы журнала транзакций, скорее всего, будет изменено при попытке инициализации восстановления и восстановления баз данных.</span><span class="sxs-lookup"><span data-stu-id="1bc94-149">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1bc94-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bc94-150">Remarks</span></span>

<span data-ttu-id="1bc94-151">Процесс восстановления воссоздаст базы данных, присоединенные к экземпляру во время резервного копирования, и сохранит изменения в файлах базы данных.</span><span class="sxs-lookup"><span data-stu-id="1bc94-151">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="1bc94-152">Результатом будут базы данных с одинаковыми транзакциями.</span><span class="sxs-lookup"><span data-stu-id="1bc94-152">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="1bc94-153">По возможности он также сохраняет в базе данных изменения, выполненные с момента создания резервной копии до тех пор, пока в журналах транзакций не найдется Последнее изменение.</span><span class="sxs-lookup"><span data-stu-id="1bc94-153">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="1bc94-154">Это могло быть возможно, если журналы транзакций, созданные с момента создания резервной копии, все еще находятся в каталоге журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="1bc94-154">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="1bc94-155">Обратите внимание, что если для экземпляра было включено циклическое ведение журнала, то созданные журналы транзакций повторно используются, так что восстановление сможет сохранить изменения, которые были выполнены в момент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="1bc94-155">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="1bc94-156">В любом случае этот процесс может занять довольно много времени, если количество файлов журнала транзакций, воспроизводимых с базами данных, велико.</span><span class="sxs-lookup"><span data-stu-id="1bc94-156">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="1bc94-157">**Жетрестореинстанце** должен вызываться для экземпляра, который уже был создан с помощью [жеткреатеинстанце](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="1bc94-157">**JetRestoreInstance** must be called on an instance which was already created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="1bc94-158">Так как во время восстановления будет использоваться значительное количество страниц базы данных и журналов транзакций, то для этих функций может возвращаться вся последовательность ошибок.</span><span class="sxs-lookup"><span data-stu-id="1bc94-158">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="1bc94-159">Такие ошибки могут воздержаться во временных сбоях выделения ресурсов, таких как Jet_errOutOfMemory к ошибкам, представляющим физические повреждения, такие как JET_errReadVerifyFailure, JET_errLogFileCorrupt или JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="1bc94-159">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="1bc94-160">Эти ошибки почти всегда вызываются аппаратными проблемами, поэтому их нельзя избежать.</span><span class="sxs-lookup"><span data-stu-id="1bc94-160">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="1bc94-161">Необычное Управление файлами будет самим манифестом JET_errMissingLogFile или JET_errAttachedDatabaseMismatch или JET_errDatabaseSharingViolation или JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="1bc94-161">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="1bc94-162">Эти ошибки предотвращаются приложением.</span><span class="sxs-lookup"><span data-stu-id="1bc94-162">These errors are preventable by the application.</span></span> <span data-ttu-id="1bc94-163">Приложение должно быть аккуратным, чтобы защитить репозиторий этих файлов от манипуляции извне, такими как пользователь или другие приложения.</span><span class="sxs-lookup"><span data-stu-id="1bc94-163">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="1bc94-164">Если приложение должно полностью уничтожить экземпляр, необходимо удалить все файлы, связанные с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="1bc94-164">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="1bc94-165">К ним относятся файл контрольных точек, файлы журнала транзакций и все файлы базы данных, присоединенные к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="1bc94-165">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="1bc94-166">На различных этапах восстановления будут созданы записи журнала событий, включая ход воспроизведения журнала транзакций и окончательный результат восстановления.</span><span class="sxs-lookup"><span data-stu-id="1bc94-166">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1bc94-167">Требования</span><span class="sxs-lookup"><span data-stu-id="1bc94-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bc94-168"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1bc94-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1bc94-169">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1bc94-169">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bc94-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1bc94-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1bc94-171">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1bc94-171">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bc94-172"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1bc94-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1bc94-173">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1bc94-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bc94-174"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="1bc94-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1bc94-175">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1bc94-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bc94-176"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="1bc94-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1bc94-177">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1bc94-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bc94-178"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="1bc94-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1bc94-179">Реализуется как <strong>жетрестореинстанцев</strong> (Юникод) и <strong>жетрестореинстанцеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1bc94-179">Implemented as <strong>JetRestoreInstanceW</strong> (Unicode) and <strong>JetRestoreInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1bc94-180">См. также:</span><span class="sxs-lookup"><span data-stu-id="1bc94-180">See Also</span></span>

[<span data-ttu-id="1bc94-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1bc94-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1bc94-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1bc94-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1bc94-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1bc94-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="1bc94-184">жетбаккуп</span><span class="sxs-lookup"><span data-stu-id="1bc94-184">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="1bc94-185">жетбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="1bc94-185">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="1bc94-186">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="1bc94-186">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="1bc94-187">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="1bc94-187">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
