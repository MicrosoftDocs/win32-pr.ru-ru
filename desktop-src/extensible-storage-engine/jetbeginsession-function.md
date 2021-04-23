---
description: Дополнительные сведения о функции Жетбегинсессион
title: Функция JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712871"
---
# <a name="jetbeginsession-function"></a><span data-ttu-id="fffae-103">Функция JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="fffae-103">JetBeginSession Function</span></span>


<span data-ttu-id="fffae-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fffae-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginsession-function"></a><span data-ttu-id="fffae-105">Функция JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="fffae-105">JetBeginSession Function</span></span>

<span data-ttu-id="fffae-106">Функция **жетбегинсессион** запускает сеанс и инициализирует и возвращает обработчик сеанса ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="fffae-106">The **JetBeginSession** function starts a session and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="fffae-107">Сеансы управляют всем доступом к базе данных и используются для управления областью транзакций.</span><span class="sxs-lookup"><span data-stu-id="fffae-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="fffae-108">Сеанс можно использовать для начала, фиксации или прерывания транзакций.</span><span class="sxs-lookup"><span data-stu-id="fffae-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="fffae-109">Сеанс также используется для присоединения, создания или открытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="fffae-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="fffae-110">Сеанс используется в качестве контекста для всех операций DDL и DML.</span><span class="sxs-lookup"><span data-stu-id="fffae-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="fffae-111">Чтобы увеличить параллелизм и параллельный доступ к базе данных, можно приступило к нескольким сеансам.</span><span class="sxs-lookup"><span data-stu-id="fffae-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a><span data-ttu-id="fffae-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fffae-112">Parameters</span></span>

<span data-ttu-id="fffae-113">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="fffae-113">*instance*</span></span>

<span data-ttu-id="fffae-114">Экземпляр базы данных, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="fffae-114">The database instance to use for this call.</span></span>

<span data-ttu-id="fffae-115">*псесид*</span><span class="sxs-lookup"><span data-stu-id="fffae-115">*psesid*</span></span>

<span data-ttu-id="fffae-116">Указатель на переменную, которую обработчик сеанса инициализирует при успешном возвращении.</span><span class="sxs-lookup"><span data-stu-id="fffae-116">Pointer to the variable that the session handle initializes on successful return.</span></span>

<span data-ttu-id="fffae-117">*сзусернаме*</span><span class="sxs-lookup"><span data-stu-id="fffae-117">*szUserName*</span></span>

<span data-ttu-id="fffae-118">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="fffae-118">This parameter is reserved.</span></span>

<span data-ttu-id="fffae-119">*сзпассворд*</span><span class="sxs-lookup"><span data-stu-id="fffae-119">*szPassword*</span></span>

<span data-ttu-id="fffae-120">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="fffae-120">This parameter is reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="fffae-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fffae-121">Return Value</span></span>

<span data-ttu-id="fffae-122">Эта функция позволяет возвратить любые [JET_ERR](./jet-err.md)s, определенные в этом API.</span><span class="sxs-lookup"><span data-stu-id="fffae-122">This function allows for the return of any [JET_ERR](./jet-err.md)s that are defined in this API.</span></span> <span data-ttu-id="fffae-123">Дополнительные сведения об ошибках Jet см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fffae-123">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fffae-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fffae-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="fffae-125">Описание</span><span class="sxs-lookup"><span data-stu-id="fffae-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fffae-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fffae-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fffae-127">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fffae-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fffae-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fffae-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fffae-129">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="fffae-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fffae-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fffae-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fffae-131">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="fffae-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="fffae-132">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="fffae-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fffae-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fffae-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fffae-134">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="fffae-134">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fffae-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fffae-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fffae-136">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="fffae-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fffae-137">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="fffae-137">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="fffae-138">Не удалось выполнить операцию, так как не удалось выделить память.</span><span class="sxs-lookup"><span data-stu-id="fffae-138">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fffae-139">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="fffae-139">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="fffae-140">Число сеансов, которые ядро позволит запустить, ограничено.</span><span class="sxs-lookup"><span data-stu-id="fffae-140">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="fffae-141">Это значение можно изменить с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с константой JET_paramMaxSessions.</span><span class="sxs-lookup"><span data-stu-id="fffae-141">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the JET_paramMaxSessions constant.</span></span> <span data-ttu-id="fffae-142">Число сеансов по умолчанию — 16.</span><span class="sxs-lookup"><span data-stu-id="fffae-142">The default number of sessions is 16.</span></span> <span data-ttu-id="fffae-143">Дополнительные сведения о JET_paramMaxSessions см. в разделе <a href="gg294139(v=exchg.10).md">системные параметры</a> .</span><span class="sxs-lookup"><span data-stu-id="fffae-143">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about JET_paramMaxSessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fffae-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fffae-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fffae-145">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="fffae-145">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fffae-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fffae-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fffae-147">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="fffae-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fffae-148">При успешном выполнении обработчик сеанса инициализируется и может использоваться для операций базы данных.</span><span class="sxs-lookup"><span data-stu-id="fffae-148">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="fffae-149">В случае сбоя отсутствуют доступные сеансы или не удалось инициализировать новый сеанс.</span><span class="sxs-lookup"><span data-stu-id="fffae-149">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fffae-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fffae-150">Remarks</span></span>

