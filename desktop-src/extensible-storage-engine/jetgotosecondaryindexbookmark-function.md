---
description: Дополнительные сведения о функции Жетготосекондариндексбукмарк
title: Функция Жетготосекондариндексбукмарк
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998659"
---
# <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="1c198-103">Функция Жетготосекондариндексбукмарк</span><span class="sxs-lookup"><span data-stu-id="1c198-103">JetGotoSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="1c198-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1c198-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="1c198-105">Функция Жетготосекондариндексбукмарк</span><span class="sxs-lookup"><span data-stu-id="1c198-105">JetGotoSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="1c198-106">Функция **жетготосекондариндексбукмарк** устанавливает курсор на запись индекса, связанную с закладкой вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="1c198-106">The **JetGotoSecondaryIndexBookmark** function positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="1c198-107">Закладку вторичного индекса необходимо использовать с тем же индексом для той же таблицы, из которой она была первоначально извлечена.</span><span class="sxs-lookup"><span data-stu-id="1c198-107">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="1c198-108">Закладку вторичного индекса для записи индекса можно получить с помощью **жетготосекондариндексбукмарк**.</span><span class="sxs-lookup"><span data-stu-id="1c198-108">The secondary index bookmark for an index entry can be retrieved using **JetGotoSecondaryIndexBookmark**.</span></span>

<span data-ttu-id="1c198-109">**Windows XP:**  **Жетготосекондариндексбукмарк** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c198-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="1c198-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c198-110">Parameters</span></span>

<span data-ttu-id="1c198-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="1c198-111">*sesid*</span></span>

<span data-ttu-id="1c198-112">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="1c198-112">The session to use for this call.</span></span>

<span data-ttu-id="1c198-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="1c198-113">*tableid*</span></span>

<span data-ttu-id="1c198-114">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="1c198-114">The cursor to use for this call.</span></span>

<span data-ttu-id="1c198-115">*пвсекондарикэй*</span><span class="sxs-lookup"><span data-stu-id="1c198-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="1c198-116">Буфер, содержащий вторичный ключ, используемый для позиционирования курсора.</span><span class="sxs-lookup"><span data-stu-id="1c198-116">The buffer that contains the secondary key to use to position the cursor.</span></span>

<span data-ttu-id="1c198-117">*кбсекондарикэй*</span><span class="sxs-lookup"><span data-stu-id="1c198-117">*cbSecondaryKey*</span></span>

<span data-ttu-id="1c198-118">Размер вторичного ключа в буфере.</span><span class="sxs-lookup"><span data-stu-id="1c198-118">The size of the secondary key in the buffer.</span></span>

<span data-ttu-id="1c198-119">*пвпримарибукмарк*</span><span class="sxs-lookup"><span data-stu-id="1c198-119">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="1c198-120">Буфер, содержащий закладку первичного ключа, используемую для позиционирования курсора.</span><span class="sxs-lookup"><span data-stu-id="1c198-120">The buffer that contains the primary key bookmark to use to position the cursor.</span></span>

<span data-ttu-id="1c198-121">*кбпримарибукмарк*</span><span class="sxs-lookup"><span data-stu-id="1c198-121">*cbPrimaryBookmark*</span></span>

<span data-ttu-id="1c198-122">Размер закладки первичного ключа в буфере.</span><span class="sxs-lookup"><span data-stu-id="1c198-122">The size of the primary key bookmark in the buffer.</span></span>

<span data-ttu-id="1c198-123">*грбит*</span><span class="sxs-lookup"><span data-stu-id="1c198-123">*grbit*</span></span>

<span data-ttu-id="1c198-124">Группа битов, которая задает ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="1c198-124">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c198-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1c198-125">Value</span></span></p></th>
<th><p><span data-ttu-id="1c198-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1c198-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c198-127">JET_bitBookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="1c198-127">JET_bitBookmarkPermitVirtualCurrency</span></span></p></td>
<td><p><span data-ttu-id="1c198-128">В случае, если запись индекса больше не может быть найдена, курсор будет расположен слева, где была найдена Эта запись индекса.</span><span class="sxs-lookup"><span data-stu-id="1c198-128">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="1c198-129">Операция по-прежнему завершится ошибкой с JET_errRecordDeleted; Тем не менее, можно перейти к следующей или предыдущей записи индекса относительно записи индекса, которая сейчас отсутствует.</span><span class="sxs-lookup"><span data-stu-id="1c198-129">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1c198-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c198-130">Return Value</span></span>

