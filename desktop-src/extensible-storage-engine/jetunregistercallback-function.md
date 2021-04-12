---
description: Дополнительные сведения о функции Жетунрегистеркаллбакк
title: Функция Жетунрегистеркаллбакк
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b342bab655e3cf1e3c1a5967410edb1c971af87b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423738"
---
# <a name="jetunregistercallback-function"></a><span data-ttu-id="2c0b8-103">Функция Жетунрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="2c0b8-103">JetUnregisterCallback Function</span></span>


<span data-ttu-id="2c0b8-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2c0b8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetunregistercallback-function"></a><span data-ttu-id="2c0b8-105">Функция Жетунрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="2c0b8-105">JetUnregisterCallback Function</span></span>

<span data-ttu-id="2c0b8-106">Функция **жетунрегистеркаллбакк** позволяет приложению настроить ядро СУБД на отмену отправки уведомлений приложению, как ранее было запрошено через [жетрегистеркаллбакк](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="2c0b8-106">The **JetUnregisterCallback** function enables the application to configure the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

<span data-ttu-id="2c0b8-107">**Windows XP:**  **Жетунрегистеркаллбакк** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-107">**Windows XP:**  **JetUnregisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="2c0b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c0b8-108">Parameters</span></span>

<span data-ttu-id="2c0b8-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="2c0b8-109">*sesid*</span></span>

<span data-ttu-id="2c0b8-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-110">The session to use for this call.</span></span>

<span data-ttu-id="2c0b8-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="2c0b8-111">*tableid*</span></span>

<span data-ttu-id="2c0b8-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-112">The cursor to use for this call.</span></span>

<span data-ttu-id="2c0b8-113">*кбтип*</span><span class="sxs-lookup"><span data-stu-id="2c0b8-113">*cbtyp*</span></span>

<span data-ttu-id="2c0b8-114">Битовая маска, состоящая из причин обратного вызова, которые приложение больше не хочет получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-114">A bitmask composed of the callback reasons that the application no longer wishes to receive notifications.</span></span>

<span data-ttu-id="2c0b8-115">Чтобы создать эту битовую маску, можно просто или совместно использовать допустимые причины обратного вызова из перечисления [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="2c0b8-115">To create this bitmask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="2c0b8-116">*хкаллбаккид*</span><span class="sxs-lookup"><span data-stu-id="2c0b8-116">*hCallbackId*</span></span>

<span data-ttu-id="2c0b8-117">Маркер зарегистрированного обратного вызова, возвращенный [жетрегистеркаллбакк](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="2c0b8-117">The handle of the registered callback that was returned by [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="2c0b8-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c0b8-118">Return Value</span></span>

<span data-ttu-id="2c0b8-119">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2c0b8-120">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2c0b8-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c0b8-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2c0b8-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="2c0b8-122">Описание</span><span class="sxs-lookup"><span data-stu-id="2c0b8-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c0b8-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2c0b8-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2c0b8-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c0b8-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2c0b8-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2c0b8-126">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c0b8-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2c0b8-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2c0b8-128">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="2c0b8-129"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-129"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c0b8-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2c0b8-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2c0b8-131">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c0b8-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2c0b8-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2c0b8-133">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c0b8-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="2c0b8-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="2c0b8-135">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-135">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="2c0b8-136"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-136"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c0b8-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2c0b8-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2c0b8-138">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-138">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c0b8-139">Если эта функция завершилась удачно, указанный обратный вызов будет отменен для заданной причины обратного вызова с таблицей, связанной с данным курсором.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-139">If this function succeeds, the specified callback will be unregistered for the given callback reasons with the table that is associated with the given cursor.</span></span> <span data-ttu-id="2c0b8-140">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-140">No change to the database state will occur.</span></span>

<span data-ttu-id="2c0b8-141">Если эта функция завершается с ошибкой, регистрация указанного обратного вызова не будет отменена.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-141">If this function fails, the specified callback will not be unregistered.</span></span> <span data-ttu-id="2c0b8-142">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-142">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2c0b8-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c0b8-143">Remarks</span></span>

<span data-ttu-id="2c0b8-144">Заданная битовая маска должна точно соответствовать битовой маске, указанной при регистрации обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-144">The given bitmask should exactly match the bitmask that is specified when registering the callback.</span></span> <span data-ttu-id="2c0b8-145">В настоящее время ядро СУБД не поддерживает удаление подмножества этих уведомлений и не возвращает ошибку при выполнении этой попытки.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-145">The database engine does not currently support removing a subset of these notifications and it does not return an error when this is attempted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2c0b8-146">Требования</span><span class="sxs-lookup"><span data-stu-id="2c0b8-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c0b8-147"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="2c0b8-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2c0b8-148">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-148">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c0b8-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2c0b8-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2c0b8-150">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-150">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c0b8-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2c0b8-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2c0b8-152">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c0b8-153"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="2c0b8-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2c0b8-154">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c0b8-155"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="2c0b8-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2c0b8-156">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2c0b8-157">См. также:</span><span class="sxs-lookup"><span data-stu-id="2c0b8-157">See Also</span></span>

[<span data-ttu-id="2c0b8-158">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="2c0b8-158">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="2c0b8-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2c0b8-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2c0b8-160">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="2c0b8-160">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="2c0b8-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2c0b8-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2c0b8-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2c0b8-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2c0b8-163">жетрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="2c0b8-163">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="2c0b8-164">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="2c0b8-164">JetStopService</span></span>](./jetstopservice-function.md)
