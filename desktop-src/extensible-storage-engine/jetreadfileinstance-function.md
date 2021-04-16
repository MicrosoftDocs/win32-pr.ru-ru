---
description: Дополнительные сведения о функции Жетреадфилеинстанце
title: Функция JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539970"
---
# <a name="jetreadfileinstance-function"></a><span data-ttu-id="75a7e-103">Функция JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="75a7e-103">JetReadFileInstance Function</span></span>


<span data-ttu-id="75a7e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="75a7e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfileinstance-function"></a><span data-ttu-id="75a7e-105">Функция JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="75a7e-105">JetReadFileInstance Function</span></span>

<span data-ttu-id="75a7e-106">Функция **жетреадфилеинстанце** извлекает содержимое файла, открытого с помощью функции [жетопенфилеинстанце](./jetopenfileinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="75a7e-106">The **JetReadFileInstance** function retrieves the contents of a file opened with the [JetOpenFileInstance](./jetopenfileinstance-function.md) function.</span></span>

<span data-ttu-id="75a7e-107">**Windows XP**:   **Жетреадфилеинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="75a7e-107">**Windows XP**:   **JetReadFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a><span data-ttu-id="75a7e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="75a7e-108">Parameters</span></span>

<span data-ttu-id="75a7e-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="75a7e-109">*instance*</span></span>

<span data-ttu-id="75a7e-110">Экземпляр, используемый для конкретного вызова API.</span><span class="sxs-lookup"><span data-stu-id="75a7e-110">The instance to use for a particular API call.</span></span>

<span data-ttu-id="75a7e-111">Обратите внимание, что для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="75a7e-111">Note that for Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="75a7e-112">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="75a7e-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="75a7e-113">Для Windows XP и более поздних выпусков можно вызвать вариант API, который не принимает этот параметр, только если ядро находится в устаревшем режиме (режим совместимости Windows 2000) в случаях, когда поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="75a7e-113">For Windows XP and later releases, you can call the API variant that does not accept this parameter only when the engine is in legacy mode (Windows 2000 compatibility mode) in cases where only one instance is supported.</span></span> <span data-ttu-id="75a7e-114">В противном случае операция завершится ошибкой и возвратит ошибку JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="75a7e-114">Otherwise, the operation will fail and return the JET_errRunningInMultiInstanceMode error.</span></span>

<span data-ttu-id="75a7e-115">*хффиле*</span><span class="sxs-lookup"><span data-stu-id="75a7e-115">*hfFile*</span></span>

<span data-ttu-id="75a7e-116">Описатель файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="75a7e-116">The handle of the file to be read.</span></span>

<span data-ttu-id="75a7e-117">*PV*</span><span class="sxs-lookup"><span data-stu-id="75a7e-117">*pv*</span></span>

<span data-ttu-id="75a7e-118">Выходной буфер, который будет принимать данные файла.</span><span class="sxs-lookup"><span data-stu-id="75a7e-118">The output buffer that will receive the file data.</span></span>

<span data-ttu-id="75a7e-119">*CB*</span><span class="sxs-lookup"><span data-stu-id="75a7e-119">*cb*</span></span>

<span data-ttu-id="75a7e-120">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="75a7e-120">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="75a7e-121">*пкб*</span><span class="sxs-lookup"><span data-stu-id="75a7e-121">*pcb*</span></span>

<span data-ttu-id="75a7e-122">Фактический объем получаемых файловых данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-122">The actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="75a7e-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75a7e-123">Return Value</span></span>

<span data-ttu-id="75a7e-124">Эта функция упрощает возврат любых [JET_ERR](./jet-err.md) типов данных, определенных в API-интерфейсе расширенного подсистемы хранилища (ESE).</span><span class="sxs-lookup"><span data-stu-id="75a7e-124">This function facilitates the return of any [JET_ERR](./jet-err.md) data types that are defined in the Extensible Storage Engine (ESE) API.</span></span> <span data-ttu-id="75a7e-125">Дополнительные сведения об ошибках JET см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="75a7e-125">For more information about JET errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75a7e-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="75a7e-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="75a7e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="75a7e-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="75a7e-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="75a7e-129">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="75a7e-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75a7e-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="75a7e-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="75a7e-131">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом функции <a href="gg269240(v=exchg.10).md">жетстопсервице</a> .</span><span class="sxs-lookup"><span data-stu-id="75a7e-131">The operation failed because the current external backup has been aborted by a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span> <span data-ttu-id="75a7e-132">Эта ошибка будет возвращена только в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="75a7e-132">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="75a7e-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="75a7e-134">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова функции <a href="gg269240(v=exchg.10).md">жетстопсервице</a> .</span><span class="sxs-lookup"><span data-stu-id="75a7e-134">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75a7e-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="75a7e-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="75a7e-136">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, произошла неустранимая ошибка, из-за которой доступ ко всем данным должен быть отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-136">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error requiring that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="75a7e-137">Эта ошибка будет возвращена только в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="75a7e-137">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-138">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="75a7e-138">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="75a7e-139">Один из указанных параметров содержит либо непредвиденное значение, либо значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="75a7e-139">One of the specified parameters contained either an unexpected value or a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="75a7e-140">Это может произойти для функции <strong>жетреадфилеинстанце</strong> при выполнении любого из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="75a7e-140">This can happen for the <strong>JetReadFileInstance</strong> function when any of the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="75a7e-141">Указан недопустимый обработчик экземпляра.</span><span class="sxs-lookup"><span data-stu-id="75a7e-141">The specified instance handle is invalid.</span></span> <span data-ttu-id="75a7e-142">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="75a7e-142">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="75a7e-143">Размер выходного буфера не кратен размеру страницы базы данных (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="75a7e-143">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="75a7e-144">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="75a7e-144">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="75a7e-145">Размер выходного буфера меньше трех страниц базы данных (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), и это первый вызов функции <strong>жетреадфилеинстанце</strong> для указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="75a7e-145">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), and this is the first call to the <strong>JetReadFileInstance</strong> function for the specified handle.</span></span> <span data-ttu-id="75a7e-146">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="75a7e-146">Windows XP and later Windows versions.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75a7e-147">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="75a7e-147">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="75a7e-148">Не удалось выполнить операцию, так как при чтении файла журнала транзакций обнаружено неустранимое повреждение данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-148">The operation failed because unrecoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="75a7e-149">Эта ошибка будет возвращена только в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="75a7e-149">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="75a7e-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="75a7e-151">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="75a7e-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75a7e-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="75a7e-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="75a7e-153">Невозможно выполнить операцию, так как экземпляр, связанный с этим сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="75a7e-153">It is not possible to complete the operation because the instance associated with this session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-154">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="75a7e-154">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="75a7e-155">Не удалось выполнить операцию, так как при чтении страницы базы данных из файла базы данных или файла исправления в файл обнаружено неустранимое повреждение данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-155">The operation failed because unrecoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75a7e-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="75a7e-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="75a7e-157">Невозможно выполнить операцию, так как в экземпляре, связанном с этим сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="75a7e-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-158">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="75a7e-158">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="75a7e-159">Не удалось выполнить операцию, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000) в случае, если поддерживается только один экземпляр, но несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="75a7e-159">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) in a case where only one instance is supported but multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75a7e-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="75a7e-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="75a7e-161">Невозможно выполнить операцию, так как работа экземпляра, связанного с этим сеансом, завершается.</span><span class="sxs-lookup"><span data-stu-id="75a7e-161">It is not possible to complete the operation because the instance associated with this session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75a7e-162">При успешном выполнении следующий фрагмент данных из файла будет считан в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="75a7e-162">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="75a7e-163">Также будет возвращено фактическое число полученных байтов.</span><span class="sxs-lookup"><span data-stu-id="75a7e-163">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="75a7e-164">Смещение файла, на котором будет выполняться следующее считывание, будет расширено этим объемом.</span><span class="sxs-lookup"><span data-stu-id="75a7e-164">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="75a7e-165">В случае сбоя состояние выходного буфера не определено.</span><span class="sxs-lookup"><span data-stu-id="75a7e-165">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="75a7e-166">Сбой приведет к отмене всего процесса резервного копирования для текущего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="75a7e-166">The failure will result in the cancellation of the entire backup process for the current instance.</span></span> <span data-ttu-id="75a7e-167">В Windows XP и более поздних версиях Windows резервная копия не будет отменена, если при чтении файла базы данных произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="75a7e-167">In Windows XP and later Windows versions, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="75a7e-168">Однако резервная копия этого файла базы данных по-прежнему будет отменена, и соответствующий маркер будет автоматически закрыт.</span><span class="sxs-lookup"><span data-stu-id="75a7e-168">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="75a7e-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75a7e-169">Remarks</span></span>

