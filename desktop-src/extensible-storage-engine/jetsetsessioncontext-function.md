---
description: Дополнительные сведения о функции Жетсетсессионконтекст
title: Функция Жетсетсессионконтекст
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711202"
---
# <a name="jetsetsessioncontext-function"></a><span data-ttu-id="591a6-103">Функция Жетсетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="591a6-103">JetSetSessionContext Function</span></span>


<span data-ttu-id="591a6-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="591a6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsessioncontext-function"></a><span data-ttu-id="591a6-105">Функция Жетсетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="591a6-105">JetSetSessionContext Function</span></span>

<span data-ttu-id="591a6-106">Функция **жетсетсессионконтекст** связывает сеанс с текущим потоком, используя заданный маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="591a6-106">The **JetSetSessionContext** function associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="591a6-107">Эта ассоциация переопределяет требование к подсистеме по умолчанию, что транзакция для данного сеанса должна полностью выполняться в том же потоке.</span><span class="sxs-lookup"><span data-stu-id="591a6-107">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span>

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a><span data-ttu-id="591a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="591a6-108">Parameters</span></span>

<span data-ttu-id="591a6-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="591a6-109">*sesid*</span></span>

<span data-ttu-id="591a6-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="591a6-110">The session to use for this call.</span></span>

<span data-ttu-id="591a6-111">*улконтекст*</span><span class="sxs-lookup"><span data-stu-id="591a6-111">*ulContext*</span></span>

<span data-ttu-id="591a6-112">Уникальный идентификатор, с которым будет связан этот сеанс.</span><span class="sxs-lookup"><span data-stu-id="591a6-112">A unique identifier to which this session will be associated.</span></span>

### <a name="return-value"></a><span data-ttu-id="591a6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="591a6-113">Return Value</span></span>

<span data-ttu-id="591a6-114">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="591a6-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="591a6-115">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="591a6-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="591a6-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="591a6-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="591a6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="591a6-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="591a6-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="591a6-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="591a6-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="591a6-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="591a6-120">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="591a6-120">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="591a6-121">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="591a6-121">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="591a6-122">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="591a6-122">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="591a6-123">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="591a6-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="591a6-124"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="591a6-124"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="591a6-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="591a6-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="591a6-126">Один из предоставленных параметров содержит непредвиденное значение, или сочетание нескольких значений параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="591a6-126">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="591a6-127">Эта ошибка будет возвращена <strong>жетсетсессионконтекст</strong> при выполнении следующих условий:</span><span class="sxs-lookup"><span data-stu-id="591a6-127">This error will be returned by <strong>JetSetSessionContext</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="591a6-128"><em>улконтекст</em> имеет значение null</span><span class="sxs-lookup"><span data-stu-id="591a6-128"><em>ulContext</em> is NULL</span></span></p></li>
<li><p><span data-ttu-id="591a6-129"><em>улконтекст</em> -1</span><span class="sxs-lookup"><span data-stu-id="591a6-129"><em>ulContext</em> is -1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="591a6-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="591a6-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="591a6-131">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="591a6-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="591a6-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="591a6-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="591a6-133">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="591a6-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="591a6-134">JET_errSessionContextAlreadySet</span><span class="sxs-lookup"><span data-stu-id="591a6-134">JET_errSessionContextAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="591a6-135">Не удалось связать сеанс с текущим потоком, так как он уже связан с потоком.</span><span class="sxs-lookup"><span data-stu-id="591a6-135">The session could not be associated with the current thread because it has already been associated with a thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="591a6-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="591a6-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="591a6-137">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="591a6-137">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="591a6-138">Если эта функция завершится с ошибкой, сеанс будет связан с текущим потоком.</span><span class="sxs-lookup"><span data-stu-id="591a6-138">If this function succeeds, the session will be associated with the current thread.</span></span> <span data-ttu-id="591a6-139">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="591a6-139">No change to the database state will occur.</span></span>

<span data-ttu-id="591a6-140">Если эта функция завершается ошибкой, состояние сеанса остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="591a6-140">If this function fails, the session state will remain unchanged.</span></span> <span data-ttu-id="591a6-141">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="591a6-141">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="591a6-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="591a6-142">Remarks</span></span>

