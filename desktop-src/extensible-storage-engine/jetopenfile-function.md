---
description: Дополнительные сведения о функции Жетопенфиле
title: Функция JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692124"
---
# <a name="jetopenfile-function"></a><span data-ttu-id="093cf-103">Функция JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="093cf-103">JetOpenFile Function</span></span>


<span data-ttu-id="093cf-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="093cf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfile-function"></a><span data-ttu-id="093cf-105">Функция JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="093cf-105">JetOpenFile Function</span></span>

<span data-ttu-id="093cf-106">Функция **жетопенфиле** открывает присоединенную базу данных, файл исправления базы данных или файл журнала транзакций активного экземпляра для выполнения потоковой архивации с нечеткой назначением.</span><span class="sxs-lookup"><span data-stu-id="093cf-106">The **JetOpenFile** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="093cf-107">Затем данные из этих файлов можно считать с помощью возвращенного маркера с помощью [жетреадфиле](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="093cf-107">The data from these files can subsequently be read through the returned handle using [JetReadFile](./jetreadfile-function.md).</span></span> <span data-ttu-id="093cf-108">Возвращаемый обработчик должен быть закрыт с помощью [жетклосефиле](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="093cf-108">The returned handle must be closed using [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="093cf-109">Внешнее резервное копирование экземпляра должно быть ранее инициировано с помощью [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="093cf-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="093cf-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="093cf-110">Parameters</span></span>

<span data-ttu-id="093cf-111">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="093cf-111">*szFileName*</span></span>

<span data-ttu-id="093cf-112">Относительный или абсолютный путь к присоединенной базе данных, файлу исправления базы данных или файлу журнала транзакций, управляемому экземпляром, который будет считаться резервной копией.</span><span class="sxs-lookup"><span data-stu-id="093cf-112">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that will be read for backup.</span></span>

<span data-ttu-id="093cf-113">*фффиле*</span><span class="sxs-lookup"><span data-stu-id="093cf-113">*phfFile*</span></span>

<span data-ttu-id="093cf-114">Выходной буфер, который получает обработчик для чтения файла.</span><span class="sxs-lookup"><span data-stu-id="093cf-114">The output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="093cf-115">*пулфилесизелов*</span><span class="sxs-lookup"><span data-stu-id="093cf-115">*pulFileSizeLow*</span></span>

<span data-ttu-id="093cf-116">Выходной буфер, который получает наименее значащий 32 бит размера файла.</span><span class="sxs-lookup"><span data-stu-id="093cf-116">The output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="093cf-117">*пулфилесизехигх*</span><span class="sxs-lookup"><span data-stu-id="093cf-117">*pulFileSizeHigh*</span></span>

<span data-ttu-id="093cf-118">Выходной буфер, который получает наиболее значимый 32 бит размера файла.</span><span class="sxs-lookup"><span data-stu-id="093cf-118">The output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="093cf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="093cf-119">Return Value</span></span>

<span data-ttu-id="093cf-120">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="093cf-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="093cf-121">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="093cf-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="093cf-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="093cf-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="093cf-123">Описание</span><span class="sxs-lookup"><span data-stu-id="093cf-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="093cf-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="093cf-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="093cf-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="093cf-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-126">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="093cf-126">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="093cf-127">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="093cf-127">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="093cf-128">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="093cf-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="093cf-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="093cf-130">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="093cf-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-131">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="093cf-131">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="093cf-132">Не удалось выполнить операцию, так как не удалось открыть запрошенный файл из-за нарушения общего доступа или недостаточных привилегий.</span><span class="sxs-lookup"><span data-stu-id="093cf-132">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-133">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="093cf-133">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="093cf-134">Не удалось выполнить операцию, так как не удалось открыть запрошенный файл, так как он не найден по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="093cf-134">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="093cf-135">Эта ошибка будет возвращена только Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="093cf-135">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="093cf-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="093cf-137">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="093cf-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="093cf-138">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="093cf-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="093cf-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="093cf-140">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="093cf-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="093cf-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="093cf-142">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="093cf-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="093cf-143">Это может произойти для <strong>жетопенфиле</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="093cf-143">This can happen for <strong>JetOpenFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="093cf-144">Указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="093cf-144">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="093cf-145">Указанный параметр filename имеет значение NULL или строку нулевой длины (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="093cf-145">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-146">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="093cf-146">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="093cf-147">Не удалось выполнить операцию, так как не удалось найти указанный путь.</span><span class="sxs-lookup"><span data-stu-id="093cf-147">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-148">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="093cf-148">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="093cf-149">Не удалось открыть запрошенный файл для резервного копирования, так как он не найден.</span><span class="sxs-lookup"><span data-stu-id="093cf-149">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="093cf-150">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="093cf-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-151">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="093cf-151">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="093cf-152">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="093cf-152">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="093cf-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="093cf-154">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="093cf-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-155">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="093cf-155">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="093cf-156">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="093cf-156">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="093cf-157"><strong>Жетопенфиле</strong> возвратит JET_errOutOfMemory, если предпринимается попытка открыть другой файл до того, как предыдущий файл, Открытый с помощью <strong>жетопенфиле</strong> , был закрыт <a href="gg294127(v=exchg.10).md">жетклосефиле</a>.</span><span class="sxs-lookup"><span data-stu-id="093cf-157"><strong>JetOpenFile</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFile</strong> has been closed by <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span></span> <span data-ttu-id="093cf-158">В настоящее время поддерживается только один необработанный обработчик файлов.</span><span class="sxs-lookup"><span data-stu-id="093cf-158">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-159">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="093cf-159">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="093cf-160">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="093cf-160">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="093cf-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="093cf-162">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="093cf-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span> <span data-ttu-id="093cf-163">JET_errRestoreInProgress выполнить операцию невозможно, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="093cf-163">JET_errRestoreInProgress It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="093cf-164">При успешном выполнении будет возвращен обработчик запрошенного файла.</span><span class="sxs-lookup"><span data-stu-id="093cf-164">On success, a handle to the requested file will be returned.</span></span> <span data-ttu-id="093cf-165">Если этот обработчик предназначен для файла базы данных, то этот файл базы данных будет подготовлен для потоковой архивации, что может привести к созданию файла исправления базы данных в том же расположении, что и файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="093cf-165">If the handle is for a database file, that database file will be prepared for streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="093cf-166">Файл исправления базы данных имеет тот же путь и имя файла, что и файл базы данных, но имеет. Расширение PAT.</span><span class="sxs-lookup"><span data-stu-id="093cf-166">The database patch file has the exact same path and filename as the database file, but has a .PAT extension.</span></span> <span data-ttu-id="093cf-167">Также будет возвращен размер файла.</span><span class="sxs-lookup"><span data-stu-id="093cf-167">The size of the file will also be returned.</span></span>

<span data-ttu-id="093cf-168">В случае сбоя состояние выходных буферов будет не определено.</span><span class="sxs-lookup"><span data-stu-id="093cf-168">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="093cf-169">Файл исправления базы данных может быть временно создан на диске, а любой существующий файл в расположении файла исправления может быть удален.</span><span class="sxs-lookup"><span data-stu-id="093cf-169">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="093cf-170">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="093cf-170">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="093cf-171">В Windows XP и более поздних версиях резервная копия не будет отменена, если была предпринята попытка резервного копирования базы данных, которая не была присоединена к экземпляру во время вызова.</span><span class="sxs-lookup"><span data-stu-id="093cf-171">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="093cf-172">**Предупреждение об ошибке**  По соображениям безопасности важно отметить, что **жетопенфиле** не проверяет, связан ли запрошенный путь к файлу с набором файлов, которые должны быть резервными копиями для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="093cf-172">**Warning**  For security reasons, it is important to note that **JetOpenFile** does not verify that the requested file path is associated with the set of files that should be backed up for the instance.</span></span> <span data-ttu-id="093cf-173">В результате эту функцию можно использовать для доступа к любому файлу, который может быть открыт текущим контекстом безопасности потока.</span><span class="sxs-lookup"><span data-stu-id="093cf-173">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="093cf-174">Очень важно, чтобы приложение ограничивало пути, передаваемые этой функции, известному набору правильных путей к файлам или разглашению атаки на информацию.</span><span class="sxs-lookup"><span data-stu-id="093cf-174">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="093cf-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="093cf-175">Remarks</span></span>

<span data-ttu-id="093cf-176">Должны присутствовать выходные буферы и размер файла.</span><span class="sxs-lookup"><span data-stu-id="093cf-176">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="093cf-177">Если они отсутствуют, произойдет сбой ядра, так как параметры выходного буфера не проверяются.</span><span class="sxs-lookup"><span data-stu-id="093cf-177">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="093cf-178">В данный момент только один файл может быть открыт для резервного копирования в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="093cf-178">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="093cf-179">**Жетопенфиле** не утверждает права на резервное копирование перед открытием запрошенного файла.</span><span class="sxs-lookup"><span data-stu-id="093cf-179">**JetOpenFile** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="093cf-180">Размер файла, который будет считаться этой функцией, может не соответствовать размеру файла на диске.</span><span class="sxs-lookup"><span data-stu-id="093cf-180">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="093cf-181">В Windows XP и более поздних выпусках дополнительные сведения могут быть добавлены к файлу базы данных, который используется ядром СУБД во время операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="093cf-181">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="093cf-182">Таким образом, приложение должно полагаться только на размер файла, возвращенный **жетопенфиле** , или на фактическое число байтов данных, возвращенных [жетреадфиле](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="093cf-182">As such, the application should only rely on the file size returned by **JetOpenFile** or on the actual number of bytes of data returned by [JetReadFile](./jetreadfile-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="093cf-183">Требования</span><span class="sxs-lookup"><span data-stu-id="093cf-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="093cf-184"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="093cf-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="093cf-185">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="093cf-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="093cf-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="093cf-187">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="093cf-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="093cf-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="093cf-189">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="093cf-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-190"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="093cf-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="093cf-191">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="093cf-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="093cf-192"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="093cf-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="093cf-193">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="093cf-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093cf-194"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="093cf-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="093cf-195">Реализуется как <strong>жетопенфилев</strong> (Юникод) и <strong>жетопенфилеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="093cf-195">Implemented as <strong>JetOpenFileW</strong> (Unicode) and <strong>JetOpenFileA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="093cf-196">См. также:</span><span class="sxs-lookup"><span data-stu-id="093cf-196">See Also</span></span>

[<span data-ttu-id="093cf-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="093cf-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="093cf-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="093cf-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="093cf-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="093cf-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="093cf-200">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="093cf-200">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="093cf-201">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="093cf-201">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="093cf-202">жетклосефиле</span><span class="sxs-lookup"><span data-stu-id="093cf-202">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="093cf-203">жетжетаттачинфо</span><span class="sxs-lookup"><span data-stu-id="093cf-203">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="093cf-204">жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="093cf-204">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="093cf-205">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="093cf-205">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="093cf-206">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="093cf-206">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="093cf-207">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="093cf-207">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="093cf-208">жеттрункателог</span><span class="sxs-lookup"><span data-stu-id="093cf-208">JetTruncateLog</span></span>](./jettruncatelog-function.md)
