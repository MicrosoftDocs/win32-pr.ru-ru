---
description: Дополнительные сведения о функции Жетжетаттачинфоинстанце
title: Функция Жетжетаттачинфоинстанце
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28abf76632f147b6e909c1b8fb036062d5d3af74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910244"
---
# <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="e05e9-103">Функция Жетжетаттачинфоинстанце</span><span class="sxs-lookup"><span data-stu-id="e05e9-103">JetGetAttachInfoInstance Function</span></span>


<span data-ttu-id="e05e9-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e05e9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="e05e9-105">Функция Жетжетаттачинфоинстанце</span><span class="sxs-lookup"><span data-stu-id="e05e9-105">JetGetAttachInfoInstance Function</span></span>

<span data-ttu-id="e05e9-106">Функция **жетжетаттачинфоинстанце** используется во время резервного копирования, инициированного [жетбегинекстерналбаккупинстанце](./jetbeginexternalbackupinstance-function.md) , чтобы запросить экземпляр для имен файлов базы данных, которые должны стать частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e05e9-106">The **JetGetAttachInfoInstance** function is used during a backup initiated by [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="e05e9-107">Будут рассматриваться только те базы данных, которые в данный момент подключены к экземпляру с помощью [жетаттачдатабасе](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e05e9-107">Only databases that are currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="e05e9-108">Эти файлы впоследствии можно открыть с помощью [жетопенфилеинстанце](./jetopenfileinstance-function.md) и прочитать с помощью [жетреадфилеинстанце](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="e05e9-108">These files may subsequently be opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) and read using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="e05e9-109">**Windows XP: жетжетаттачинфоинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e05e9-109">**Windows XP:  JetGetAttachInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="e05e9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e05e9-110">Parameters</span></span>

<span data-ttu-id="e05e9-111">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="e05e9-111">*instance*</span></span>

<span data-ttu-id="e05e9-112">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e05e9-112">The instance to use for this call.</span></span>

<span data-ttu-id="e05e9-113">Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e05e9-113">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="e05e9-114">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e05e9-114">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="e05e9-115">Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e05e9-115">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="e05e9-116">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="e05e9-116">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="e05e9-117">*сзз*</span><span class="sxs-lookup"><span data-stu-id="e05e9-117">*szz*</span></span>

<span data-ttu-id="e05e9-118">Выходной буфер, который получает список строк, заканчивающихся нулем, описывающих набор файлов базы данных, который должен быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e05e9-118">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="e05e9-119">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="e05e9-119">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="e05e9-120">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="e05e9-120">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="e05e9-121">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="e05e9-121">*cbMax*</span></span>

<span data-ttu-id="e05e9-122">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="e05e9-122">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="e05e9-123">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="e05e9-123">*pcbActual*</span></span>

<span data-ttu-id="e05e9-124">Указатель на выходной буфер, который получает фактический объем строковых данных.</span><span class="sxs-lookup"><span data-stu-id="e05e9-124">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="e05e9-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e05e9-125">Return Value</span></span>

<span data-ttu-id="e05e9-126">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="e05e9-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e05e9-127">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e05e9-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e05e9-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e05e9-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="e05e9-129">Описание</span><span class="sxs-lookup"><span data-stu-id="e05e9-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e05e9-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e05e9-131">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e05e9-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05e9-132">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="e05e9-132">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="e05e9-133">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg269309(v=exchg.10).md">жетстопбаккупинстанце</a>.</span><span class="sxs-lookup"><span data-stu-id="e05e9-133">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="e05e9-134">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e05e9-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-135">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e05e9-135">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e05e9-136">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg294108(v=exchg.10).md">жетстопсервицеинстанце</a>.</span><span class="sxs-lookup"><span data-stu-id="e05e9-136">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05e9-137">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e05e9-137">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e05e9-138">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="e05e9-138">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e05e9-139">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e05e9-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-140">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="e05e9-140">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="e05e9-141">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="e05e9-141">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="e05e9-142"><strong>Жетжетаттачинфоинстанце</strong> возвращает эту ошибку, если текущая резервная копия не является полной резервной копией.</span><span class="sxs-lookup"><span data-stu-id="e05e9-142"><strong>JetGetAttachInfoInstance</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05e9-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e05e9-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e05e9-144">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="e05e9-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="e05e9-145">Это может произойти для <strong>жетжетаттачинфоинстанце</strong> , если указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="e05e9-145">This can happen for <strong>JetGetAttachInfoInstance</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-146">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="e05e9-146">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="e05e9-147">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="e05e9-147">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05e9-148">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e05e9-148">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e05e9-149">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="e05e9-149">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-150">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e05e9-150">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e05e9-151">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="e05e9-151">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05e9-152">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="e05e9-152">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="e05e9-153">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="e05e9-153">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e05e9-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e05e9-155">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="e05e9-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e05e9-156">При успешном выполнении запрошенные сведения о наборе файлов базы данных, которые должны быть частью набора файлов резервной копии, будут помещены в выходные буферы там, где они предоставлены.</span><span class="sxs-lookup"><span data-stu-id="e05e9-156">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="e05e9-157">В случае сбоя состояние выходных буферов не определено.</span><span class="sxs-lookup"><span data-stu-id="e05e9-157">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="e05e9-158">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e05e9-158">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e05e9-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e05e9-159">Remarks</span></span>

<span data-ttu-id="e05e9-160">Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e05e9-160">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="e05e9-161">Приложение всегда должно предоставлять буфер для получения фактического размера этого списка и использовать эти сведения для определения усечения списка.</span><span class="sxs-lookup"><span data-stu-id="e05e9-161">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e05e9-162">Требования</span><span class="sxs-lookup"><span data-stu-id="e05e9-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-163"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e05e9-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e05e9-164">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e05e9-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05e9-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e05e9-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e05e9-166">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e05e9-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e05e9-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e05e9-168">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e05e9-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05e9-169"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="e05e9-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e05e9-170">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e05e9-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05e9-171"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="e05e9-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e05e9-172">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e05e9-172">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05e9-173"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="e05e9-173"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e05e9-174">Реализуется как <strong>жетжетаттачинфоинстанцев</strong> (Юникод) и <strong>жетжетаттачинфоинстанцеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e05e9-174">Implemented as <strong>JetGetAttachInfoInstanceW</strong> (Unicode) and <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e05e9-175">См. также:</span><span class="sxs-lookup"><span data-stu-id="e05e9-175">See Also</span></span>

[<span data-ttu-id="e05e9-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e05e9-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e05e9-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e05e9-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e05e9-178">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="e05e9-178">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="e05e9-179">жетбегинекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="e05e9-179">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="e05e9-180">жетопенфилеинстанце</span><span class="sxs-lookup"><span data-stu-id="e05e9-180">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="e05e9-181">жетреадфилеинстанце</span><span class="sxs-lookup"><span data-stu-id="e05e9-181">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="e05e9-182">жетстопбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="e05e9-182">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="e05e9-183">жетстопсервицеинстанце</span><span class="sxs-lookup"><span data-stu-id="e05e9-183">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