<span data-ttu-id="591a6-143">Сеанс обычно привязывается к определенному потоку на протяжении транзакции.</span><span class="sxs-lookup"><span data-stu-id="591a6-143">A session is usually bound to a specific thread for the duration of a transaction.</span></span> <span data-ttu-id="591a6-144">Такое поведение предназначено для того, чтобы помочь приложениям обнаруживать и предотвращать концептуально некорректное совместное использование одного сеанса в нескольких потоках.</span><span class="sxs-lookup"><span data-stu-id="591a6-144">This behavior is designed to help applications detect and prevent the conceptually ill-advised sharing of a single session amongst multiple threads.</span></span> <span data-ttu-id="591a6-145">Иногда эта простая проверка не работает с архитектурой приложения.</span><span class="sxs-lookup"><span data-stu-id="591a6-145">Sometimes, this simple check does not work with the application's architecture.</span></span> <span data-ttu-id="591a6-146">Например, если приложение размещает объекты на стороне сервера с помощью пула потоков, а транзакции охватывают несколько вызовов сервера к данному объекту, то эта защита может вызвать сбой некоторых из этих вызовов с JET_errSessionSharingViolation даже несмотря на то, что шаблон использования правильный.</span><span class="sxs-lookup"><span data-stu-id="591a6-146">For example, if the application is hosting server-side objects using a thread pool and transactions span multiple server calls to a given object then this protection may cause some of those calls to fail with JET_errSessionSharingViolation even though the usage pattern is correct.</span></span> <span data-ttu-id="591a6-147">Эта ситуация встречается для серверов COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="591a6-147">This situation is common for COM object servers.</span></span>

<span data-ttu-id="591a6-148">**Жетсетсессионконтекст** и [жетресетсессионконтекст](./jetresetsessioncontext-function.md) решают эту проблему, делая проверку общего доступа к сеансу более гибкой.</span><span class="sxs-lookup"><span data-stu-id="591a6-148">**JetSetSessionContext** and [JetResetSessionContext](./jetresetsessioncontext-function.md) solve this problem by making this session sharing check a little more flexible.</span></span> <span data-ttu-id="591a6-149">Когда приложение начинает выполнять ряд вызовов API ESE с помощью определенного сеанса, он сначала устанавливает для контекста сеанса заданное значение.</span><span class="sxs-lookup"><span data-stu-id="591a6-149">When the application starts to make a series of ESE API calls using a particular session, it first sets the session context to a given value.</span></span> <span data-ttu-id="591a6-150">Это действие связывает сеанс с вызывающим потоком.</span><span class="sxs-lookup"><span data-stu-id="591a6-150">This action associates the session to the calling thread.</span></span> <span data-ttu-id="591a6-151">В данном примере этот контекст может быть адресом объекта, который содержит обработчик сеанса JET.</span><span class="sxs-lookup"><span data-stu-id="591a6-151">In the given example, this context could be the address of the object that contains the JET session handle.</span></span> <span data-ttu-id="591a6-152">После вызова API ESE приложение сбрасывает контекст сеанса.</span><span class="sxs-lookup"><span data-stu-id="591a6-152">Once the ESE API calls have been made, the application resets the session context.</span></span> <span data-ttu-id="591a6-153">Это действие отменяет связь между сеансом и вызывающим потоком.</span><span class="sxs-lookup"><span data-stu-id="591a6-153">This action disassociates the session from the calling thread.</span></span> <span data-ttu-id="591a6-154">Объект и его сеанс могут затем использоваться другим потоком, даже если в сеансе есть активная транзакция.</span><span class="sxs-lookup"><span data-stu-id="591a6-154">The object and its session can then be used by another thread even if the session has an active transaction.</span></span>

<span data-ttu-id="591a6-155">Важно отметить, что перед открытием транзакции в этом сеансе необходимо вызвать **жетсетсессионконтекст** , иначе связь не будет работать.</span><span class="sxs-lookup"><span data-stu-id="591a6-155">It is important to note that **JetSetSessionContext** must be called prior to opening a transaction on that session or the association will not work.</span></span>

<span data-ttu-id="591a6-156">**Жетсетсессионконтекст** является потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="591a6-156">**JetSetSessionContext** is thread safe.</span></span> <span data-ttu-id="591a6-157">Несколько потоков могут попытаться установить контекст потока в одном сеансе одновременно, и только один из них будет выиграть.</span><span class="sxs-lookup"><span data-stu-id="591a6-157">Multiple threads can try to set a thread context on the same session at the same time and only one will win.</span></span> <span data-ttu-id="591a6-158">Этот факт может использоваться приложением как средство для выделения сеанса из пула без сохранения внешнего состояния выделения.</span><span class="sxs-lookup"><span data-stu-id="591a6-158">This fact can be used by the application as a means to allocate a session from a pool without storing external state about its allocation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="591a6-159">Требования</span><span class="sxs-lookup"><span data-stu-id="591a6-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="591a6-160"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="591a6-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="591a6-161">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="591a6-161">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="591a6-162"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="591a6-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="591a6-163">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="591a6-163">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="591a6-164"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="591a6-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="591a6-165">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="591a6-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="591a6-166"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="591a6-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="591a6-167">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="591a6-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="591a6-168"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="591a6-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="591a6-169">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="591a6-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="591a6-170">См. также:</span><span class="sxs-lookup"><span data-stu-id="591a6-170">See Also</span></span>

[<span data-ttu-id="591a6-171">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="591a6-171">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="591a6-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="591a6-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="591a6-173">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="591a6-173">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="591a6-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="591a6-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="591a6-175">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="591a6-175">JetStopService</span></span>](./jetstopservice-function.md)