<span data-ttu-id="75a7e-170">Любой вызов функции **жетреадфилеинстанце** , выполненной с помощью маркера, который уже вернул все данные в базовом файле (например, если предыдущий вызов вернул меньшее число байтов, чем размер выходного буфера), всегда будет успешно выполнен, но возвратит нулевые байты данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-170">Any call to the **JetReadFileInstance** function made by using a handle that has already returned all the data in the underlying file (such as if a previous call returned fewer bytes than the size of the output buffer) will always succeed but will return zero bytes of data.</span></span>

<span data-ttu-id="75a7e-171">Для повышения производительности резервного копирования следует использовать большой выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="75a7e-171">You should use a large output buffer to maximize backup performance.</span></span> <span data-ttu-id="75a7e-172">Может потребоваться поэкспериментировать, чтобы найти оптимальный компромисс между потреблением ресурсов и пропускной способностью в конкретной ситуации.</span><span class="sxs-lookup"><span data-stu-id="75a7e-172">You might need to experiment to find the optimal tradeoff between resource consumption and throughput for a particular situation.</span></span> <span data-ttu-id="75a7e-173">В любом случае размер выходного буфера не должен превышать 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="75a7e-173">In any case, the output buffer should be no smaller than 64 KB.</span></span> <span data-ttu-id="75a7e-174">Указатель, передаваемый в **жетреадфилеинстанце** , должен быть согласован с границей страницы памяти (4 КБ или 8 КБ).</span><span class="sxs-lookup"><span data-stu-id="75a7e-174">The pointer that you pass to **JetReadFileInstance** must be aligned with a memory page boundary (either 4 KB or 8 KB).</span></span> <span data-ttu-id="75a7e-175">Это можно сделать, вызвав функцию **VirtualAlloc** .</span><span class="sxs-lookup"><span data-stu-id="75a7e-175">You can do this by calling the **VirtualAlloc** function.</span></span>

