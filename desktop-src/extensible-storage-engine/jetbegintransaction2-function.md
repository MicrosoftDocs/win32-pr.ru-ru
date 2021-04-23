---
description: Дополнительные сведения о функции JetBeginTransaction2
title: Функция JetBeginTransaction2
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d21bb88301a1f5d30df673a56032ef91c3847599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712582"
---
# <a name="jetbegintransaction2-function"></a><span data-ttu-id="12639-103">Функция JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="12639-103">JetBeginTransaction2 Function</span></span>


<span data-ttu-id="12639-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="12639-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction2-function"></a><span data-ttu-id="12639-105">Функция JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="12639-105">JetBeginTransaction2 Function</span></span>

<span data-ttu-id="12639-106">Функция **JetBeginTransaction2** заставляет сеанс войти в транзакцию и создать новую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="12639-106">The **JetBeginTransaction2** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="12639-107">Эту функцию можно вызвать несколько раз в одном сеансе, чтобы создать дополнительные точки сохранения.</span><span class="sxs-lookup"><span data-stu-id="12639-107">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="12639-108">Эти точки сохранения можно использовать для выборочного сохранения или отмены изменений в базе данных.</span><span class="sxs-lookup"><span data-stu-id="12639-108">These save points can be used to selectively to keep or discard changes to the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="12639-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="12639-109">Parameters</span></span>

<span data-ttu-id="12639-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="12639-110">*sesid*</span></span>

<span data-ttu-id="12639-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="12639-111">The session to use for this call.</span></span>

<span data-ttu-id="12639-112">*грбит*</span><span class="sxs-lookup"><span data-stu-id="12639-112">*grbit*</span></span>

<span data-ttu-id="12639-113">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="12639-113">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12639-114">Значение</span><span class="sxs-lookup"><span data-stu-id="12639-114">Value</span></span></p></th>
<th><p><span data-ttu-id="12639-115">Значение</span><span class="sxs-lookup"><span data-stu-id="12639-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12639-116">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="12639-116">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="12639-117">Транзакция не изменит базу данных.</span><span class="sxs-lookup"><span data-stu-id="12639-117">The transaction will not modify the database.</span></span> <span data-ttu-id="12639-118">При попытке обновления эта операция завершится ошибкой с JET_errTransReadOnly.</span><span class="sxs-lookup"><span data-stu-id="12639-118">If an update is attempted, that operation will fail with JET_errTransReadOnly.</span></span> <span data-ttu-id="12639-119">Этот параметр игнорируется, если он не запрашивается, если данный сеанс еще не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="12639-119">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="12639-120">Этот параметр доступен только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="12639-120">This option is only available as of Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="12639-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12639-121">Return Value</span></span>

<span data-ttu-id="12639-122">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="12639-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="12639-123">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="12639-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12639-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="12639-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="12639-125">Описание</span><span class="sxs-lookup"><span data-stu-id="12639-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12639-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="12639-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="12639-127">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="12639-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12639-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="12639-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="12639-129">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="12639-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12639-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="12639-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="12639-131">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="12639-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="12639-132">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="12639-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12639-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="12639-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="12639-134">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="12639-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12639-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="12639-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="12639-136">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="12639-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12639-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="12639-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="12639-138">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="12639-138">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="12639-139">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="12639-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12639-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="12639-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="12639-141">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="12639-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12639-142">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="12639-142">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="12639-143">Не удается запустить новую транзакцию, так как сеанс уже находится в максимально допустимой глубины точки сохранения в ядре СУБД.</span><span class="sxs-lookup"><span data-stu-id="12639-143">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="12639-144">При успешном выполнении указанный сеанс будет находиться внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="12639-144">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="12639-145">Если сеанс был ранее внутри транзакции, будет создана новая точка сохранения.</span><span class="sxs-lookup"><span data-stu-id="12639-145">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="12639-146">В случае сбоя состояние транзакции сеанса останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="12639-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="12639-147">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12639-147">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="12639-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12639-148">Remarks</span></span>

<span data-ttu-id="12639-149">Дополнительные сведения о работе транзакций см. в разделе [жетбегинтрансактион](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="12639-149">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="12639-150">Требования</span><span class="sxs-lookup"><span data-stu-id="12639-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12639-151"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="12639-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="12639-152">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="12639-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12639-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="12639-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="12639-154">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="12639-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12639-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="12639-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="12639-156">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="12639-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12639-157"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="12639-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="12639-158">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="12639-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12639-159"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="12639-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="12639-160">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="12639-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="12639-161">См. также:</span><span class="sxs-lookup"><span data-stu-id="12639-161">See Also</span></span>

[<span data-ttu-id="12639-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="12639-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="12639-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="12639-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="12639-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="12639-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="12639-165">жетбегинтрансактион</span><span class="sxs-lookup"><span data-stu-id="12639-165">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="12639-166">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="12639-166">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="12639-167">жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="12639-167">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="12639-168">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="12639-168">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="12639-169">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="12639-169">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="12639-170">жетсетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="12639-170">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="12639-171">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="12639-171">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
