---
description: Дополнительные сведения о функции JetRestore2
title: Функция JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb297aac0bc26e50bba519206eff346abb7943c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703086"
---
# <a name="jetrestore2-function"></a><span data-ttu-id="245b4-103">Функция JetRestore2</span><span class="sxs-lookup"><span data-stu-id="245b4-103">JetRestore2 Function</span></span>


<span data-ttu-id="245b4-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="245b4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore2-function"></a><span data-ttu-id="245b4-105">Функция JetRestore2</span><span class="sxs-lookup"><span data-stu-id="245b4-105">JetRestore2 Function</span></span>

<span data-ttu-id="245b4-106">**JetRestore2** восстанавливает и восстанавливает потоковую передачу резервной копии экземпляра, включая все подключенные базы данных.</span><span class="sxs-lookup"><span data-stu-id="245b4-106">The **JetRestore2** restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="245b4-107">Эта функция предназначена в первую очередь для обеспечения обратной совместимости с Windows 2000 и более ранними ядрами СУБД, в которых разрешен только один экземпляр базы данных.</span><span class="sxs-lookup"><span data-stu-id="245b4-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="245b4-108">В этом случае активный экземпляр — это восстанавливаемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="245b4-108">In this case, the active instance is the instance that is restored.</span></span>

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="245b4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="245b4-109">Parameters</span></span>

<span data-ttu-id="245b4-110">*SZ*</span><span class="sxs-lookup"><span data-stu-id="245b4-110">*sz*</span></span>

