---
description: Дополнительные сведения о функции Жетендсессион
title: Функция Жетендсессион
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46bea6f5db745252a5e0ac6e8e03550dfead1b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346665"
---
# <a name="jetendsession-function"></a><span data-ttu-id="ef09f-103">Функция Жетендсессион</span><span class="sxs-lookup"><span data-stu-id="ef09f-103">JetEndSession Function</span></span>


<span data-ttu-id="ef09f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ef09f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendsession-function"></a><span data-ttu-id="ef09f-105">Функция Жетендсессион</span><span class="sxs-lookup"><span data-stu-id="ef09f-105">JetEndSession Function</span></span>

<span data-ttu-id="ef09f-106">Функция **жетендсессион** завершает сеанс и очищает и освобождает все ресурсы, связанные с указанным сеансом.</span><span class="sxs-lookup"><span data-stu-id="ef09f-106">The **JetEndSession** function ends the session, and cleans up and deallocates any resources associated with the specified session.</span></span>

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ef09f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef09f-107">Parameters</span></span>

<span data-ttu-id="ef09f-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="ef09f-108">*sesid*</span></span>

<span data-ttu-id="ef09f-109">Сеанс, который необходимо завершить.</span><span class="sxs-lookup"><span data-stu-id="ef09f-109">The session to end.</span></span> <span data-ttu-id="ef09f-110">Связанные ресурсы освобождаются по окончании сеанса.</span><span class="sxs-lookup"><span data-stu-id="ef09f-110">Associated resources are released when the session ends.</span></span>

<span data-ttu-id="ef09f-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="ef09f-111">*grbit*</span></span>

<span data-ttu-id="ef09f-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ef09f-112">Reserved.</span></span> <span data-ttu-id="ef09f-113">Этот параметр может содержать флаг JET_bitForceSessionClosed, но этот флаг зарезервирован и его установка не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="ef09f-113">This parameter can contain the JET_bitForceSessionClosed flag, but this flag is reserved and setting it has no effect.</span></span>

### <a name="return-value"></a><span data-ttu-id="ef09f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef09f-114">Return Value</span></span>

<span data-ttu-id="ef09f-115">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="ef09f-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ef09f-116">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ef09f-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef09f-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ef09f-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="ef09f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ef09f-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ef09f-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ef09f-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ef09f-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef09f-121">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ef09f-121">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ef09f-122">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="ef09f-122">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-123">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ef09f-123">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ef09f-124">Один из предоставленных параметров содержит непредвиденное значение, или сочетание нескольких значений параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="ef09f-124">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef09f-125">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="ef09f-125">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="ef09f-126">Сеанс не был допустимым сеансом JET.</span><span class="sxs-lookup"><span data-stu-id="ef09f-126">The session was not a valid JET session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ef09f-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ef09f-128">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="ef09f-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef09f-129">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="ef09f-129">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="ef09f-130">Не удалось выполнить операцию, так как не удалось выделить память.</span><span class="sxs-lookup"><span data-stu-id="ef09f-130">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-131">JET_errSessionInUse</span><span class="sxs-lookup"><span data-stu-id="ef09f-131">JET_errSessionInUse</span></span></p></td>
<td><p><span data-ttu-id="ef09f-132">Это означает, что сеанс использовался в другом потоке, или сеанс не был установлен или сброшен должным образом.</span><span class="sxs-lookup"><span data-stu-id="ef09f-132">This means the session was in use on another thread, or the session was not set or reset properly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef09f-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ef09f-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ef09f-134">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="ef09f-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="ef09f-135">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="ef09f-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-136">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="ef09f-136">JET_errOutOfBuffers</span></span></p></td>
<td><p><span data-ttu-id="ef09f-137">Системная ошибка, указывающая, что больше нет буферов.</span><span class="sxs-lookup"><span data-stu-id="ef09f-137">System error that indicates that there are no more buffers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef09f-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ef09f-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ef09f-139">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="ef09f-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ef09f-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ef09f-141">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="ef09f-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef09f-142">При успешном выполнении обработчик сеанса закрывается и недоступен, и все ресурсы, связанные с этим сеансом, очищаются.</span><span class="sxs-lookup"><span data-stu-id="ef09f-142">On success, the session handle is closed, and unavailable, and all resources related to this session are cleaned up.</span></span>

<span data-ttu-id="ef09f-143">В случае сбоя существует несколько дополнительных ошибок, которые могут возникнуть в процессе сортировки закрытия таблицы, закрытия курсора и отката транзакции.</span><span class="sxs-lookup"><span data-stu-id="ef09f-143">On failure, there are several additional errors that could occur as part of sort table close, cursor close, and transaction rollback.</span></span> <span data-ttu-id="ef09f-144">Эти ошибки довольно маловероятно и крайне маловероятно, если сеансы полностью не используются при вызове **жетендсессион** .</span><span class="sxs-lookup"><span data-stu-id="ef09f-144">These errors are fairly unlikely, and extremely unlikely if your sessions are completely not in use when **JetEndSession** is called.</span></span> <span data-ttu-id="ef09f-145">Эти ошибки будут возвращены, если часть сеанса не удалось правильно очистить.</span><span class="sxs-lookup"><span data-stu-id="ef09f-145">These errors will be returned if some part of the session was unable to be cleaned up properly.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ef09f-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef09f-146">Remarks</span></span>

<span data-ttu-id="ef09f-147">Этот API будет выполнять откат всех открытых транзакций (не зафиксированных на уровне 0).</span><span class="sxs-lookup"><span data-stu-id="ef09f-147">This API will rollback any open transactions (not committed to level 0).</span></span> <span data-ttu-id="ef09f-148">Кроме того, все курсоры, связанные с этим сеансом, и все созданные или открытые таблицы сортировки будут очищены.</span><span class="sxs-lookup"><span data-stu-id="ef09f-148">Also all cursors associated with this session, and any sort tables that have been created or opened will be cleaned up.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ef09f-149">Требования</span><span class="sxs-lookup"><span data-stu-id="ef09f-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-150"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="ef09f-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ef09f-151">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ef09f-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef09f-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ef09f-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ef09f-153">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ef09f-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ef09f-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ef09f-155">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ef09f-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef09f-156"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="ef09f-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ef09f-157">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ef09f-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef09f-158"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="ef09f-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ef09f-159">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ef09f-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ef09f-160">См. также:</span><span class="sxs-lookup"><span data-stu-id="ef09f-160">See Also</span></span>

[<span data-ttu-id="ef09f-161">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ef09f-161">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ef09f-162">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ef09f-162">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ef09f-163">жетбегинсессион</span><span class="sxs-lookup"><span data-stu-id="ef09f-163">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="ef09f-164">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="ef09f-164">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="ef09f-165">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="ef09f-165">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="ef09f-166">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="ef09f-166">JetStopService</span></span>](./jetstopservice-function.md)
