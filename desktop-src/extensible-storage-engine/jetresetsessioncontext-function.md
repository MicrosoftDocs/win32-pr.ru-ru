---
description: Дополнительные сведения о функции Жетресетсессионконтекст
title: Функция Жетресетсессионконтекст
TOCTitle: JetResetSessionContext Function
ms:assetid: 537a4753-b804-457a-9a13-53e8d1056eab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269250(v=EXCHG.10)
ms:contentKeyID: 32765552
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ee02050a9583aa67f50fbe53d710c352c196048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264773"
---
# <a name="jetresetsessioncontext-function"></a><span data-ttu-id="dad9c-103">Функция Жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="dad9c-103">JetResetSessionContext Function</span></span>


<span data-ttu-id="dad9c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dad9c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresetsessioncontext-function"></a><span data-ttu-id="dad9c-105">Функция Жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="dad9c-105">JetResetSessionContext Function</span></span>

<span data-ttu-id="dad9c-106">Функция **жетресетсессионконтекст** отменяет связь между сеансом и текущим потоком.</span><span class="sxs-lookup"><span data-stu-id="dad9c-106">The **JetResetSessionContext** function disassociates a session from the current thread.</span></span>

```cpp
    JET_ERR JET_API JetResetSessionContext(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="dad9c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dad9c-107">Parameters</span></span>

<span data-ttu-id="dad9c-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="dad9c-108">*sesid*</span></span>

<span data-ttu-id="dad9c-109">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="dad9c-109">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="dad9c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dad9c-110">Return Value</span></span>

<span data-ttu-id="dad9c-111">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="dad9c-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="dad9c-112">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dad9c-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dad9c-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dad9c-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="dad9c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="dad9c-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dad9c-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dad9c-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dad9c-116">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dad9c-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dad9c-117">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="dad9c-117">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="dad9c-118">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="dad9c-118">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="dad9c-119">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="dad9c-119">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dad9c-120">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="dad9c-120">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="dad9c-121">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="dad9c-121">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dad9c-122">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="dad9c-122">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="dad9c-123">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="dad9c-123">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dad9c-124">JET_errSessionContextNotSetByThisThread</span><span class="sxs-lookup"><span data-stu-id="dad9c-124">JET_errSessionContextNotSetByThisThread</span></span></p></td>
<td><p><span data-ttu-id="dad9c-125">Не удалось разосопоставить сеанс с текущим потоком, так как он связан с другим потоком.</span><span class="sxs-lookup"><span data-stu-id="dad9c-125">The session could not be disassociated from the current thread because it is associated with a different thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dad9c-126">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="dad9c-126">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="dad9c-127">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="dad9c-127">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dad9c-128">При успешном выполнении сеанс будет несвязанным с текущим потоком.</span><span class="sxs-lookup"><span data-stu-id="dad9c-128">On success, the session will be disassociated from the current thread.</span></span> <span data-ttu-id="dad9c-129">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dad9c-129">No change to the database state will occur.</span></span>

<span data-ttu-id="dad9c-130">В случае сбоя состояние сеанса останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="dad9c-130">On failure, the session state will remain unchanged.</span></span> <span data-ttu-id="dad9c-131">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dad9c-131">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="dad9c-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dad9c-132">Remarks</span></span>

<span data-ttu-id="dad9c-133">**Жетресетсессионконтекст** должен вызываться в том же потоке, который вызвал [жетсетсессионконтекст](./jetsetsessioncontext-function.md) для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="dad9c-133">**JetResetSessionContext** must be called on the same thread that called [JetSetSessionContext](./jetsetsessioncontext-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dad9c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="dad9c-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dad9c-135"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="dad9c-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dad9c-136">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="dad9c-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dad9c-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dad9c-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dad9c-138">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="dad9c-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dad9c-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dad9c-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dad9c-140">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="dad9c-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dad9c-141"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="dad9c-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dad9c-142">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dad9c-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dad9c-143"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="dad9c-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dad9c-144">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dad9c-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dad9c-145">См. также:</span><span class="sxs-lookup"><span data-stu-id="dad9c-145">See Also</span></span>

[<span data-ttu-id="dad9c-146">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="dad9c-146">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="dad9c-147">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dad9c-147">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dad9c-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dad9c-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dad9c-149">жетсетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="dad9c-149">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)
