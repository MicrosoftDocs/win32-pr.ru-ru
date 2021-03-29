---
description: Дополнительные сведения о функции Жетпрепареупдате
title: Функция Жетпрепареупдате
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647711"
---
# <a name="jetprepareupdate-function"></a><span data-ttu-id="f975c-103">Функция Жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="f975c-103">JetPrepareUpdate Function</span></span>


<span data-ttu-id="f975c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f975c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprepareupdate-function"></a><span data-ttu-id="f975c-105">Функция Жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="f975c-105">JetPrepareUpdate Function</span></span>

<span data-ttu-id="f975c-106">Функция **жетпрепареупдате** является первой операцией при выполнении обновления для вставки новой записи или замены существующей записи новыми значениями.</span><span class="sxs-lookup"><span data-stu-id="f975c-106">The **JetPrepareUpdate** function is the first operation in performing an update, for the purposes of inserting a new record or replacing an existing record with new values.</span></span> <span data-ttu-id="f975c-107">Обновления выполняются путем вызова **жетпрепареупдате**, вызова [жетсетколумн](./jetsetcolumn-function.md) или [жетсетколумнс](./jetsetcolumns-function.md) ноль или более раз и, наконец, путем вызова [жетупдате](./jetupdate-function.md) для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="f975c-107">Updates are done by calling **JetPrepareUpdate**, then calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) zero or more times and finally by calling [JetUpdate](./jetupdate-function.md) to complete the operation.</span></span> <span data-ttu-id="f975c-108">**Жетпрепареупдате** и [жетупдате](./jetupdate-function.md) устанавливают границы для операции обновления и важны только для последнего состояния обновления записи, указанной в индексах.</span><span class="sxs-lookup"><span data-stu-id="f975c-108">**JetPrepareUpdate** and [JetUpdate](./jetupdate-function.md) set the boundaries for an update operation and are important in having only the final update state of a record entered into indexes.</span></span> <span data-ttu-id="f975c-109">Это более эффективно, но также требуется в случаях, когда данные должны соответствовать допустимому состоянию с использованием более чем в операции с набором столбцов.</span><span class="sxs-lookup"><span data-stu-id="f975c-109">This is both more efficient, but also required in cases where data must match a valid state through more than on set column operation.</span></span>

<span data-ttu-id="f975c-110">Существует несколько различных вариантов вставки или замены записей, и они более подробно описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="f975c-110">There are a few different options for inserting or replacing records and they are described in more detail below.</span></span>

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a><span data-ttu-id="f975c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f975c-111">Parameters</span></span>

<span data-ttu-id="f975c-112">*сесид*</span><span class="sxs-lookup"><span data-stu-id="f975c-112">*sesid*</span></span>

<span data-ttu-id="f975c-113">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f975c-113">The session to use for this call.</span></span>

<span data-ttu-id="f975c-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="f975c-114">*tableid*</span></span>

<span data-ttu-id="f975c-115">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f975c-115">The cursor to use for this call.</span></span>

<span data-ttu-id="f975c-116">*подготовить*</span><span class="sxs-lookup"><span data-stu-id="f975c-116">*prep*</span></span>

