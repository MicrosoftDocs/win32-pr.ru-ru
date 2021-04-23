---
description: Дополнительные сведения о функции Жетроллбакк
title: Функция Жетроллбакк
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eda0c8947e9609717bbb3f1a16999b450d7e4882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703084"
---
# <a name="jetrollback-function"></a><span data-ttu-id="fad50-103">Функция Жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="fad50-103">JetRollback Function</span></span>


<span data-ttu-id="fad50-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fad50-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrollback-function"></a><span data-ttu-id="fad50-105">Функция Жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="fad50-105">JetRollback Function</span></span>

<span data-ttu-id="fad50-106">Функция **жетроллбакк** отменяет изменения, внесенные в состояние базы данных, и возвращает ее в последнюю точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="fad50-106">The **JetRollback** function undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="fad50-107">**Жетроллбакк** также закроет курсоры, открытые во время точки сохранения.</span><span class="sxs-lookup"><span data-stu-id="fad50-107">**JetRollback** will also close any cursors opened during the save point.</span></span> <span data-ttu-id="fad50-108">Если внешняя точка сохранения отменена, сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="fad50-108">If the outermost save point is undone, the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="fad50-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fad50-109">Parameters</span></span>

<span data-ttu-id="fad50-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="fad50-110">*sesid*</span></span>

<span data-ttu-id="fad50-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="fad50-111">The session to use for this call.</span></span>

<span data-ttu-id="fad50-112">*грбит*</span><span class="sxs-lookup"><span data-stu-id="fad50-112">*grbit*</span></span>

<span data-ttu-id="fad50-113">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, в том числе ноль или более следующих:</span><span class="sxs-lookup"><span data-stu-id="fad50-113">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fad50-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fad50-114">Value</span></span></p></th>
<th><p><span data-ttu-id="fad50-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fad50-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fad50-116">JET_bitRollbackAll</span><span class="sxs-lookup"><span data-stu-id="fad50-116">JET_bitRollbackAll</span></span></p></td>
<td><p><span data-ttu-id="fad50-117">Этот параметр запрашивает отмену всех изменений, внесенных в состояние базы данных во время всех точек сохранения.</span><span class="sxs-lookup"><span data-stu-id="fad50-117">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="fad50-118">В результате сеанс выполнит выход из транзакции.</span><span class="sxs-lookup"><span data-stu-id="fad50-118">As a result, the session will exit the transaction.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fad50-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fad50-119">Return Value</span></span>

<span data-ttu-id="fad50-120">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="fad50-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fad50-121">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fad50-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fad50-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fad50-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="fad50-123">Описание</span><span class="sxs-lookup"><span data-stu-id="fad50-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fad50-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fad50-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fad50-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fad50-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad50-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fad50-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fad50-127">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="fad50-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad50-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fad50-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fad50-129">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="fad50-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="fad50-130">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="fad50-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad50-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fad50-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fad50-132">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="fad50-132">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad50-133">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="fad50-133">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="fad50-134">Не удалось выполнить операцию, так как данный сеанс не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="fad50-134">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad50-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fad50-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fad50-136">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="fad50-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad50-137">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="fad50-137">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="fad50-138">Откат изменений невозможен из-за неустранимой ошибки.</span><span class="sxs-lookup"><span data-stu-id="fad50-138">It was not possible to rollback the changes due to a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad50-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="fad50-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="fad50-140">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="fad50-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="fad50-141">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="fad50-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad50-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fad50-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fad50-143">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="fad50-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fad50-144">При успешном выполнении все изменения, внесенные в базу данных во время текущей точки сохранения для данного сеанса, будут отменены, и эта точка сохранения будет закончена.</span><span class="sxs-lookup"><span data-stu-id="fad50-144">On success, any changes made to the database during the current save point for the given session will be undone and that save point will be ended.</span></span> <span data-ttu-id="fad50-145">Если последняя точка сохранения сеанса была завершена, сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="fad50-145">If the last save point for the session was ended then the session will exit the transaction.</span></span>

<span data-ttu-id="fad50-146">В случае сбоя состояние транзакции сеанса останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="fad50-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="fad50-147">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fad50-147">No change to the database state will occur.</span></span> <span data-ttu-id="fad50-148">Сбой во время отката считается катастрофической ошибкой базы данных.</span><span class="sxs-lookup"><span data-stu-id="fad50-148">A failure during rollback is considered to be a catastrophic database error.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fad50-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fad50-149">Remarks</span></span>

<span data-ttu-id="fad50-150">Должен быть один вызов [жеткоммиттрансактион](./jetcommittransaction-function.md) или **жетроллбакк** для сопоставления каждого вызова [жетбегинтрансактион](./jetbegintransaction-function.md) для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="fad50-150">There must be one call to [JetCommitTransaction](./jetcommittransaction-function.md) or **JetRollback** to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

<span data-ttu-id="fad50-151">Если какие-либо курсоры были открыты (например, с помощью [жетопентабле](./jetopentable-function.md)) во время точки сохранения, для которой выполняется откат, этот курсор будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="fad50-151">If any cursors were opened (using [JetOpenTable](./jetopentable-function.md), for example) during a save point that is being rolled back then that cursor will be closed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fad50-152">Требования</span><span class="sxs-lookup"><span data-stu-id="fad50-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fad50-153"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="fad50-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fad50-154">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fad50-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad50-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fad50-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fad50-156">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fad50-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad50-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fad50-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fad50-158">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fad50-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad50-159"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="fad50-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fad50-160">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fad50-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad50-161"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="fad50-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fad50-162">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fad50-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fad50-163">См. также:</span><span class="sxs-lookup"><span data-stu-id="fad50-163">See Also</span></span>

[<span data-ttu-id="fad50-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fad50-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fad50-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fad50-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fad50-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fad50-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fad50-167">жетбегинтрансактион</span><span class="sxs-lookup"><span data-stu-id="fad50-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="fad50-168">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="fad50-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
