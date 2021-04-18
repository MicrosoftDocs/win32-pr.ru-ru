---
description: Дополнительные сведения о функции Жетжеткурсоринфо
title: Функция Жетжеткурсоринфо
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656714"
---
# <a name="jetgetcursorinfo-function"></a><span data-ttu-id="4d086-103">Функция Жетжеткурсоринфо</span><span class="sxs-lookup"><span data-stu-id="4d086-103">JetGetCursorInfo Function</span></span>


<span data-ttu-id="4d086-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4d086-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcursorinfo-function"></a><span data-ttu-id="4d086-105">Функция Жетжеткурсоринфо</span><span class="sxs-lookup"><span data-stu-id="4d086-105">JetGetCursorInfo Function</span></span>

<span data-ttu-id="4d086-106">Функция **жетжеткурсоринфо** используется для определения того, что обновление текущей записи курсора приведет к конфликту записи, в зависимости от текущего состояния обновления записи.</span><span class="sxs-lookup"><span data-stu-id="4d086-106">The **JetGetCursorInfo** function is used to determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="4d086-107">Возможно, конфликт записи будет возвращен, даже если **жетжеткурсоринфо** возвращает JET_errSuccess, так как другой сеанс может обновить запись, прежде чем текущий сеанс сможет обновить ту же запись.</span><span class="sxs-lookup"><span data-stu-id="4d086-107">It is possible that a write conflict will ultimately be returned even if **JetGetCursorInfo** returns JET_errSuccess, because another session may update the record before the current session is able to update the same record.</span></span>

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="4d086-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d086-108">Parameters</span></span>

<span data-ttu-id="4d086-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="4d086-109">*sesid*</span></span>

<span data-ttu-id="4d086-110">Сеанс, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="4d086-110">The session that will be used for this call.</span></span>

<span data-ttu-id="4d086-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="4d086-111">*tableid*</span></span>

<span data-ttu-id="4d086-112">Курсор, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="4d086-112">The cursor that will be used for this call.</span></span>

<span data-ttu-id="4d086-113">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="4d086-113">*pvResult*</span></span>

<span data-ttu-id="4d086-114">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4d086-114">Reserved for future use.</span></span>

<span data-ttu-id="4d086-115">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="4d086-115">*cbMax*</span></span>

<span data-ttu-id="4d086-116">Значение должно быть равно 0 (нулю); в противном случае — неиспользуемое.</span><span class="sxs-lookup"><span data-stu-id="4d086-116">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="4d086-117">Он имеется для будущих функций.</span><span class="sxs-lookup"><span data-stu-id="4d086-117">It is present for future functionality.</span></span>

<span data-ttu-id="4d086-118">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="4d086-118">*InfoLevel*</span></span>

<span data-ttu-id="4d086-119">Значение должно быть равно 0 (нулю); в противном случае — неиспользуемое.</span><span class="sxs-lookup"><span data-stu-id="4d086-119">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="4d086-120">Он имеется для будущих функций.</span><span class="sxs-lookup"><span data-stu-id="4d086-120">It is present for future functionality.</span></span>

### <a name="return-value"></a><span data-ttu-id="4d086-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d086-121">Return Value</span></span>