<span data-ttu-id="f975c-117">Параметры, которые можно использовать для подготовки к обновлению, в том числе следующие.</span><span class="sxs-lookup"><span data-stu-id="f975c-117">The options that can be used to prepare for an update, which include the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f975c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f975c-118">Value</span></span></p></th>
<th><p><span data-ttu-id="f975c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f975c-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f975c-120">JET_prepCancel</span><span class="sxs-lookup"><span data-stu-id="f975c-120">JET_prepCancel</span></span></p></td>
<td><p><span data-ttu-id="f975c-121">Этот флаг приводит к тому, что <strong>жетпрепареупдате</strong> отменяет обновление для данного курсора.</span><span class="sxs-lookup"><span data-stu-id="f975c-121">This flag causes <strong>JetPrepareUpdate</strong> to cancel the update for this cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-122">JET_prepInsert</span><span class="sxs-lookup"><span data-stu-id="f975c-122">JET_prepInsert</span></span></p></td>
<td><p><span data-ttu-id="f975c-123">Этот флаг заставляет курсор подготовиться к вставке новой записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-123">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="f975c-124">Все данные инициализируются в состояние по умолчанию для записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-124">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="f975c-125">Если в таблице есть столбец с автоматическим приращением, то эта запись назначается новому значению независимо от того, завершилось ли обновление в конечном итоге успешно, завершается сбоем или отменяется.</span><span class="sxs-lookup"><span data-stu-id="f975c-125">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-126">JET_prepInsertCopy</span><span class="sxs-lookup"><span data-stu-id="f975c-126">JET_prepInsertCopy</span></span></p></td>
<td><p><span data-ttu-id="f975c-127">Этот флаг заставляет курсор подготовиться к вставке копии существующей записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-127">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="f975c-128">При использовании этого параметра должна существовать текущая запись.</span><span class="sxs-lookup"><span data-stu-id="f975c-128">There must be a current record if this option is used.</span></span> <span data-ttu-id="f975c-129">Начальное состояние новой записи копируется из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-129">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="f975c-130">Длинные значения, хранящиеся за пределами записи, практически копируются.</span><span class="sxs-lookup"><span data-stu-id="f975c-130">Long values that are stored off-record are virtually copied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-131">JET_prepInsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="f975c-131">JET_prepInsertCopyDeleteOriginal</span></span></p></td>
<td><p><span data-ttu-id="f975c-132">Этот флаг заставляет курсор подготовиться к вставке той же записи, а также к удалению или исходной записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-132">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="f975c-133">Он используется в случаях, когда первичный ключ изменился.</span><span class="sxs-lookup"><span data-stu-id="f975c-133">It is used in cases in which the primary key has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-134">JET_prepReplace</span><span class="sxs-lookup"><span data-stu-id="f975c-134">JET_prepReplace</span></span></p></td>
<td><p><span data-ttu-id="f975c-135">Этот флаг заставляет курсор подготовиться к замене текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-135">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="f975c-136">Если таблица имеет столбец Version, то для столбца Version устанавливается следующее значение в последовательности.</span><span class="sxs-lookup"><span data-stu-id="f975c-136">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="f975c-137">Если это обновление не завершено, то значение версии в записи не изменится.</span><span class="sxs-lookup"><span data-stu-id="f975c-137">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="f975c-138">Для записи была снята блокировка обновления, чтобы другие сеансы не обновляли эту запись до завершения этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="f975c-138">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-139">JET_prepReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="f975c-139">JET_prepReplaceNoLock</span></span></p></td>
<td><p><span data-ttu-id="f975c-140">Этот флаг аналогичен JET_prepReplace, но блокировка не предпринимается, чтобы другие сеансы не обновляли эту запись.</span><span class="sxs-lookup"><span data-stu-id="f975c-140">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="f975c-141">Вместо этого этот сеанс может получить JET_errWriteConflict при вызове <a href="gg269288(v=exchg.10).md">жетупдате</a> для завершения обновления.</span><span class="sxs-lookup"><span data-stu-id="f975c-141">Instead, this session may receive JET_errWriteConflict when it calls <a href="gg269288(v=exchg.10).md">JetUpdate</a> to complete the update.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f975c-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f975c-142">Return Value</span></span>

<span data-ttu-id="f975c-143">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="f975c-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f975c-144">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f975c-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f975c-145">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f975c-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="f975c-146">Описание</span><span class="sxs-lookup"><span data-stu-id="f975c-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f975c-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f975c-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f975c-148">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f975c-148">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-149">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="f975c-149">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="f975c-150"><strong>Жетпрепареупдате</strong> был вызван с допустимым флагом для подготовки, но не JET_prepCancel, а курсор уже находится в состоянии готовности.</span><span class="sxs-lookup"><span data-stu-id="f975c-150"><strong>JetPrepareUpdate</strong> was called with a valid flag for prep but not JET_prepCancel and the cursor was already in the prepared state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-151">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f975c-151">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f975c-152">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="f975c-152">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-153">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f975c-153">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f975c-154">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="f975c-154">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f975c-155">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f975c-155">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f975c-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f975c-157">Данный флаг подготовки не является допустимым флагом.</span><span class="sxs-lookup"><span data-stu-id="f975c-157">The given prep flag is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f975c-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f975c-159">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="f975c-159">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-160">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="f975c-160">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f975c-161"><strong>Жетпрепареупдате</strong> был вызван для замены записи, которая содержит столбцы SLV.</span><span class="sxs-lookup"><span data-stu-id="f975c-161"><strong>JetPrepareUpdate</strong> was called to replace a record which had SLV columns.</span></span> <span data-ttu-id="f975c-162">Столбцы SLV.</span><span class="sxs-lookup"><span data-stu-id="f975c-162">SLV columns.</span></span> <span data-ttu-id="f975c-163">Обратите внимание, что столбцы SLV являются функцией, не предназначенной для общего использования.</span><span class="sxs-lookup"><span data-stu-id="f975c-163">Please note that SLV columns are a feature not intended for general usage.</span></span> <span data-ttu-id="f975c-164">Эта функция используется для поддержки инфраструктуры Microsoft Exchange и не предназначена для использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="f975c-164">This feature is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f975c-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f975c-166">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="f975c-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-167">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="f975c-167">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="f975c-168"><strong>Жетпрепареупдате</strong> был вызван с JET_prepCancel, но не смог откатить все изменения, внесенные в столбцы типа JET_coltypLongText и/или столбцов типа JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="f975c-168"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but could not rollback all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f975c-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f975c-170">Этот флаг нельзя использовать одновременно с одним сеансом из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="f975c-170">This flag cannot be used with the same session from more than one thread at the same time.</span></span> <span data-ttu-id="f975c-171">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f975c-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f975c-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f975c-173">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="f975c-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-174">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="f975c-174">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="f975c-175"><strong>Жетпрепареупдате</strong> был вызван с JET_prepCancel, но курсор не был в подготовленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="f975c-175"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f975c-176">При успешном завершении курсор меняется на подготовленное состояние для требуемого обновления или в случае JET_prepCancel курсор возвращается к неподготовленному состоянию, а все изменения отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="f975c-176">On success, the cursor is changed to the prepared state for the purpose of the desired update, or in the case of JET_prepCancel, the cursor is reverted to the non-prepared state and any changes are discarded.</span></span>