<span data-ttu-id="245b4-111">Папка, в которой находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="245b4-111">The folder where the backup is located.</span></span> <span data-ttu-id="245b4-112">Резервная копия должна быть создана с помощью API-интерфейсов [жетбаккуп](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="245b4-112">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="245b4-113">*сздест*</span><span class="sxs-lookup"><span data-stu-id="245b4-113">*szDest*</span></span>

<span data-ttu-id="245b4-114">Имя папки, в которую будут копироваться и восстанавливаться файлы базы данных из набора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="245b4-114">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="245b4-115">Если задано значение NULL (то есть для устаревшей [жетресторе](./jetrestore-function.md)), файлы базы данных будут скопированы и восстановлены в исходном расположении.</span><span class="sxs-lookup"><span data-stu-id="245b4-115">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="245b4-116">*PFN*</span><span class="sxs-lookup"><span data-stu-id="245b4-116">*pfn*</span></span>

<span data-ttu-id="245b4-117">Необязательный указатель на функцию, которая будет вызываться как уведомление о ходе выполнения операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="245b4-117">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="245b4-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="245b4-118">Return Value</span></span>

<span data-ttu-id="245b4-119">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="245b4-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="245b4-120">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="245b4-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="245b4-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="245b4-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="245b4-122">Описание</span><span class="sxs-lookup"><span data-stu-id="245b4-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="245b4-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="245b4-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="245b4-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="245b4-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245b4-125">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="245b4-125">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="245b4-126">Не удалось выполнить операцию, так как модуль уже инициализирован для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="245b4-126">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="245b4-127">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="245b4-127">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="245b4-128">Набор файлов журнала из резервного набора данных и из текущего пути к журналу не совпадают.</span><span class="sxs-lookup"><span data-stu-id="245b4-128">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245b4-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="245b4-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="245b4-130">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="245b4-130">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="245b4-131">Эта ошибка будет возвращена <a href="gg269306(v=exchg.10).md">жетрестореинстанце</a> , когда модуль находится в режиме с несколькими экземплярами, а пинстанце ссылается на недопустимый экземпляр Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="245b4-131">This error will be returned by <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="245b4-132">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="245b4-132">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="245b4-133">Не удалось выполнить операцию, так как некоторые из указанных путей являются недопустимыми (путь резервной копии, путь назначения, журнал или системный путь для экземпляра).</span><span class="sxs-lookup"><span data-stu-id="245b4-133">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245b4-134">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="245b4-134">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="245b4-135">Операция завершилась сбоем, так как модуль настроен на использование размера страницы базы данных (с использованием <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> для <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), который не соответствует размеру страницы базы данных, используемому для создания файлов журнала транзакций, или баз данных, связанных с файлами журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="245b4-135">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="245b4-136">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="245b4-136">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="245b4-137">Операция завершилась с ошибкой, так как параметры явно заданный режим одиночного экземпляра (режим совместимости Windows 2000) и модуль уже находятся в режиме с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="245b4-137">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="245b4-138">В случае успеха файлы базы данных из набора резервных копий будут восстановлены в своем расположении, а восстановление будет выполняться таким, что базы данных будут находиться в состоянии чистой согласованности транзакций.</span><span class="sxs-lookup"><span data-stu-id="245b4-138">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="245b4-139">Восстановление приведет к воспроизведению файлов журналов из резервного набора данных и файлов журналов из пути к журналу, если такие файлы существуют.</span><span class="sxs-lookup"><span data-stu-id="245b4-139">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="245b4-140">Это восстановление приведет к изменению файла контрольных точек, файлов журнала транзакций и любых баз данных, на которые ссылаются эти файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="245b4-140">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="245b4-141">При сбое экземпляр остается в неинициализированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="245b4-141">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="245b4-142">Состояние файлов журнала транзакций и всех баз данных, на которые ссылаются эти файлы журнала транзакций, скорее всего, будет изменено при попытке инициализации восстановления и восстановления баз данных.</span><span class="sxs-lookup"><span data-stu-id="245b4-142">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="245b4-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="245b4-143">Remarks</span></span>

<span data-ttu-id="245b4-144">Процесс восстановления воссоздаст базы данных, присоединенные к экземпляру во время резервного копирования, и сохранит изменения в файлах базы данных.</span><span class="sxs-lookup"><span data-stu-id="245b4-144">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="245b4-145">Результатом будут базы данных с одинаковыми транзакциями.</span><span class="sxs-lookup"><span data-stu-id="245b4-145">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="245b4-146">По возможности он также сохраняет в базе данных изменения, выполненные с момента создания резервной копии до тех пор, пока в журналах транзакций не найдется Последнее изменение.</span><span class="sxs-lookup"><span data-stu-id="245b4-146">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="245b4-147">Это могло быть возможно, если журналы транзакций, созданные с момента создания резервной копии, все еще находятся в каталоге журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="245b4-147">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="245b4-148">Обратите внимание, что если для экземпляра было включено циклическое ведение журнала, то созданные журналы транзакций повторно используются, так что восстановление сможет сохранить изменения, которые были выполнены в момент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="245b4-148">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="245b4-149">В любом случае этот процесс может занять довольно много времени, если количество файлов журнала транзакций, воспроизводимых с базами данных, велико.</span><span class="sxs-lookup"><span data-stu-id="245b4-149">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="245b4-150">Функции [жетресторе](./jetrestore-function.md) должны вызываться для экземпляра до вызова [жетинит](./jetinit-function.md) для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="245b4-150">[JetRestore](./jetrestore-function.md) functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="245b4-151">Так как во время восстановления будет использоваться значительное количество страниц базы данных и журналов транзакций, то для этих функций может возвращаться вся последовательность ошибок.</span><span class="sxs-lookup"><span data-stu-id="245b4-151">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="245b4-152">Такие ошибки могут воздержаться во временных сбоях выделения ресурсов, таких как Jet_errOutOfMemory к ошибкам, представляющим физические повреждения, такие как JET_errReadVerifyFailure, JET_errLogFileCorrupt или JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="245b4-152">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="245b4-153">Эти ошибки почти всегда вызываются аппаратными проблемами, поэтому их нельзя избежать.</span><span class="sxs-lookup"><span data-stu-id="245b4-153">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="245b4-154">Необычное Управление файлами будет самим манифестом JET_errMissingLogFile или JET_errAttachedDatabaseMismatch или JET_errDatabaseSharingViolation или JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="245b4-154">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="245b4-155">Эти ошибки предотвращаются приложением.</span><span class="sxs-lookup"><span data-stu-id="245b4-155">These errors are preventable by the application.</span></span> <span data-ttu-id="245b4-156">Приложение должно быть аккуратным, чтобы защитить репозиторий этих файлов от манипуляции извне, такими как пользователь или другие приложения.</span><span class="sxs-lookup"><span data-stu-id="245b4-156">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="245b4-157">Если приложение должно полностью уничтожить экземпляр, необходимо удалить все файлы, связанные с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="245b4-157">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="245b4-158">К ним относятся файл контрольных точек, файлы журнала транзакций и все файлы базы данных, присоединенные к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="245b4-158">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="245b4-159">На различных этапах восстановления будут созданы записи журнала событий, включая ход воспроизведения журнала транзакций и окончательный результат восстановления.</span><span class="sxs-lookup"><span data-stu-id="245b4-159">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="245b4-160">Требования</span><span class="sxs-lookup"><span data-stu-id="245b4-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="245b4-161"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="245b4-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="245b4-162">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="245b4-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245b4-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="245b4-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="245b4-164">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="245b4-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="245b4-165"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="245b4-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="245b4-166">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="245b4-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245b4-167"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="245b4-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="245b4-168">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="245b4-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="245b4-169"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="245b4-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="245b4-170">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="245b4-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245b4-171"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="245b4-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="245b4-172">Реализуется как <strong>JetRestore2W</strong> (Юникод) и <strong>JetRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="245b4-172">Implemented as <strong>JetRestore2W</strong> (Unicode) and <strong>JetRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="245b4-173">См. также:</span><span class="sxs-lookup"><span data-stu-id="245b4-173">See Also</span></span>

[<span data-ttu-id="245b4-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="245b4-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="245b4-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="245b4-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="245b4-176">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="245b4-176">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="245b4-177">жетбаккуп</span><span class="sxs-lookup"><span data-stu-id="245b4-177">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="245b4-178">жетбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="245b4-178">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="245b4-179">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="245b4-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="245b4-180">жетинит</span><span class="sxs-lookup"><span data-stu-id="245b4-180">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="245b4-181">жетресторе</span><span class="sxs-lookup"><span data-stu-id="245b4-181">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="245b4-182">жетрестореинстанце</span><span class="sxs-lookup"><span data-stu-id="245b4-182">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="245b4-183">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="245b4-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