<span data-ttu-id="75a7e-176">Несколько одновременных вызовов **жетреадфилеинстанце** , выполненных с помощью одного и того же файла, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="75a7e-176">Multiple concurrent calls to **JetReadFileInstance** made by using the same file handle are not supported.</span></span> <span data-ttu-id="75a7e-177">Это означает, что невозможно поставить в очередь несколько буферов для параллельного чтения в одном и том же файле для достижения высокой последовательной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="75a7e-177">This means that it is not possible to queue several buffers for concurrent reading against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="75a7e-178">Вместо этого следует использовать один большой буфер.</span><span class="sxs-lookup"><span data-stu-id="75a7e-178">You should use a single large buffer instead.</span></span>

<span data-ttu-id="75a7e-179">Если вы настроили определенный экземпляр таким образом, что включена очистка страниц базы данных (см. параметр [JET_paramCircularLog](./transaction-log-parameters.md) в разделе [системные параметры](./extensible-storage-engine-system-parameters.md)), удаленные данные будут удалены из базы данных как побочный результат вызова **жетреадфилеинстанце** для файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-179">If you have configured a particular instance such that database page scrubbing is enabled (see the [JET_paramCircularLog](./transaction-log-parameters.md) parameter in [System Parameters](./extensible-storage-engine-system-parameters.md)), deleted data will be removed from the database as a side-effect of a call to **JetReadFileInstance** against the database file.</span></span>

