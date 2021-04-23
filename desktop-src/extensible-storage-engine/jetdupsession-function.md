---
description: Дополнительные сведения о функции Жетдупсессион
title: Функция Жетдупсессион
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912171"
---
# <a name="jetdupsession-function"></a><span data-ttu-id="eab29-103">Функция Жетдупсессион</span><span class="sxs-lookup"><span data-stu-id="eab29-103">JetDupSession Function</span></span>


<span data-ttu-id="eab29-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="eab29-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupsession-function"></a><span data-ttu-id="eab29-105">Функция Жетдупсессион</span><span class="sxs-lookup"><span data-stu-id="eab29-105">JetDupSession Function</span></span>

<span data-ttu-id="eab29-106">Функция **жетдупсессион** запускает сеанс, инициализирует и возвращает обработчик сеанса ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="eab29-106">The **JetDupSession** function starts a session, and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="eab29-107">Сеансы управляют всем доступом к базе данных и используются для управления областью транзакций.</span><span class="sxs-lookup"><span data-stu-id="eab29-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="eab29-108">Сеанс можно использовать для начала, фиксации или прерывания транзакций.</span><span class="sxs-lookup"><span data-stu-id="eab29-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="eab29-109">Сеанс также используется для присоединения, создания или открытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="eab29-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="eab29-110">Сеанс используется в качестве контекста для всех операций DDL и DML.</span><span class="sxs-lookup"><span data-stu-id="eab29-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="eab29-111">Чтобы увеличить параллелизм и параллельный доступ к базе данных, можно приступило к нескольким сеансам.</span><span class="sxs-lookup"><span data-stu-id="eab29-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

<span data-ttu-id="eab29-112">**Примечание** . Этот API будет работать во всех направлениях как [жетбегинсессион](./jetbeginsession-function.md) , вызываемый в экземпляре переданного сеанса.</span><span class="sxs-lookup"><span data-stu-id="eab29-112">**Note** This API will act in all ways as a [JetBeginSession](./jetbeginsession-function.md) called on the instance of the session passed in.</span></span> <span data-ttu-id="eab29-113">Эта функция не рекомендуется, [жетбегинсессион](./jetbeginsession-function.md) является предпочтительной.</span><span class="sxs-lookup"><span data-stu-id="eab29-113">This function is not recommended, [JetBeginSession](./jetbeginsession-function.md) is preferred.</span></span>

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a><span data-ttu-id="eab29-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="eab29-114">Parameters</span></span>

<span data-ttu-id="eab29-115">*сесид*</span><span class="sxs-lookup"><span data-stu-id="eab29-115">*sesid*</span></span>

<span data-ttu-id="eab29-116">Сеанс, используемый в качестве источника для дублирования или начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="eab29-116">The session to use as the source for duplicating or beginning the session.</span></span>

<span data-ttu-id="eab29-117">*псесид*</span><span class="sxs-lookup"><span data-stu-id="eab29-117">*psesid*</span></span>

<span data-ttu-id="eab29-118">Указатель на переменную, которую обработчик сеанса инициализирует при успешном возвращении.</span><span class="sxs-lookup"><span data-stu-id="eab29-118">A pointer to the variable that the session handle initializes on successful return.</span></span>

### <a name="return-value"></a><span data-ttu-id="eab29-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eab29-119">Return Value</span></span>

<span data-ttu-id="eab29-120">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="eab29-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="eab29-121">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eab29-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eab29-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="eab29-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="eab29-123">Описание</span><span class="sxs-lookup"><span data-stu-id="eab29-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eab29-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="eab29-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="eab29-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="eab29-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eab29-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="eab29-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="eab29-127">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="eab29-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eab29-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="eab29-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="eab29-129">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="eab29-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="eab29-130">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="eab29-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eab29-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="eab29-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="eab29-132">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="eab29-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eab29-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="eab29-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="eab29-134">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="eab29-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eab29-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="eab29-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="eab29-136">Не удалось выполнить операцию, так как не удалось выделить память.</span><span class="sxs-lookup"><span data-stu-id="eab29-136">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eab29-137">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="eab29-137">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="eab29-138">Число сеансов, которые ядро позволит запустить, ограничено.</span><span class="sxs-lookup"><span data-stu-id="eab29-138">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="eab29-139">Это значение можно изменить с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с константой <em>JET_paramMaxSessions</em> .</span><span class="sxs-lookup"><span data-stu-id="eab29-139">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the <em>JET_paramMaxSessions</em> constant.</span></span> <span data-ttu-id="eab29-140">Число сеансов по умолчанию — 16.</span><span class="sxs-lookup"><span data-stu-id="eab29-140">The default number of sessions is 16.</span></span> <span data-ttu-id="eab29-141">Дополнительные сведения о <em>JET_paramMaxSessions</em>см. в разделе <a href="gg294139(v=exchg.10).md">системные параметры</a> .</span><span class="sxs-lookup"><span data-stu-id="eab29-141">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about <em>JET_paramMaxSessions</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eab29-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="eab29-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="eab29-143">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="eab29-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eab29-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="eab29-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="eab29-145">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="eab29-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eab29-146">При успешном выполнении обработчик сеанса инициализируется и может использоваться для операций базы данных.</span><span class="sxs-lookup"><span data-stu-id="eab29-146">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="eab29-147">В случае сбоя отсутствуют доступные сеансы или не удалось инициализировать новый сеанс.</span><span class="sxs-lookup"><span data-stu-id="eab29-147">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="requirements"></a><span data-ttu-id="eab29-148">Требования</span><span class="sxs-lookup"><span data-stu-id="eab29-148">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eab29-149"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="eab29-149"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eab29-150">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="eab29-150">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eab29-151"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="eab29-151"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eab29-152">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="eab29-152">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eab29-153"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="eab29-153"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eab29-154">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="eab29-154">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eab29-155"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="eab29-155"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="eab29-156">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="eab29-156">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eab29-157"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="eab29-157"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="eab29-158">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="eab29-158">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="eab29-159">См. также:</span><span class="sxs-lookup"><span data-stu-id="eab29-159">See Also</span></span>

[<span data-ttu-id="eab29-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="eab29-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="eab29-161">жетбегинсессион</span><span class="sxs-lookup"><span data-stu-id="eab29-161">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="eab29-162">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="eab29-162">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="eab29-163">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="eab29-163">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="eab29-164">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="eab29-164">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