<span data-ttu-id="f975c-177">В случае сбоя состояние курсора остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="f975c-177">On failure, the cursor state is left unchanged.</span></span> <span data-ttu-id="f975c-178">Если сбой был JET_errRollbackError то состояние курсора меняется на неподготовленное, но не все изменения были отменены.</span><span class="sxs-lookup"><span data-stu-id="f975c-178">If the failure was JET_errRollbackError then the cursor state is changed to the non-prepared state but not all of the changes have been reverted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f975c-179">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f975c-179">Remarks</span></span>

<span data-ttu-id="f975c-180">Вставка копии записи является важной оптимизацией, когда записи совместно используют данные типа JET_coltypLongText и (или) JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="f975c-180">Inserting a copy of a record is an important optimization when records share data of type JET_coltypLongText and/or JET_coltypLongBinary.</span></span> <span data-ttu-id="f975c-181">Эти данные хранятся вне записи, когда она велика, и существует вероятность того, что несколько записей могут совместно использовать одно и то же физическое представление данных.</span><span class="sxs-lookup"><span data-stu-id="f975c-181">This data is stored off-record when large and it is possible for multiple records to share the same physical representation of the data.</span></span> <span data-ttu-id="f975c-182">В этом случае данные могут быть обновлены из любой записи, но это приведет к тому, что данные будут находиться в таком виде, что каждая запись будет иметь собственную копию.</span><span class="sxs-lookup"><span data-stu-id="f975c-182">In this case, the data can be updated from either record, but doing so will cause the data to be burst such that each record has its own copy.</span></span> <span data-ttu-id="f975c-183">Невозможно изменить данные в одной записи с помощью изменения из другой записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-183">It is not possible to change data in one record by a modification from another record.</span></span> <span data-ttu-id="f975c-184">Кроме того, невозможно заблокировать обновление одной записи с помощью обновления другой записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-184">Also, it is not possible to block an update of one record by an update of another record.</span></span> <span data-ttu-id="f975c-185">Это центральная функция ESE и известна как блокировка на уровне записи.</span><span class="sxs-lookup"><span data-stu-id="f975c-185">This is a central feature to ESE and is known as Record Level Locking.</span></span>

<span data-ttu-id="f975c-186">Операции [жетупдате](./jetupdate-function.md) , которые не удается оставить курсор в состоянии "подготовлено к обновлению".</span><span class="sxs-lookup"><span data-stu-id="f975c-186">[JetUpdate](./jetupdate-function.md) operations which fail leave the cursor in the update prepared state.</span></span> <span data-ttu-id="f975c-187">Это позволяет исправить некоторые ошибки, например неправильное значение столбца, не требуя повторного создания состояния обновления.</span><span class="sxs-lookup"><span data-stu-id="f975c-187">This is to permit correction to some errors, such as a wrong column value, without requiring the update state to be recreated.</span></span> <span data-ttu-id="f975c-188">Это означает, что во всех случаях, когда курсор отменяет обновление, он должен явным образом вызвать **жетпрепареупдате** с JET_prepCancel.</span><span class="sxs-lookup"><span data-stu-id="f975c-188">This means that in all cases where a cursor abandons an update, it must explicitly call **JetPrepareUpdate** with JET_prepCancel.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f975c-189">Требования</span><span class="sxs-lookup"><span data-stu-id="f975c-189">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f975c-190"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f975c-190"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f975c-191">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f975c-191">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-192"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f975c-192"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f975c-193">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f975c-193">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-194"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f975c-194"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f975c-195">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f975c-195">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f975c-196"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="f975c-196"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f975c-197">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f975c-197">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f975c-198"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="f975c-198"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f975c-199">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f975c-199">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f975c-200">См. также:</span><span class="sxs-lookup"><span data-stu-id="f975c-200">See Also</span></span>

[<span data-ttu-id="f975c-201">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f975c-201">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f975c-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f975c-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f975c-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f975c-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f975c-204">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="f975c-204">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="f975c-205">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="f975c-205">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="f975c-206">жетупдате</span><span class="sxs-lookup"><span data-stu-id="f975c-206">JetUpdate</span></span>](./jetupdate-function.md)