<span data-ttu-id="4d086-122">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="4d086-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4d086-123">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4d086-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d086-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4d086-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="4d086-125">Описание</span><span class="sxs-lookup"><span data-stu-id="4d086-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d086-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4d086-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4d086-127">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4d086-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d086-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4d086-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4d086-129">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="4d086-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d086-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4d086-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4d086-131">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="4d086-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="4d086-132">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="4d086-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d086-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4d086-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4d086-134">Значение <em>кбмакс</em> не равно 0 (ноль) или <em>инфолевел</em> не равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="4d086-134">Either <em>cbMax</em> is not 0 (zero) or <em>InfoLevel</em> is not 0 (zero).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d086-135">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="4d086-135">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="4d086-136">Курсор в настоящий момент не находится в записи, и данные логической записи не могут быть возвращены в результате.</span><span class="sxs-lookup"><span data-stu-id="4d086-136">The cursor is not currently on a record and information on a logical record cannot be returned as a result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d086-137">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4d086-137">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4d086-138">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="4d086-138">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d086-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4d086-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4d086-140">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="4d086-140">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d086-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4d086-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4d086-142">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="4d086-142">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="4d086-143">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="4d086-143">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d086-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4d086-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4d086-145">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="4d086-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d086-146">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4d086-146">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4d086-147">Текущая запись курсора была обновлена другим сеансом, и обновление этой записи на этом сеансе приведет к конфликту записи.</span><span class="sxs-lookup"><span data-stu-id="4d086-147">The current record of the cursor has been updated by another session and an update of this record by this session will result in a write conflict.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4d086-148">При успешном выполнении эта операция не оказывает влияния на расположение курсора, но только указывает на то, что ни один другой сеанс не обновил эту запись в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="4d086-148">On success, this operation has no effect on the location of the cursor but only indicates that no other session has currently updated this record.</span></span>

<span data-ttu-id="4d086-149">При сбое, если возвращается отрицательный код ошибки, в курсор или базу данных ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="4d086-149">On failure, if a negative error code is returned there are no effects to the cursor or the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4d086-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d086-150">Remarks</span></span>

<span data-ttu-id="4d086-151">Эта операция не влияет на состояние курсора или данных.</span><span class="sxs-lookup"><span data-stu-id="4d086-151">This operation does not affect the state of the cursor or the data.</span></span> <span data-ttu-id="4d086-152">Он возвращает только код ошибки, описывающий, является ли обновление текущей записи вызывающим сеансом результатом JET_errWriteConflict или неизвестное значение для возвращения JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="4d086-152">It only returns an error code describing whether an update to the current record by the calling session is known to result in a JET_errWriteConflict, or is unknown to return JET_errWriteConflict.</span></span> <span data-ttu-id="4d086-153">Если другой сеанс уже обновил эту запись для использования, убедитесь, что обновление этой записи в этом сеансе приведет к конфликту записи.</span><span class="sxs-lookup"><span data-stu-id="4d086-153">If another session has already updated this record to use it is certain that an update of this record by this session will result in a write conflict.</span></span> <span data-ttu-id="4d086-154">Это будет иметь значение true, пока этот сеанс не зафиксирует или не произведет откат своих транзакций до уровня транзакций 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="4d086-154">This will be true until this session commits or rolls back its transactions to transaction level 0 (zero).</span></span> <span data-ttu-id="4d086-155">Однако если **жетжеткурсоринфо** возвращает JET_errSuccess, другой сеанс по-прежнему может обновить эту запись до текущего сеанса, и поэтому по-прежнему возможно, что обновление текущей записи на этом сеансе в текущей транзакции приведет к конфликту записи.</span><span class="sxs-lookup"><span data-stu-id="4d086-155">However, if **JetGetCursorInfo** returns JET_errSuccess, it is still possible for another session to update this record before the current session and thus it is still possible that an update of the current record by this session in its current transaction will result in a write conflict.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4d086-156">Требования</span><span class="sxs-lookup"><span data-stu-id="4d086-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d086-157"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="4d086-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4d086-158">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4d086-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d086-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4d086-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4d086-160">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4d086-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d086-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4d086-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4d086-162">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4d086-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d086-163"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="4d086-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4d086-164">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4d086-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d086-165"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="4d086-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4d086-166">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4d086-166">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4d086-167">См. также:</span><span class="sxs-lookup"><span data-stu-id="4d086-167">See Also</span></span>

[<span data-ttu-id="4d086-168">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4d086-168">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4d086-169">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4d086-169">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4d086-170">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4d086-170">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4d086-171">жетжетлокк</span><span class="sxs-lookup"><span data-stu-id="4d086-171">JetGetLock</span></span>](./jetgetlock-function.md)  
[<span data-ttu-id="4d086-172">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="4d086-172">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="4d086-173">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="4d086-173">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="4d086-174">жетупдате</span><span class="sxs-lookup"><span data-stu-id="4d086-174">JetUpdate</span></span>](./jetupdate-function.md)