<span data-ttu-id="1c198-131">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="1c198-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1c198-132">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1c198-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c198-133">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1c198-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="1c198-134">Описание</span><span class="sxs-lookup"><span data-stu-id="1c198-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c198-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1c198-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1c198-136">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1c198-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c198-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1c198-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1c198-138">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="1c198-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c198-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1c198-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1c198-140">Операция не может быть завершена, так как в экземпляре, связанном с сеансом, произошла неустранимая ошибка, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="1c198-140">The operation cannot complete because is because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1c198-141"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c198-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c198-142">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="1c198-142">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="1c198-143">Указана недопустимая закладка вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="1c198-143">The secondary index bookmark that was provided was invalid.</span></span> <span data-ttu-id="1c198-144">Эта ошибка могла произойти из-за того, что вторичный ключ равен нулю или указатель буфера вторичного ключа имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c198-144">This error might have occurred because the secondary key is zero or the secondary key buffer pointer is <strong>NULL</strong>.</span></span> <span data-ttu-id="1c198-145">Эта ошибка возникает из-за того, что</span><span class="sxs-lookup"><span data-stu-id="1c198-145">This error occurs because</span></span></p>
<ul>
<li><p><span data-ttu-id="1c198-146">Текущий вторичный индекс не имеет ограничения уникальности, а размер указанной закладки равен нулю.</span><span class="sxs-lookup"><span data-stu-id="1c198-146">The current secondary index does not have a uniqueness constraint and the size of the provided bookmark is zero.</span></span></p></li>
<li><p><span data-ttu-id="1c198-147">Указатель буфера закладки имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c198-147">The bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c198-148">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="1c198-148">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="1c198-149">Курсор в данный момент не находится во вторичном индексе.</span><span class="sxs-lookup"><span data-stu-id="1c198-149">The cursor is not currently on a secondary index.</span></span> <span data-ttu-id="1c198-150">Не имеет смысла переходить к закладке вторичного индекса, если в данный момент курсор не использует вторичный индекс.</span><span class="sxs-lookup"><span data-stu-id="1c198-150">It is not meaningful to go to a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="1c198-151"><a href="gg294053(v=exchg.10).md">Жетготобукмарк</a> следует использовать, если курсор не находится на вторичном индексе.</span><span class="sxs-lookup"><span data-stu-id="1c198-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c198-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1c198-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1c198-153">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="1c198-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c198-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="1c198-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="1c198-155">Не удалось найти запись индекса, связанную с закладкой вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="1c198-155">The index entry that is associated with the secondary index bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c198-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1c198-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1c198-157">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="1c198-157">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c198-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1c198-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1c198-159">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="1c198-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="1c198-160"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c198-160"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c198-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1c198-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1c198-162">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="1c198-162">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c198-163">Если эта функция выполнена, курсор будет размещен в записи индекса, связанной с закладкой дополнительного индекса.</span><span class="sxs-lookup"><span data-stu-id="1c198-163">If this function succeeds, the cursor will be positioned at an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="1c198-164">Если запись подготовлена к обновлению, это обновление будет отменено.</span><span class="sxs-lookup"><span data-stu-id="1c198-164">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="1c198-165">Если действует диапазон индексов, то диапазон индексов будет отменен.</span><span class="sxs-lookup"><span data-stu-id="1c198-165">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="1c198-166">Если для использования курсора был создан ключ поиска, этот ключ поиска будет удален.</span><span class="sxs-lookup"><span data-stu-id="1c198-166">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="1c198-167">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c198-167">No change to the database state will occur.</span></span>

<span data-ttu-id="1c198-168">Если эта функция завершается ошибкой, то позицию курсора остается неизменной, если не будет возвращен JET_errRecordDeleted и не будет указан JET_bitBookmarkPermitVirtualCurrency.</span><span class="sxs-lookup"><span data-stu-id="1c198-168">If this function fails, the position of the cursor remains unchanged unless JET_errRecordDeleted is returned and JET_bitBookmarkPermitVirtualCurrency is specified.</span></span> <span data-ttu-id="1c198-169">В этом случае курсор будет размещен в том месте, где была бы запись индекса, связанная с заданной закладкой вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="1c198-169">In that case, the cursor will be positioned where the index entry that is associated with the specified secondary index bookmark would have been.</span></span> <span data-ttu-id="1c198-170">Курсор можно переместить относительно этой позиции, но по-прежнему не находится в допустимой записи индекса.</span><span class="sxs-lookup"><span data-stu-id="1c198-170">The cursor can be moved relative to that position, but is still not on a valid index entry.</span></span>

<span data-ttu-id="1c198-171">Если запись подготовлена к обновлению, это обновление будет отменено.</span><span class="sxs-lookup"><span data-stu-id="1c198-171">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="1c198-172">Если действует диапазон индексов, то диапазон индексов будет отменен.</span><span class="sxs-lookup"><span data-stu-id="1c198-172">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="1c198-173">Если для использования курсора был создан ключ поиска, этот ключ поиска будет удален.</span><span class="sxs-lookup"><span data-stu-id="1c198-173">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="1c198-174">В любом случае изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c198-174">In any case, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1c198-175">Требования</span><span class="sxs-lookup"><span data-stu-id="1c198-175">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c198-176"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1c198-176"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1c198-177">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c198-177">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c198-178"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1c198-178"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1c198-179">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1c198-179">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c198-180"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1c198-180"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1c198-181">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1c198-181">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c198-182"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="1c198-182"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1c198-183">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1c198-183">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c198-184"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="1c198-184"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1c198-185">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1c198-185">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1c198-186">См. также:</span><span class="sxs-lookup"><span data-stu-id="1c198-186">See Also</span></span>

[<span data-ttu-id="1c198-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1c198-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1c198-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1c198-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1c198-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1c198-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1c198-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1c198-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1c198-191">жетжетсекондариндексбукмарк</span><span class="sxs-lookup"><span data-stu-id="1c198-191">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)  
[<span data-ttu-id="1c198-192">жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="1c198-192">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="1c198-193">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="1c198-193">JetStopService</span></span>](./jetstopservice-function.md)
