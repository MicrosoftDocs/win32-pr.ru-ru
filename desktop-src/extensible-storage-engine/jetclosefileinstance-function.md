---
description: Дополнительные сведения о функции Жетклосефилеинстанце
title: Функция Жетклосефилеинстанце
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539983"
---
# <a name="jetclosefileinstance-function"></a><span data-ttu-id="a12d8-103">Функция Жетклосефилеинстанце</span><span class="sxs-lookup"><span data-stu-id="a12d8-103">JetCloseFileInstance Function</span></span>


<span data-ttu-id="a12d8-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a12d8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefileinstance-function"></a><span data-ttu-id="a12d8-105">Функция Жетклосефилеинстанце</span><span class="sxs-lookup"><span data-stu-id="a12d8-105">JetCloseFileInstance Function</span></span>

<span data-ttu-id="a12d8-106">Функция **жетклосефилеинстанце** закрывает файл, Открытый в [жетопенфилеинстанце](./jetopenfileinstance-function.md) , после извлечения данных из этого файла с помощью [жетреадфилеинстанце](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="a12d8-106">The **JetCloseFileInstance** function closes a file that was opened with [JetOpenFileInstance](./jetopenfileinstance-function.md) after the data from that file has been extracted using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="a12d8-107">**Windows XP: жетклосефилеинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a12d8-107">**Windows XP:  JetCloseFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="a12d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a12d8-108">Parameters</span></span>

<span data-ttu-id="a12d8-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="a12d8-109">*instance*</span></span>

<span data-ttu-id="a12d8-110">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="a12d8-110">The instance to use for this call.</span></span>

<span data-ttu-id="a12d8-111">Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a12d8-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="a12d8-112">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a12d8-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="a12d8-113">Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a12d8-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="a12d8-114">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="a12d8-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="a12d8-115">*хффиле*</span><span class="sxs-lookup"><span data-stu-id="a12d8-115">*hfFile*</span></span>

<span data-ttu-id="a12d8-116">Описатель файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="a12d8-116">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="a12d8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a12d8-117">Return Value</span></span>

<span data-ttu-id="a12d8-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="a12d8-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a12d8-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a12d8-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a12d8-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a12d8-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="a12d8-121">Описание</span><span class="sxs-lookup"><span data-stu-id="a12d8-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a12d8-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a12d8-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a12d8-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a12d8-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a12d8-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a12d8-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a12d8-125">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg294108(v=exchg.10).md">жетстопсервицеинстанце</a>.</span><span class="sxs-lookup"><span data-stu-id="a12d8-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a12d8-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a12d8-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a12d8-127">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="a12d8-127">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a12d8-128">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a12d8-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a12d8-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a12d8-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a12d8-130">Один из предоставленных параметров содержит непредвиденное значение, или сочетание нескольких значений параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="a12d8-130">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="a12d8-131">Это может произойти для <strong>жетклосефилеинстанце</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="a12d8-131">This can happen for <strong>JetCloseFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a12d8-132">Указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии)</span><span class="sxs-lookup"><span data-stu-id="a12d8-132">The specified instance handle is invalid (Windows XP and later releases)</span></span></p></li>
<li><p><span data-ttu-id="a12d8-133">Указанный описатель файла недопустим</span><span class="sxs-lookup"><span data-stu-id="a12d8-133">The specified file handle is invalid</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a12d8-134">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="a12d8-134">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="a12d8-135">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="a12d8-135">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a12d8-136">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a12d8-136">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a12d8-137">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="a12d8-137">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a12d8-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a12d8-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a12d8-139">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="a12d8-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a12d8-140">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a12d8-140">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a12d8-141">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="a12d8-141">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a12d8-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a12d8-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a12d8-143">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="a12d8-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a12d8-144">При успешном выполнении маркер файла закрывается.</span><span class="sxs-lookup"><span data-stu-id="a12d8-144">On success, the file handle is closed.</span></span> <span data-ttu-id="a12d8-145">Если файл базы данных был закрыт, то связанный с ним файл исправления базы данных (если таковой имеется) уничтожается.</span><span class="sxs-lookup"><span data-stu-id="a12d8-145">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="a12d8-146">При сбое изменения не происходят.</span><span class="sxs-lookup"><span data-stu-id="a12d8-146">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a12d8-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a12d8-147">Remarks</span></span>

<span data-ttu-id="a12d8-148">В настоящее время ядро СУБД поддерживает только один открытый файл через [жетопенфилеинстанце](./jetopenfileinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a12d8-148">The database engine currently only supports one open file through [JetOpenFileInstance](./jetopenfileinstance-function.md) at a time.</span></span> <span data-ttu-id="a12d8-149">Если маркер файла открыт с помощью [жетопенфилеинстанце](./jetopenfileinstance-function.md) , его необходимо закрыть с помощью **жетклосефилеинстанце** , прежде чем можно будет открыть другой файл.</span><span class="sxs-lookup"><span data-stu-id="a12d8-149">If a file handle is opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) then it must be closed using **JetCloseFileInstance** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a12d8-150">Требования</span><span class="sxs-lookup"><span data-stu-id="a12d8-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a12d8-151"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a12d8-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a12d8-152">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a12d8-152">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a12d8-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a12d8-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a12d8-154">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a12d8-154">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a12d8-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a12d8-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a12d8-156">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a12d8-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a12d8-157"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a12d8-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a12d8-158">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a12d8-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a12d8-159"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a12d8-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a12d8-160">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a12d8-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a12d8-161">См. также:</span><span class="sxs-lookup"><span data-stu-id="a12d8-161">See Also</span></span>

[<span data-ttu-id="a12d8-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a12d8-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a12d8-163">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="a12d8-163">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="a12d8-164">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a12d8-164">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a12d8-165">жетопенфилеинстанце</span><span class="sxs-lookup"><span data-stu-id="a12d8-165">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="a12d8-166">жетреадфилеинстанце</span><span class="sxs-lookup"><span data-stu-id="a12d8-166">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="a12d8-167">жетстопсервицеинстанце</span><span class="sxs-lookup"><span data-stu-id="a12d8-167">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
