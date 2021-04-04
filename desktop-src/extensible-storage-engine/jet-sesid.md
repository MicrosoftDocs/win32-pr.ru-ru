---
description: 'Дополнительные сведения: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896977"
---
# <a name="jet_sesid"></a><span data-ttu-id="88530-103">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="88530-103">JET_SESID</span></span>


<span data-ttu-id="88530-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="88530-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_sesid"></a><span data-ttu-id="88530-105">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="88530-105">JET_SESID</span></span>

<span data-ttu-id="88530-106">**JET_SESID** тип данных содержит маркер сеанса, используемый для вызова API Jet.</span><span class="sxs-lookup"><span data-stu-id="88530-106">The **JET_SESID** data type contains a handle to the session to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a><span data-ttu-id="88530-107">Типы данных</span><span class="sxs-lookup"><span data-stu-id="88530-107">Data Types</span></span>

<span data-ttu-id="88530-108">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="88530-108">JET_SESID</span></span>

<span data-ttu-id="88530-109">Для указания недопустимого обработчика сеанса можно использовать **значение NULL** или [JET_sesidNil](./invalid-handle-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="88530-109">Either **NULL** or [JET_sesidNil](./invalid-handle-constants.md) can be used to indicate an invalid session handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="88530-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88530-110">Remarks</span></span>

<span data-ttu-id="88530-111">Сеанс — это контекст транзакции ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="88530-111">A session is the transaction context of the database engine.</span></span> <span data-ttu-id="88530-112">Его можно использовать для начала, фиксации или прерывания транзакций, влияющих на видимость и устойчивость изменений, внесенных в этом или других сеансах.</span><span class="sxs-lookup"><span data-stu-id="88530-112">It can be used to begin, commit, or abort transactions that affect the visibility and durability of changes that are made by this or other sessions.</span></span>

<span data-ttu-id="88530-113">Транзакцию можно запустить с помощью [жетбегинтрансактион](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="88530-113">A transaction can be started using [JetBeginTransaction](./jetbegintransaction-function.md).</span></span> <span data-ttu-id="88530-114">Сеанс можно создать с помощью [жетбегинсессион](./jetbeginsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="88530-114">A session may be created using [JetBeginSession](./jetbeginsession-function.md).</span></span> <span data-ttu-id="88530-115">Максимальное число сеансов, которые могут быть созданы за один раз, контролируется [JET_paramMaxSessions](./resource-parameters.md), которые можно настроить с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="88530-115">The maximum number of sessions that can be created at any one time is controlled by [JET_paramMaxSessions](./resource-parameters.md), which can be configured by means of [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="88530-116">Сеанс явно завершается вызовом [жетендсессион](./jetendsession-function.md) или неявно завершается вызовом [жеттерм](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="88530-116">A session is explicitly ended by a call to [JetEndSession](./jetendsession-function.md) or implicitly ended by a call to [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="88530-117">Каждый сеанс может использоваться только одним потоком за раз.</span><span class="sxs-lookup"><span data-stu-id="88530-117">Each session can only be used by one thread at a time.</span></span> <span data-ttu-id="88530-118">Кроме того, поведение обработчика по умолчанию заключается в ограничении использования сеанса тем же потоком с момента выполнения первого вызова [жетбегинтрансактион](./jetbegintransaction-function.md) до тех пор, пока не будет произведен соответствующий вызов [жеткоммиттрансактион](./jetcommittransaction-function.md) или [жетроллбакк](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="88530-118">In addition, the default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to [JetBeginTransaction](./jetbegintransaction-function.md) is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="88530-119">Это поведение можно изменить, чтобы удалить это второе ограничение, задав пользовательский контекст сеанса с помощью [жетсетсессионконтекст](./jetsetsessioncontext-function.md) и [жетресетсессионконтекст](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="88530-119">This behavior can be changed to remove this second restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="88530-120">Требования</span><span class="sxs-lookup"><span data-stu-id="88530-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88530-121"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="88530-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="88530-122">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="88530-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88530-123"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="88530-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="88530-124">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="88530-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88530-125"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="88530-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="88530-126">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="88530-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="88530-127">См. также:</span><span class="sxs-lookup"><span data-stu-id="88530-127">See Also</span></span>

[<span data-ttu-id="88530-128">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="88530-128">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="88530-129">жетбегинсессион</span><span class="sxs-lookup"><span data-stu-id="88530-129">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="88530-130">жетбегинтрансактион</span><span class="sxs-lookup"><span data-stu-id="88530-130">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="88530-131">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="88530-131">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="88530-132">жетендсессион</span><span class="sxs-lookup"><span data-stu-id="88530-132">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="88530-133">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="88530-133">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="88530-134">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="88530-134">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="88530-135">жетсетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="88530-135">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="88530-136">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="88530-136">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="88530-137">жеттерм</span><span class="sxs-lookup"><span data-stu-id="88530-137">JetTerm</span></span>](./jetterm-function.md)
