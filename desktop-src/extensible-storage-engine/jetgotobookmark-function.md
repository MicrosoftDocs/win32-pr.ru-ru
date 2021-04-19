---
description: Дополнительные сведения о функции Жетготобукмарк
title: Функция Жетготобукмарк
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703091"
---
# <a name="jetgotobookmark-function"></a><span data-ttu-id="b48e8-103">Функция Жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="b48e8-103">JetGotoBookmark Function</span></span>


<span data-ttu-id="b48e8-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b48e8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotobookmark-function"></a><span data-ttu-id="b48e8-105">Функция Жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="b48e8-105">JetGotoBookmark Function</span></span>

<span data-ttu-id="b48e8-106">Функция **жетготобукмарк** устанавливает курсор на запись индекса для записи, связанной с указанной закладкой.</span><span class="sxs-lookup"><span data-stu-id="b48e8-106">The **JetGotoBookmark** function positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="b48e8-107">Закладку можно использовать с любым индексом, определенным для таблицы.</span><span class="sxs-lookup"><span data-stu-id="b48e8-107">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="b48e8-108">Закладку для записи можно получить с помощью [жетжетбукмарк](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="b48e8-108">The bookmark for a record can be retrieved using [JetGetBookmark](./jetgetbookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a><span data-ttu-id="b48e8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b48e8-109">Parameters</span></span>

<span data-ttu-id="b48e8-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="b48e8-110">*sesid*</span></span>

<span data-ttu-id="b48e8-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="b48e8-111">The session to use for this call.</span></span>

<span data-ttu-id="b48e8-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b48e8-112">*tableid*</span></span>

<span data-ttu-id="b48e8-113">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="b48e8-113">The cursor to use for this call.</span></span>

<span data-ttu-id="b48e8-114">*пвбукмарк*</span><span class="sxs-lookup"><span data-stu-id="b48e8-114">*pvBookmark*</span></span>

<span data-ttu-id="b48e8-115">Буфер, содержащий закладку, используемую для позиционирования курсора.</span><span class="sxs-lookup"><span data-stu-id="b48e8-115">The buffer that contains the bookmark to use to position the cursor.</span></span>

<span data-ttu-id="b48e8-116">*кббукмарк*</span><span class="sxs-lookup"><span data-stu-id="b48e8-116">*cbBookmark*</span></span>

<span data-ttu-id="b48e8-117">Размер закладки в буфере.</span><span class="sxs-lookup"><span data-stu-id="b48e8-117">The size of the bookmark in the buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="b48e8-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b48e8-118">Return Value</span></span>

<span data-ttu-id="b48e8-119">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="b48e8-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b48e8-120">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b48e8-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b48e8-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b48e8-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="b48e8-122">Описание</span><span class="sxs-lookup"><span data-stu-id="b48e8-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b48e8-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b48e8-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b48e8-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b48e8-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b48e8-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b48e8-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b48e8-126">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="b48e8-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b48e8-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b48e8-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b48e8-128">Операция не может быть завершена, поскольку в экземпляре, связанном с сеансом, произошла неустранимая ошибка, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="b48e8-128">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b48e8-129"><strong>Windows XP:</strong>   Это возвращаемое значение было введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b48e8-129"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b48e8-130">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="b48e8-130">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="b48e8-131">Указана недопустимая закладка.</span><span class="sxs-lookup"><span data-stu-id="b48e8-131">The bookmark that was provided is invalid.</span></span> <span data-ttu-id="b48e8-132">Это могло произойти из-за того, что размер закладки равен нулю или указатель буфера закладки имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="b48e8-132">This might have occurred because the size of the bookmark is zero or the bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b48e8-133">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="b48e8-133">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="b48e8-134">Курсор находится на вторичном индексе, и не удалось найти запись индекса для записи, связанной с закладкой.</span><span class="sxs-lookup"><span data-stu-id="b48e8-134">The cursor is on a secondary index and no index entry could be found for the record that is associated with the bookmark.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b48e8-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b48e8-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b48e8-136">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="b48e8-136">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b48e8-137">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="b48e8-137">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="b48e8-138">Не удалось найти запись, связанную с закладкой.</span><span class="sxs-lookup"><span data-stu-id="b48e8-138">The record that is associated with the bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b48e8-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b48e8-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b48e8-140">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="b48e8-140">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b48e8-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b48e8-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b48e8-142">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="b48e8-142">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="b48e8-143"><strong>Windows XP:</strong>   Это возвращаемое значение было введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b48e8-143"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b48e8-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b48e8-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b48e8-145">Операция не может быть завершена, так как экземпляр, связанный с сеансом, завершает работу.</span><span class="sxs-lookup"><span data-stu-id="b48e8-145">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b48e8-146">Если эта функция выполнена, курсор будет размещен в записи индекса для записи, связанной с указанной закладкой.</span><span class="sxs-lookup"><span data-stu-id="b48e8-146">If this function succeeds, the cursor will be positioned at an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="b48e8-147">Если запись подготовлена к обновлению, это обновление будет отменено.</span><span class="sxs-lookup"><span data-stu-id="b48e8-147">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="b48e8-148">Если действует диапазон индексов, то диапазон индексов будет отменен.</span><span class="sxs-lookup"><span data-stu-id="b48e8-148">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="b48e8-149">Если для курсора был создан ключ поиска, этот ключ поиска будет удален.</span><span class="sxs-lookup"><span data-stu-id="b48e8-149">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="b48e8-150">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b48e8-150">No change to the database state will occur.</span></span>

<span data-ttu-id="b48e8-151">Если эта функция завершается ошибкой, то позиции курсора останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="b48e8-151">If this function fails, the position of the cursor will remain unchanged.</span></span> <span data-ttu-id="b48e8-152">Если запись подготовлена к обновлению, это обновление будет отменено.</span><span class="sxs-lookup"><span data-stu-id="b48e8-152">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="b48e8-153">Если действует диапазон индексов, то диапазон индексов будет отменен.</span><span class="sxs-lookup"><span data-stu-id="b48e8-153">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="b48e8-154">Если для курсора был создан ключ поиска, этот ключ поиска будет удален.</span><span class="sxs-lookup"><span data-stu-id="b48e8-154">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="b48e8-155">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b48e8-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b48e8-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b48e8-156">Remarks</span></span>

<span data-ttu-id="b48e8-157">Существует два способа использования закладки для размещения курсора в индексе.</span><span class="sxs-lookup"><span data-stu-id="b48e8-157">There are two ways to use a bookmark to position a cursor on an index.</span></span> <span data-ttu-id="b48e8-158">Первый — использовать закладку для непосредственного позиционирования записи.</span><span class="sxs-lookup"><span data-stu-id="b48e8-158">The first is to use the bookmark to position on the record directly.</span></span> <span data-ttu-id="b48e8-159">Это происходит, когда текущий индекс курсора является первичным индексом.</span><span class="sxs-lookup"><span data-stu-id="b48e8-159">This occurs when the current index of the cursor is the primary index.</span></span> <span data-ttu-id="b48e8-160">Эта методика работает потому, что закладка ESENT совпадает с первичным ключом связанной записи.</span><span class="sxs-lookup"><span data-stu-id="b48e8-160">This technique works because an ESENT bookmark is the same as the associated record's primary key.</span></span>

<span data-ttu-id="b48e8-161">Второй способ использовать закладку — это разместить его на записи во вторичном индексе, соответствующем записи, связанной с этой закладкой.</span><span class="sxs-lookup"><span data-stu-id="b48e8-161">The second way to use a bookmark is to position it on an entry in a secondary index that corresponds to the record that is associated with that bookmark.</span></span> <span data-ttu-id="b48e8-162">Во время этого процесса подсистема ищет фактическую запись, используя закладку в первичном индексе.</span><span class="sxs-lookup"><span data-stu-id="b48e8-162">During this process, the engine looks up the actual record using the bookmark on the primary index.</span></span> <span data-ttu-id="b48e8-163">Затем он использует данные записи и определение вторичного индекса, чтобы вычислить ключ во вторичном индексе, указывающем на запись.</span><span class="sxs-lookup"><span data-stu-id="b48e8-163">It then uses the record data and the secondary index definition to compute a key into the secondary index that points to the record.</span></span> <span data-ttu-id="b48e8-164">Затем курсор размещается на записи индекса для этого ключа.</span><span class="sxs-lookup"><span data-stu-id="b48e8-164">It then positions the cursor on the index entry for that key.</span></span> <span data-ttu-id="b48e8-165">Если курсор в данный момент находится во вторичном индексе над одним или несколькими многозначными ключевыми столбцами, курсор будет размещен в записи индекса, соответствующей первому многозначному значению каждого из этих ключевых столбцов.</span><span class="sxs-lookup"><span data-stu-id="b48e8-165">If the cursor is currently on a secondary index over one or more multi-valued key columns, the cursor will be positioned on the index entry corresponding to the first multi-value of each of those key columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b48e8-166">Требования</span><span class="sxs-lookup"><span data-stu-id="b48e8-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b48e8-167"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="b48e8-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b48e8-168">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b48e8-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b48e8-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b48e8-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b48e8-170">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b48e8-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b48e8-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b48e8-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b48e8-172">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b48e8-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b48e8-173"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="b48e8-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b48e8-174">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b48e8-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b48e8-175"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="b48e8-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b48e8-176">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b48e8-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b48e8-177">См. также:</span><span class="sxs-lookup"><span data-stu-id="b48e8-177">See Also</span></span>

[<span data-ttu-id="b48e8-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b48e8-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b48e8-179">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b48e8-179">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b48e8-180">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b48e8-180">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b48e8-181">жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="b48e8-181">JetGetBookmark</span></span>](./jetgetbookmark-function.md)