<span data-ttu-id="75a7e-180">Очень важно понимать, как взаимодействуют резервные копии и повреждения данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-180">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="75a7e-181">Если ядро СУБД обнаружит повреждение данных во время резервного копирования, произойдет сбой резервного копирования затронутой базы данных или всего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="75a7e-181">If the database engine detects data corruption during a backup, it will fail the backup of either the affected database or the entire instance.</span></span> <span data-ttu-id="75a7e-182">Это осознанное решение по проектированию, предназначенное для защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-182">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="75a7e-183">Если ядро СУБД позволило успешно выполнить резервное копирование, при котором произошло повреждение данных, возможно, что в результате может быть отклонено старое, неповрежденное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="75a7e-183">If the database engine allowed a backup to succeed where data corruption was present, it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="75a7e-184">Это было бы неудачно, так как можно было бы исправить повреждение данных на динамическом экземпляре, восстановив эту резервную копию и воспроизводящую все файлы журнала транзакций для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-184">This would be unfortunate because then it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="75a7e-185">Этот сценарий с нулевой потерей данных предполагает, что циклическое ведение журнала не включено (см. [JET_paramCircularLog](./transaction-log-parameters.md) в разделе [системные параметры](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="75a7e-185">This zero-data-loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="75a7e-186">Также важно понимать, что случаи повреждения данных обычно сначала обнаруживаются во время потоковой архивации.</span><span class="sxs-lookup"><span data-stu-id="75a7e-186">It is also important to understand that cases of data corruption are usually first detected during streaming backup.</span></span> <span data-ttu-id="75a7e-187">Это обусловлено тем, что потоковая Архивация является единственным процессом, который ежедневно сканирует каждую отдельную страницу файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-187">This is because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="75a7e-188">Также вполне вероятно, что потоковая Архивация будет первым процессом для обнаружения ранних нарушений аппаратного сбоя, вызванных непостоянными ошибками повреждения данных, из-за объема данных, получаемых при резервном копировании, и скорости, с которой эти данные извлекаются.</span><span class="sxs-lookup"><span data-stu-id="75a7e-188">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors, because of both the amount of data retrieved by backup and the speed at which that data is retrieved.</span></span>

<span data-ttu-id="75a7e-189">Повреждение данных обнаруживается ядром СУБД с помощью блочных контрольных сумм.</span><span class="sxs-lookup"><span data-stu-id="75a7e-189">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="75a7e-190">Эти контрольные суммы задаются непосредственно перед записью страницы базы данных и проверяются на прочитанной странице базы данных.</span><span class="sxs-lookup"><span data-stu-id="75a7e-190">These checksums are set just before a database page write and are verified on a database page read.</span></span> <span data-ttu-id="75a7e-191">Эта схема позволяет ядру СУБД определить, что данные повреждены в некоторый момент, но не позволяют ядру СУБД определить источник этого повреждения.</span><span class="sxs-lookup"><span data-stu-id="75a7e-191">This scheme enables the database engine to determine that data has been corrupted at some point, but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="75a7e-192">Исторически экземпляры такого повреждения данных поступили из источников, отличных от самого ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="75a7e-192">Historically, instances of such data corruption have originated from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="75a7e-193">Требования</span><span class="sxs-lookup"><span data-stu-id="75a7e-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-194">Клиент</span><span class="sxs-lookup"><span data-stu-id="75a7e-194">Client</span></span></p></td>
<td><p><span data-ttu-id="75a7e-195">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="75a7e-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75a7e-196">Сервер</span><span class="sxs-lookup"><span data-stu-id="75a7e-196">Server</span></span></p></td>
<td><p><span data-ttu-id="75a7e-197">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="75a7e-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-198">Header</span><span class="sxs-lookup"><span data-stu-id="75a7e-198">Header</span></span></p></td>
<td><p><span data-ttu-id="75a7e-199">Объявляется в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="75a7e-199">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75a7e-200">Библиотека</span><span class="sxs-lookup"><span data-stu-id="75a7e-200">Library</span></span></p></td>
<td><p><span data-ttu-id="75a7e-201">Использует ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="75a7e-201">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75a7e-202">DLL</span><span class="sxs-lookup"><span data-stu-id="75a7e-202">DLL</span></span></p></td>
<td><p><span data-ttu-id="75a7e-203">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="75a7e-203">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="75a7e-204">См. также:</span><span class="sxs-lookup"><span data-stu-id="75a7e-204">See Also</span></span>

[<span data-ttu-id="75a7e-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="75a7e-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="75a7e-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="75a7e-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="75a7e-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="75a7e-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="75a7e-208">жетопенфилеинстанце</span><span class="sxs-lookup"><span data-stu-id="75a7e-208">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="75a7e-209">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="75a7e-209">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="75a7e-210">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="75a7e-210">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