<span data-ttu-id="fffae-151">При использовании сеансов в разных потоках необходимо тщательное внимание.</span><span class="sxs-lookup"><span data-stu-id="fffae-151">Careful attention must be used when using sessions across different threads.</span></span> <span data-ttu-id="fffae-152">Сеанс отслеживает, какой поток использовался во время [жетбегинтрансактион](./jetbegintransaction-function.md), [жеткоммиттрансактион](./jetcommittransaction-function.md)или [жетроллбакк](./jetrollback-function.md), и при использовании в нескольких потоках с открытой транзакцией возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="fffae-152">A session tracks which thread it was used on during [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md), or [JetRollback](./jetrollback-function.md), and it will throw an error if used on multiple threads with an open transaction.</span></span> <span data-ttu-id="fffae-153">[Жетресетсессионконтекст](./jetresetsessioncontext-function.md), [жетсетсессионконтекст](./jetsetsessioncontext-function.md) может изменить это поведение.</span><span class="sxs-lookup"><span data-stu-id="fffae-153">The [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) can change this behavior.</span></span> <span data-ttu-id="fffae-154">Так как сеанс по-прежнему является сериализованным контекстом, и несколько операций с базой данных не могут выполняться одновременно в одном сеансе, только последовательно.</span><span class="sxs-lookup"><span data-stu-id="fffae-154">Since the session is still a serialized context, and multiple database operations cannot be performed on a single session concurrently, only serially.</span></span> <span data-ttu-id="fffae-155">Однако можно использовать несколько сеансов для достижения параллельного доступа к базе данных.</span><span class="sxs-lookup"><span data-stu-id="fffae-155">However, you can use multiple sessions to achieve concurrent database access.</span></span> <span data-ttu-id="fffae-156">Сеансы можно использовать внутри транзакции в потоках путем установки и сброса контекстов сеанса.</span><span class="sxs-lookup"><span data-stu-id="fffae-156">Sessions can be used inside a transaction across threads by setting and resetting the session contexts.</span></span>

<span data-ttu-id="fffae-157">Обработчик сеанса должен быть закрыт с помощью [жетендсессион](./jetendsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="fffae-157">The session handle should be closed with [JetEndSession](./jetendsession-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="fffae-158">Требования</span><span class="sxs-lookup"><span data-stu-id="fffae-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fffae-159"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="fffae-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fffae-160">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fffae-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fffae-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fffae-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fffae-162">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fffae-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fffae-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fffae-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fffae-164">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fffae-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fffae-165"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="fffae-165"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fffae-166">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fffae-166">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fffae-167"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="fffae-167"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fffae-168">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fffae-168">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fffae-169"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="fffae-169"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fffae-170">Реализуется как <strong>жетбегинсессионв</strong> (Юникод) и <strong>жетбегинсессиона</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fffae-170">Implemented as <strong>JetBeginSessionW</strong> (Unicode) and <strong>JetBeginSessionA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fffae-171">См. также:</span><span class="sxs-lookup"><span data-stu-id="fffae-171">See Also</span></span>

[<span data-ttu-id="fffae-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fffae-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fffae-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="fffae-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="fffae-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fffae-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fffae-175">жетбегинтрансактион</span><span class="sxs-lookup"><span data-stu-id="fffae-175">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="fffae-176">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="fffae-176">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="fffae-177">жетдупсессион</span><span class="sxs-lookup"><span data-stu-id="fffae-177">JetDupSession</span></span>](./jetdupsession-function.md)  
[<span data-ttu-id="fffae-178">жетендсессион</span><span class="sxs-lookup"><span data-stu-id="fffae-178">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="fffae-179">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="fffae-179">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="fffae-180">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="fffae-180">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="fffae-181">жетсетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="fffae-181">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="fffae-182">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="fffae-182">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="fffae-183">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="fffae-183">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
