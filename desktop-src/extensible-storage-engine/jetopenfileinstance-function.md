---
description: Дополнительные сведения о функции Жетопенфилеинстанце
title: Функция JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693778"
---
# <a name="jetopenfileinstance-function"></a><span data-ttu-id="918b4-103">Функция JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="918b4-103">JetOpenFileInstance Function</span></span>


<span data-ttu-id="918b4-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="918b4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfileinstance-function"></a><span data-ttu-id="918b4-105">Функция JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="918b4-105">JetOpenFileInstance Function</span></span>

<span data-ttu-id="918b4-106">Функция **жетопенфилеинстанце** открывает присоединенную базу данных, файл исправления базы данных или файл журнала транзакций активного экземпляра для выполнения потоковой архивации с нечеткой назначением.</span><span class="sxs-lookup"><span data-stu-id="918b4-106">The **JetOpenFileInstance** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="918b4-107">Затем данные из этих файлов можно считать с помощью возвращенного маркера с помощью [жетреадфилеинстанце](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="918b4-107">The data from these files can subsequently be read through the returned handle using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span> <span data-ttu-id="918b4-108">Возвращаемый обработчик должен быть закрыт с помощью [жетклосефилеинстанце](./jetclosefileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="918b4-108">The returned handle must be closed using [JetCloseFileInstance](./jetclosefileinstance-function.md).</span></span> <span data-ttu-id="918b4-109">Внешнее резервное копирование экземпляра должно быть ранее инициировано с помощью [жетбегинекстерналбаккупинстанце](./jetbeginexternalbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="918b4-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span></span>

<span data-ttu-id="918b4-110">**Windows XP:**  **Жетопенфилеинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="918b4-110">**Windows XP:**  **JetOpenFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="918b4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="918b4-111">Parameters</span></span>

<span data-ttu-id="918b4-112">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="918b4-112">*instance*</span></span>

<span data-ttu-id="918b4-113">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="918b4-113">The instance to use for this call.</span></span>

<span data-ttu-id="918b4-114">Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="918b4-114">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="918b4-115">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="918b4-115">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="918b4-116">Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="918b4-116">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="918b4-117">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="918b4-117">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="918b4-118">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="918b4-118">*szFileName*</span></span>

<span data-ttu-id="918b4-119">Относительный или абсолютный путь к присоединенной базе данных, файлу исправления базы данных или файлу журнала транзакций, управляемому экземпляром, который считывается для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="918b4-119">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that is read for backup.</span></span>

<span data-ttu-id="918b4-120">*фффиле*</span><span class="sxs-lookup"><span data-stu-id="918b4-120">*phfFile*</span></span>

<span data-ttu-id="918b4-121">Указатель на выходной буфер, который получает маркер для чтения файла.</span><span class="sxs-lookup"><span data-stu-id="918b4-121">Pointer to the output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="918b4-122">*пулфилесизелов*</span><span class="sxs-lookup"><span data-stu-id="918b4-122">*pulFileSizeLow*</span></span>

<span data-ttu-id="918b4-123">Указатель на выходной буфер, который получает наименее значащий 32 бит размера файла.</span><span class="sxs-lookup"><span data-stu-id="918b4-123">Pointer to the output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="918b4-124">*пулфилесизехигх*</span><span class="sxs-lookup"><span data-stu-id="918b4-124">*pulFileSizeHigh*</span></span>

<span data-ttu-id="918b4-125">Указатель на выходной буфер, который получает наиболее значимый 32 бит размера файла.</span><span class="sxs-lookup"><span data-stu-id="918b4-125">Pointer to the output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="918b4-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="918b4-126">Return Value</span></span>

<span data-ttu-id="918b4-127">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="918b4-127">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="918b4-128">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="918b4-128">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="918b4-129">Код возврата</span><span class="sxs-lookup"><span data-stu-id="918b4-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="918b4-130">Описание</span><span class="sxs-lookup"><span data-stu-id="918b4-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="918b4-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="918b4-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="918b4-132">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="918b4-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-133">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="918b4-133">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="918b4-134">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg269309(v=exchg.10).md">жетстопбаккупинстанце</a>.</span><span class="sxs-lookup"><span data-stu-id="918b4-134">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="918b4-135">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="918b4-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="918b4-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="918b4-137">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg294108(v=exchg.10).md">жетстопсервицеинстанце</a>.</span><span class="sxs-lookup"><span data-stu-id="918b4-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-138">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="918b4-138">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="918b4-139">Не удалось выполнить операцию, так как не удалось открыть запрошенный файл из-за нарушения общего доступа или недостаточных привилегий.</span><span class="sxs-lookup"><span data-stu-id="918b4-139">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-140">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="918b4-140">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="918b4-141">Не удалось выполнить операцию, так как не удалось открыть запрошенный файл, так как он не найден по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="918b4-141">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="918b4-142">Эта ошибка будет возвращена только Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="918b4-142">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-143">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="918b4-143">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="918b4-144">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="918b4-144">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-145">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="918b4-145">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="918b4-146">Не удалось выполнить операцию, так как не удалось найти указанный путь.</span><span class="sxs-lookup"><span data-stu-id="918b4-146">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="918b4-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="918b4-148">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="918b4-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="918b4-149">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="918b4-149">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="918b4-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="918b4-151">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="918b4-151">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="918b4-152">Это может произойти для <strong>жетопенфилеинстанце</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="918b4-152">This can happen for <strong>JetOpenFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="918b4-153">Указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="918b4-153">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="918b4-154">Указанный параметр filename имеет значение NULL или строку нулевой длины (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="918b4-154">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-155">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="918b4-155">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="918b4-156">Не удалось открыть запрошенный файл для резервного копирования, так как он не найден.</span><span class="sxs-lookup"><span data-stu-id="918b4-156">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="918b4-157">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="918b4-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-158">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="918b4-158">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="918b4-159">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="918b4-159">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="918b4-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="918b4-161">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="918b4-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-162">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="918b4-162">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="918b4-163">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="918b4-163">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="918b4-164"><strong>Жетопенфилеинстанце</strong> возвратит JET_errOutOfMemory, если предпринимается попытка открыть другой файл до того, как предыдущий файл, Открытый с помощью <strong>жетопенфилеинстанце</strong> , был закрыт <a href="gg269270(v=exchg.10).md">жетклосефилеинстанце</a>.</span><span class="sxs-lookup"><span data-stu-id="918b4-164"><strong>JetOpenFileInstance</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFileInstance</strong> has been closed by <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span></span> <span data-ttu-id="918b4-165">В настоящее время поддерживается только один необработанный обработчик файлов.</span><span class="sxs-lookup"><span data-stu-id="918b4-165">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="918b4-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="918b4-167">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="918b4-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-168">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="918b4-168">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="918b4-169">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="918b4-169">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="918b4-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="918b4-171">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="918b4-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="918b4-172">При успешном выполнении возвращается маркер запрошенного файла.</span><span class="sxs-lookup"><span data-stu-id="918b4-172">On success, a handle to the requested file is returned.</span></span> <span data-ttu-id="918b4-173">Если этот обработчик предназначен для файла базы данных, то этот файл базы данных будет подготовлен для потоковой резервной копии, что может привести к созданию файла исправления базы данных в том же расположении, что и файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="918b4-173">If the handle is for a database file, that database file will be prepared for a streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="918b4-174">Файл исправления базы данных имеет тот же путь и имя файла, что и файл базы данных, но с. Расширение PAT.</span><span class="sxs-lookup"><span data-stu-id="918b4-174">The database patch file has the exact same path and filename as the database file but with a .PAT extension.</span></span> <span data-ttu-id="918b4-175">Также будет возвращен размер файла.</span><span class="sxs-lookup"><span data-stu-id="918b4-175">The size of the file will also be returned.</span></span>

<span data-ttu-id="918b4-176">В случае сбоя состояние выходных буферов будет не определено.</span><span class="sxs-lookup"><span data-stu-id="918b4-176">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="918b4-177">Файл исправления базы данных может быть временно создан на диске, а любой существующий файл в расположении файла исправления может быть удален.</span><span class="sxs-lookup"><span data-stu-id="918b4-177">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="918b4-178">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="918b4-178">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="918b4-179">В Windows XP и более поздних версиях резервная копия не будет отменена, если была предпринята попытка резервного копирования базы данных, которая не была присоединена к экземпляру во время вызова.</span><span class="sxs-lookup"><span data-stu-id="918b4-179">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="918b4-180">**Предупреждение об ошибке**  По соображениям безопасности важно отметить, что **жетопенфилеинстанце** не проверяет, связан ли запрошенный путь к файлу с набором файлов, для которых выполняется резервное копирование экземпляра.</span><span class="sxs-lookup"><span data-stu-id="918b4-180">**Warning**  For security reasons, it is important to note that **JetOpenFileInstance** does not verify that the requested file path is associated with the set of files that are backed up for the instance.</span></span> <span data-ttu-id="918b4-181">В результате эту функцию можно использовать для доступа к любому файлу, который может быть открыт текущим контекстом безопасности потока.</span><span class="sxs-lookup"><span data-stu-id="918b4-181">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="918b4-182">Очень важно, чтобы приложение ограничивало пути, передаваемые этой функции, известному набору правильных путей к файлам или разглашению атаки на информацию.</span><span class="sxs-lookup"><span data-stu-id="918b4-182">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="918b4-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="918b4-183">Remarks</span></span>

<span data-ttu-id="918b4-184">Должны присутствовать выходные буферы и размер файла.</span><span class="sxs-lookup"><span data-stu-id="918b4-184">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="918b4-185">Если они отсутствуют, произойдет сбой ядра, так как параметры выходного буфера не проверяются.</span><span class="sxs-lookup"><span data-stu-id="918b4-185">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="918b4-186">В данный момент только один файл может быть открыт для резервного копирования в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="918b4-186">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="918b4-187">**Жетопенфилеинстанце** не утверждает права на резервное копирование перед открытием запрошенного файла.</span><span class="sxs-lookup"><span data-stu-id="918b4-187">**JetOpenFileInstance** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="918b4-188">Размер файла, который будет считаться этой функцией, может не соответствовать размеру файла на диске.</span><span class="sxs-lookup"><span data-stu-id="918b4-188">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="918b4-189">В Windows XP и более поздних выпусках дополнительные сведения могут быть добавлены к файлу базы данных, который используется ядром СУБД во время операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="918b4-189">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="918b4-190">Таким образом, приложение должно полагаться только на размер файла, возвращенный **жетопенфилеинстанце** , или на фактическое число байтов данных, возвращенных [жетреадфилеинстанце](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="918b4-190">As such, the application should only rely on the file size returned by **JetOpenFileInstance** or on the actual number of bytes of data returned by [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="918b4-191">Требования</span><span class="sxs-lookup"><span data-stu-id="918b4-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="918b4-192"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="918b4-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="918b4-193">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="918b4-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="918b4-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="918b4-195">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="918b4-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="918b4-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="918b4-197">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="918b4-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-198"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="918b4-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="918b4-199">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="918b4-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="918b4-200"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="918b4-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="918b4-201">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="918b4-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="918b4-202"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="918b4-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="918b4-203">Реализуется как <strong>жетопенфилеинстанцев</strong> (Юникод) и <strong>жетопенфилеинстанцеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="918b4-203">Implemented as <strong>JetOpenFileInstanceW</strong> (Unicode) and <strong>JetOpenFileInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="918b4-204">См. также:</span><span class="sxs-lookup"><span data-stu-id="918b4-204">See Also</span></span>

[<span data-ttu-id="918b4-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="918b4-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="918b4-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="918b4-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="918b4-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="918b4-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="918b4-208">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="918b4-208">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="918b4-209">жетбегинекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="918b4-209">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="918b4-210">жетклосефилеинстанце</span><span class="sxs-lookup"><span data-stu-id="918b4-210">JetCloseFileInstance</span></span>](./jetclosefileinstance-function.md)  
[<span data-ttu-id="918b4-211">жетжетаттачинфоинстанце</span><span class="sxs-lookup"><span data-stu-id="918b4-211">JetGetAttachInfoInstance</span></span>](./jetgetattachinfoinstance-function.md)  
[<span data-ttu-id="918b4-212">жетжетлогинфоинстанце</span><span class="sxs-lookup"><span data-stu-id="918b4-212">JetGetLogInfoInstance</span></span>](./jetgetloginfoinstance-function.md)  
[<span data-ttu-id="918b4-213">жетреадфилеинстанце</span><span class="sxs-lookup"><span data-stu-id="918b4-213">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="918b4-214">жетстопбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="918b4-214">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="918b4-215">жеттрункателогинстанце</span><span class="sxs-lookup"><span data-stu-id="918b4-215">JetTruncateLogInstance</span></span>](./jettruncateloginstance-function.md)
