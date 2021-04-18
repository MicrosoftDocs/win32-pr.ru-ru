---
description: Дополнительные сведения о функции JetGetLogInfoInstance2
title: Функция JetGetLogInfoInstance2
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f58a04c49a82604fb5ded09b6328e9e03df7963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693148"
---
# <a name="jetgetloginfoinstance2-function"></a><span data-ttu-id="f3b79-103">Функция JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="f3b79-103">JetGetLogInfoInstance2 Function</span></span>


<span data-ttu-id="f3b79-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f3b79-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance2-function"></a><span data-ttu-id="f3b79-105">Функция JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="f3b79-105">JetGetLogInfoInstance2 Function</span></span>

<span data-ttu-id="f3b79-106">Функция **JetGetLogInfoInstance2** используется во время резервного копирования, инициированного [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) , для запроса экземпляра имен файлов исправления базы данных и файлов журнала транзакций, которые должны стать частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f3b79-106">The **JetGetLogInfoInstance2** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="f3b79-107">Эти файлы впоследствии можно открыть с помощью [жетопенфиле](./jetopenfile-function.md) и прочитать с помощью [жетреадфиле](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="f3b79-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="f3b79-108">**Windows XP: JetGetLogInfoInstance2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f3b79-108">**Windows XP:  JetGetLogInfoInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="f3b79-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3b79-109">Parameters</span></span>

<span data-ttu-id="f3b79-110">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="f3b79-110">*instance*</span></span>

<span data-ttu-id="f3b79-111">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f3b79-111">The instance to use for this call.</span></span>

<span data-ttu-id="f3b79-112">Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="f3b79-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="f3b79-113">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f3b79-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="f3b79-114">Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="f3b79-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="f3b79-115">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="f3b79-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="f3b79-116">*сзз*</span><span class="sxs-lookup"><span data-stu-id="f3b79-116">*szz*</span></span>

<span data-ttu-id="f3b79-117">Выходной буфер, который получит список строк, заканчивающихся нулем, описывающих набор файлов исправления базы данных и файлов журнала транзакций, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f3b79-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="f3b79-118">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="f3b79-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="f3b79-119">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="f3b79-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="f3b79-120">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="f3b79-120">*cbMax*</span></span>

<span data-ttu-id="f3b79-121">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="f3b79-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="f3b79-122">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="f3b79-122">*pcbActual*</span></span>

<span data-ttu-id="f3b79-123">Получает фактический объем строковых данных, полученных в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="f3b79-123">Receives the actual amount of string data received in the output buffer.</span></span>

<span data-ttu-id="f3b79-124">*плогинфо*</span><span class="sxs-lookup"><span data-stu-id="f3b79-124">*pLogInfo*</span></span>

<span data-ttu-id="f3b79-125">Получает структурированные сведения о файлах журнала транзакций, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f3b79-125">Receives structured information on the transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="f3b79-126">Если этот параметр отсутствует, предполагается, что его значение равно NULL.</span><span class="sxs-lookup"><span data-stu-id="f3b79-126">When this parameter is not present, its value is presumed to be NULL.</span></span>

### <a name="return-value"></a><span data-ttu-id="f3b79-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3b79-127">Return Value</span></span>

<span data-ttu-id="f3b79-128">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="f3b79-128">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f3b79-129">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f3b79-129">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3b79-130">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f3b79-130">Return code</span></span></p></th>
<th><p><span data-ttu-id="f3b79-131">Описание</span><span class="sxs-lookup"><span data-stu-id="f3b79-131">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-132">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f3b79-132">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f3b79-133">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f3b79-133">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3b79-134">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="f3b79-134">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="f3b79-135">Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</span><span class="sxs-lookup"><span data-stu-id="f3b79-135">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="f3b79-136">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f3b79-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f3b79-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f3b79-138">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="f3b79-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3b79-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f3b79-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f3b79-140">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="f3b79-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f3b79-141">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f3b79-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-142">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="f3b79-142">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="f3b79-143">Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="f3b79-143">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="f3b79-144"><a href="gg294055(v=exchg.10).md">Жетжетлогинфо</a> возвращает эту ошибку, если в экземпляре имеются необработанные дескрипторы файлов, созданные с помощью <a href="gg269249(v=exchg.10).md">жетопенфиле</a> .</span><span class="sxs-lookup"><span data-stu-id="f3b79-144"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3b79-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f3b79-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f3b79-146">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="f3b79-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="f3b79-147">Это может произойти для <a href="gg294055(v=exchg.10).md">жетжетлогинфо</a> , если указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</span><span class="sxs-lookup"><span data-stu-id="f3b79-147">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-148">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="f3b79-148">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="f3b79-149">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="f3b79-149">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3b79-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f3b79-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f3b79-151">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="f3b79-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f3b79-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f3b79-153">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="f3b79-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3b79-154">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f3b79-154">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f3b79-155">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="f3b79-155">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-156">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f3b79-156">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f3b79-157">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="f3b79-157">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3b79-158">При успешном выполнении запрошенные сведения о наборе файлов исправления базы данных и журналов транзакций, которые должны быть частью набора файлов резервной копии, помещаются в выходные буферы там, где они предоставлены.</span><span class="sxs-lookup"><span data-stu-id="f3b79-158">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="f3b79-159">Конечный автомат резервного копирования будет дополнительно таким, что резервная копия файлов базы данных больше не разрешается.</span><span class="sxs-lookup"><span data-stu-id="f3b79-159">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="f3b79-160">Только файлы исправления базы данных и файлы журнала транзакций могут быть открыты для резервного копирования за пределами этой точки.</span><span class="sxs-lookup"><span data-stu-id="f3b79-160">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="f3b79-161">В случае сбоя состояние выходных буферов не определено.</span><span class="sxs-lookup"><span data-stu-id="f3b79-161">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="f3b79-162">Сбой приведет к отмене всего процесса резервного копирования для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f3b79-162">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f3b79-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3b79-163">Remarks</span></span>

<span data-ttu-id="f3b79-164">Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f3b79-164">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="f3b79-165">Приложение всегда должно предоставлять буфер для получения фактического размера этого списка и использовать эти сведения для определения усечения списка.</span><span class="sxs-lookup"><span data-stu-id="f3b79-165">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f3b79-166">Требования</span><span class="sxs-lookup"><span data-stu-id="f3b79-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-167"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f3b79-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f3b79-168">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f3b79-168">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3b79-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f3b79-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f3b79-170">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f3b79-170">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f3b79-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f3b79-172">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f3b79-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3b79-173"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="f3b79-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f3b79-174">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f3b79-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3b79-175"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="f3b79-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f3b79-176">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f3b79-176">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3b79-177"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="f3b79-177"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f3b79-178">Реализуется как <strong>JetGetLogInfoInstance2W</strong> (Юникод) и <strong>JetGetLogInfoInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f3b79-178">Implemented as <strong>JetGetLogInfoInstance2W</strong> (Unicode) and <strong>JetGetLogInfoInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f3b79-179">См. также:</span><span class="sxs-lookup"><span data-stu-id="f3b79-179">See Also</span></span>

[<span data-ttu-id="f3b79-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f3b79-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f3b79-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f3b79-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f3b79-182">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="f3b79-182">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="f3b79-183">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="f3b79-183">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="f3b79-184">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="f3b79-184">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="f3b79-185">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="f3b79-185">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="f3b79-186">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="f3b79-186">JetStopBackup</span></span>](./jetstopbackup-function.md)
