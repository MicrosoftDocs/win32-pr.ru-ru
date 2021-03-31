---
description: Дополнительные сведения о функции Жетклосефиле
title: Функция Жетклосефиле
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423649"
---
# <a name="jetclosefile-function"></a><span data-ttu-id="940f1-103">Функция Жетклосефиле</span><span class="sxs-lookup"><span data-stu-id="940f1-103">JetCloseFile Function</span></span>


<span data-ttu-id="940f1-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="940f1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefile-function"></a><span data-ttu-id="940f1-105">Функция Жетклосефиле</span><span class="sxs-lookup"><span data-stu-id="940f1-105">JetCloseFile Function</span></span>

<span data-ttu-id="940f1-106">Функция **жетклосефиле** закрывает файл, Открытый в [жетопенфиле](./jetopenfile-function.md) , после извлечения данных из этого файла с помощью [жетреадфиле](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="940f1-106">The **JetCloseFile** function closes a file that was opened with [JetOpenFile](./jetopenfile-function.md) after the data from that file has been extracted using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="940f1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="940f1-107">Parameters</span></span>

<span data-ttu-id="940f1-108">*хффиле*</span><span class="sxs-lookup"><span data-stu-id="940f1-108">*hfFile*</span></span>

<span data-ttu-id="940f1-109">Описатель файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="940f1-109">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="940f1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="940f1-110">Return Value</span></span>

<span data-ttu-id="940f1-111">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="940f1-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="940f1-112">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="940f1-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="940f1-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="940f1-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="940f1-114">Описание</span><span class="sxs-lookup"><span data-stu-id="940f1-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="940f1-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="940f1-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="940f1-116">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="940f1-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940f1-117">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="940f1-117">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="940f1-118">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="940f1-118">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940f1-119">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="940f1-119">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="940f1-120">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="940f1-120">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="940f1-121">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="940f1-121">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940f1-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="940f1-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="940f1-123">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="940f1-123">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="940f1-124">Это может произойти для <strong>жетклосефиле</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="940f1-124">This can happen for <strong>JetCloseFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="940f1-125">Указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии),</span><span class="sxs-lookup"><span data-stu-id="940f1-125">The specified instance handle is invalid (Windows XP and later releases),</span></span></p></li>
<li><p><span data-ttu-id="940f1-126">Указанный описатель файла недопустим.</span><span class="sxs-lookup"><span data-stu-id="940f1-126">The specified file handle is invalid.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940f1-127">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="940f1-127">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="940f1-128">Не удалось выполнить операцию, так как не выполняется внешняя архивация.</span><span class="sxs-lookup"><span data-stu-id="940f1-128">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940f1-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="940f1-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="940f1-130">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="940f1-130">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940f1-131">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="940f1-131">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="940f1-132">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="940f1-132">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940f1-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="940f1-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="940f1-134">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="940f1-134">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940f1-135">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="940f1-135">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="940f1-136">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="940f1-136">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="940f1-137">При успешном выполнении маркер файла закрывается.</span><span class="sxs-lookup"><span data-stu-id="940f1-137">On success, the file handle is closed.</span></span> <span data-ttu-id="940f1-138">Если файл базы данных был закрыт, то связанный с ним файл исправления базы данных (если таковой имеется) уничтожается.</span><span class="sxs-lookup"><span data-stu-id="940f1-138">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="940f1-139">При сбое изменения не происходят.</span><span class="sxs-lookup"><span data-stu-id="940f1-139">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="940f1-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="940f1-140">Remarks</span></span>

<span data-ttu-id="940f1-141">В настоящее время ядро СУБД поддерживает только один открытый файл через [жетопенфиле](./jetopenfile-function.md) .</span><span class="sxs-lookup"><span data-stu-id="940f1-141">The database engine currently only supports one open file through [JetOpenFile](./jetopenfile-function.md) at a time.</span></span> <span data-ttu-id="940f1-142">Если маркер файла открыт с помощью [жетопенфиле](./jetopenfile-function.md) , его необходимо закрыть с помощью **жетклосефиле** , прежде чем можно будет открыть другой файл.</span><span class="sxs-lookup"><span data-stu-id="940f1-142">If a file handle is opened using [JetOpenFile](./jetopenfile-function.md) then it must be closed using **JetCloseFile** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="940f1-143">Требования</span><span class="sxs-lookup"><span data-stu-id="940f1-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="940f1-144"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="940f1-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="940f1-145">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="940f1-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940f1-146"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="940f1-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="940f1-147">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="940f1-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940f1-148"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="940f1-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="940f1-149">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="940f1-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940f1-150"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="940f1-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="940f1-151">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="940f1-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940f1-152"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="940f1-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="940f1-153">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="940f1-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="940f1-154">См. также:</span><span class="sxs-lookup"><span data-stu-id="940f1-154">See Also</span></span>

[<span data-ttu-id="940f1-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="940f1-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="940f1-156">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="940f1-156">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="940f1-157">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="940f1-157">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="940f1-158">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="940f1-158">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="940f1-159">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="940f1-159">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="940f1-160">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="940f1-160">JetStopService</span></span>](./jetstopservice-function.md)
