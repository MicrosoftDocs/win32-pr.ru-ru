---
description: Дополнительные сведения о функции Жетрегистеркаллбакк
title: Функция JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ca7559488182f2d687d5c678639e108792f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710999"
---
# <a name="jetregistercallback-function"></a><span data-ttu-id="981aa-103">Функция JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="981aa-103">JetRegisterCallback Function</span></span>


<span data-ttu-id="981aa-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="981aa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetregistercallback-function"></a><span data-ttu-id="981aa-105">Функция JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="981aa-105">JetRegisterCallback Function</span></span>

<span data-ttu-id="981aa-106">Функция **жетрегистеркаллбакк** позволяет приложению настроить ядро СУБД, чтобы выдать уведомления приложению о конкретных событиях.</span><span class="sxs-lookup"><span data-stu-id="981aa-106">The **JetRegisterCallback** function allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="981aa-107">Эти уведомления связаны с определенной таблицей и остаются в силе только до тех пор, пока экземпляр, содержащий таблицу, не завершит работу с помощью [жеттерм](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="981aa-107">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="981aa-108">**Windows XP: жетрегистеркаллбакк** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="981aa-108">**Windows XP:  JetRegisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="981aa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="981aa-109">Parameters</span></span>

<span data-ttu-id="981aa-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="981aa-110">*sesid*</span></span>

<span data-ttu-id="981aa-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="981aa-111">The session to use for this call.</span></span>

<span data-ttu-id="981aa-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="981aa-112">*tableid*</span></span>

<span data-ttu-id="981aa-113">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="981aa-113">The cursor to use for this call.</span></span>

<span data-ttu-id="981aa-114">*кбтип*</span><span class="sxs-lookup"><span data-stu-id="981aa-114">*cbtyp*</span></span>

<span data-ttu-id="981aa-115">Битовая маска, состоящая из причин обратного вызова, для которых приложение хочет получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="981aa-115">A bit mask composed of the callback reasons for which the application wishes to receive notifications.</span></span>

<span data-ttu-id="981aa-116">Чтобы создать эту битовую маску, можно просто или совместно использовать допустимые причины обратного вызова из перечисления [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="981aa-116">To create this bit mask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="981aa-117">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="981aa-117">*pCallback*</span></span>

<span data-ttu-id="981aa-118">Указатель функции на функцию обратного вызова для приложения.</span><span class="sxs-lookup"><span data-stu-id="981aa-118">The function pointer to the callback function for the application.</span></span>

<span data-ttu-id="981aa-119">*пвконтекст*</span><span class="sxs-lookup"><span data-stu-id="981aa-119">*pvContext*</span></span>

<span data-ttu-id="981aa-120">Задает указатель контекста, который будет передан функции обратного вызова для приложения.</span><span class="sxs-lookup"><span data-stu-id="981aa-120">Specifies a context pointer that will be given to the callback function for the application.</span></span>

<span data-ttu-id="981aa-121">*фкаллбаккид*</span><span class="sxs-lookup"><span data-stu-id="981aa-121">*phCallbackId*</span></span>

<span data-ttu-id="981aa-122">Возвращает маркер, который впоследствии можно использовать для отмены регистрации данной функции обратного вызова с помощью [жетунрегистеркаллбакк](./jetunregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="981aa-122">Returns a handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback](./jetunregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="981aa-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="981aa-123">Return Value</span></span>

<span data-ttu-id="981aa-124">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="981aa-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="981aa-125">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="981aa-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="981aa-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="981aa-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="981aa-127">Описание</span><span class="sxs-lookup"><span data-stu-id="981aa-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="981aa-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="981aa-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="981aa-129">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="981aa-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981aa-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="981aa-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="981aa-131">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="981aa-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="981aa-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="981aa-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="981aa-133">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="981aa-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="981aa-134">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="981aa-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981aa-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="981aa-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="981aa-136">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="981aa-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="981aa-137">Эта ошибка будет возвращена <strong>жетрегистеркаллбакк</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="981aa-137">This error will be returned by <strong>JetRegisterCallback</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="981aa-138"><em>кбтип</em> равен нулю,</span><span class="sxs-lookup"><span data-stu-id="981aa-138"><em>cbtyp</em> is zero,</span></span></p></li>
<li><p><span data-ttu-id="981aa-139"><em>пкаллбакк</em> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="981aa-139"><em>pCallback</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="981aa-140"><em>фкаллбаккид</em> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="981aa-140"><em>phCallbackId</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="981aa-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="981aa-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="981aa-142">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="981aa-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981aa-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="981aa-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="981aa-144">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="981aa-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="981aa-145">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="981aa-145">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="981aa-146">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="981aa-146">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="981aa-147">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="981aa-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981aa-148">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="981aa-148">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="981aa-149">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="981aa-149">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="981aa-150">При успешном выполнении указанный обратный вызов будет зарегистрирован для данной причины обратного вызова с таблицей, связанной с данным курсором.</span><span class="sxs-lookup"><span data-stu-id="981aa-150">On success, the specified callback will be registered for the given callback reasons with the table associated with the given cursor.</span></span> <span data-ttu-id="981aa-151">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="981aa-151">No change to the database state will occur.</span></span>

<span data-ttu-id="981aa-152">В случае сбоя обратный вызов не будет зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="981aa-152">On failure, the callback will not be registered.</span></span> <span data-ttu-id="981aa-153">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="981aa-153">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="981aa-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="981aa-154">Remarks</span></span>

<span data-ttu-id="981aa-155">Этот метод предоставляет приложению возможность связать временные обратные вызовы с таблицей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="981aa-155">This method provides a means for the application to associate volatile callbacks with a table in a database.</span></span> <span data-ttu-id="981aa-156">Если приложение желает связать сохраняемые обратные вызовы с таблицей в базе данных, необходимо передать обратный вызов для [JET_TABLECREATE](./jet-tablecreate-structure.md) с помощью [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="981aa-156">If the application wishes to associate persisted callbacks with a table in the database then it should pass the callback to [JET_TABLECREATE](./jet-tablecreate-structure.md) using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="981aa-157">Требования</span><span class="sxs-lookup"><span data-stu-id="981aa-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="981aa-158"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="981aa-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="981aa-159">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="981aa-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981aa-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="981aa-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="981aa-161">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="981aa-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="981aa-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="981aa-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="981aa-163">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="981aa-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981aa-164"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="981aa-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="981aa-165">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="981aa-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="981aa-166"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="981aa-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="981aa-167">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="981aa-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="981aa-168">См. также:</span><span class="sxs-lookup"><span data-stu-id="981aa-168">See Also</span></span>

[<span data-ttu-id="981aa-169">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="981aa-169">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="981aa-170">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="981aa-170">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="981aa-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="981aa-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="981aa-172">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="981aa-172">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="981aa-173">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="981aa-173">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="981aa-174">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="981aa-174">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="981aa-175">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="981aa-175">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="981aa-176">жеттерм</span><span class="sxs-lookup"><span data-stu-id="981aa-176">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="981aa-177">жетунрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="981aa-177">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)
