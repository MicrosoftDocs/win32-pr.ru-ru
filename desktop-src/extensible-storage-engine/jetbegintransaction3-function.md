---
description: Дополнительные сведения о функции JetBeginTransaction3
title: Функция JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710875"
---
# <a name="jetbegintransaction3-function"></a><span data-ttu-id="5d8c4-103">Функция JetBeginTransaction3</span><span class="sxs-lookup"><span data-stu-id="5d8c4-103">JetBeginTransaction3 Function</span></span>


<span data-ttu-id="5d8c4-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5d8c4-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="5d8c4-105">Функция **JetBeginTransaction3** заставляет сеанс войти в транзакцию и создать новую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-105">The **JetBeginTransaction3** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="5d8c4-106">Эту функцию можно вызвать несколько раз в одном сеансе, чтобы создать дополнительные точки сохранения.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-106">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="5d8c4-107">Эти точки сохранения можно использовать для выборочного сохранения или отмены изменений в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-107">These save points can be used to selectively to keep or discard changes to the database.</span></span>

<span data-ttu-id="5d8c4-108">Функция **JetBeginTransaction3** была введена в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-108">The **JetBeginTransaction3** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="5d8c4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d8c4-109">Parameters</span></span>

<span data-ttu-id="5d8c4-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="5d8c4-110">*sesid*</span></span>

<span data-ttu-id="5d8c4-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-111">The session to use for this call.</span></span>

<span data-ttu-id="5d8c4-112">*трксид*</span><span class="sxs-lookup"><span data-stu-id="5d8c4-112">*trxid*</span></span>

<span data-ttu-id="5d8c4-113">Необязательный идентификатор, предоставленный пользователем для идентификации транзакции.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-113">An optional identifier supplied by the user to identify the transaction.</span></span>

<span data-ttu-id="5d8c4-114">*грбит*</span><span class="sxs-lookup"><span data-stu-id="5d8c4-114">*grbit*</span></span>

<span data-ttu-id="5d8c4-115">Группа битов, которая указывает ноль или более значений параметров вызова, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-115">A group of bits that that specifies zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d8c4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5d8c4-116">Value</span></span></p></th>
<th><p><span data-ttu-id="5d8c4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5d8c4-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d8c4-118">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="5d8c4-118">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-119">Транзакция не изменит базу данных.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-119">The transaction will not modify the database.</span></span> <span data-ttu-id="5d8c4-120">При попытке обновления эта операция завершится ошибкой с JET_errTransReadOnly кодом ответа.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-120">If an update is attempted, that operation will fail with JET_errTransReadOnly response code.</span></span> <span data-ttu-id="5d8c4-121">Этот параметр игнорируется, если он не запрашивается, если данный сеанс еще не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-121">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="5d8c4-122">Этот параметр доступен в версиях операционной системы Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-122">This option is available in versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5d8c4-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d8c4-123">Return value</span></span>

<span data-ttu-id="5d8c4-124">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-124">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="5d8c4-125">Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5d8c4-125">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d8c4-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5d8c4-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="5d8c4-127">Описание</span><span class="sxs-lookup"><span data-stu-id="5d8c4-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d8c4-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5d8c4-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-129">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d8c4-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5d8c4-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-131">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова функции <a href="gg269240(v=exchg.10).md">жетстопсервице</a> .</span><span class="sxs-lookup"><span data-stu-id="5d8c4-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d8c4-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5d8c4-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-133">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5d8c4-134">Этот код возврата возвращается версиями Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-134">This return code is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d8c4-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5d8c4-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-136">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d8c4-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5d8c4-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-138">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-138">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d8c4-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5d8c4-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-140">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="5d8c4-141">Эта ошибка возвращается версиями Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-141">This error is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d8c4-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5d8c4-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-143">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d8c4-144">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="5d8c4-144">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="5d8c4-145">Не удается запустить новую транзакцию, так как сеанс уже находится в максимально допустимой глубины точки сохранения в ядре СУБД.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-145">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d8c4-146">При успешном выполнении указанный сеанс будет находиться внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-146">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="5d8c4-147">Если сеанс был ранее в рамках транзакции, будет создана новая точка сохранения.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-147">If the session was previously inside a transaction, a new save point will be created.</span></span>

<span data-ttu-id="5d8c4-148">В случае сбоя состояние транзакции сеанса останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-148">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="5d8c4-149">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-149">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5d8c4-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d8c4-150">Remarks</span></span>

<span data-ttu-id="5d8c4-151">Дополнительные сведения о работе транзакций см. в разделе [жетбегинтрансактион](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="5d8c4-151">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5d8c4-152">Требования</span><span class="sxs-lookup"><span data-stu-id="5d8c4-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d8c4-153"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="5d8c4-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5d8c4-154">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d8c4-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5d8c4-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5d8c4-156">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d8c4-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5d8c4-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5d8c4-158">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d8c4-159"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="5d8c4-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5d8c4-160">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d8c4-161"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="5d8c4-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5d8c4-162">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5d8c4-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d8c4-163">See also</span></span>

[<span data-ttu-id="5d8c4-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5d8c4-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5d8c4-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5d8c4-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5d8c4-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5d8c4-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5d8c4-167">жетбегинтрансактион</span><span class="sxs-lookup"><span data-stu-id="5d8c4-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="5d8c4-168">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="5d8c4-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="5d8c4-169">жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="5d8c4-169">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="5d8c4-170">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="5d8c4-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="5d8c4-171">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="5d8c4-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="5d8c4-172">жетсетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="5d8c4-172">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="5d8c4-173">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="5d8c4-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
