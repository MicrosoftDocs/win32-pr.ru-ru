---
description: Дополнительные сведения о функции Жетжетрекордпоситион
title: Функция JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080884"
---
# <a name="jetgetrecordposition-function"></a><span data-ttu-id="9c49e-103">Функция JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="9c49e-103">JetGetRecordPosition Function</span></span>


<span data-ttu-id="9c49e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c49e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordposition-function"></a><span data-ttu-id="9c49e-105">Функция JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="9c49e-105">JetGetRecordPosition Function</span></span>

<span data-ttu-id="9c49e-106">Функция **жетжетрекордпоситион** Возвращает дробную часть текущей записи в текущем индексе в виде структуры [JET_RECPOS](./jet-recpos-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="9c49e-106">The **JetGetRecordPosition** function returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-structure.md) structure.</span></span> <span data-ttu-id="9c49e-107">Эта структура описывает дробные положения с точки зрения приблизительного числа элементов индекса до текущей записи и приблизительного общего числа записей в индексе.</span><span class="sxs-lookup"><span data-stu-id="9c49e-107">This structure describes fractional positions in terms of an approximate number of index entries before the current record and an approximate total number of entries in the index.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a><span data-ttu-id="9c49e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c49e-108">Parameters</span></span>

<span data-ttu-id="9c49e-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="9c49e-109">*sesid*</span></span>

<span data-ttu-id="9c49e-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9c49e-110">The session to use for this call.</span></span>

<span data-ttu-id="9c49e-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9c49e-111">*tableid*</span></span>

<span data-ttu-id="9c49e-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9c49e-112">The cursor to use for this call.</span></span>

<span data-ttu-id="9c49e-113">*прекпос*</span><span class="sxs-lookup"><span data-stu-id="9c49e-113">*precpos*</span></span>

<span data-ttu-id="9c49e-114">Описание доли, используемой при получении позиции текущей записи в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="9c49e-114">The description of the fraction to use in getting the position of the current record in the current index.</span></span>

<span data-ttu-id="9c49e-115">*кбрекпос*</span><span class="sxs-lookup"><span data-stu-id="9c49e-115">*cbRecpos*</span></span>

<span data-ttu-id="9c49e-116">Размер памяти, выделенной на *прекпос*.</span><span class="sxs-lookup"><span data-stu-id="9c49e-116">The size of memory allocated at *precpos*.</span></span>

### <a name="return-value"></a><span data-ttu-id="9c49e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c49e-117">Return Value</span></span>

<span data-ttu-id="9c49e-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="9c49e-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9c49e-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9c49e-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c49e-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9c49e-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="9c49e-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9c49e-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c49e-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9c49e-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9c49e-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9c49e-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c49e-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9c49e-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9c49e-125">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="9c49e-125">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c49e-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9c49e-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9c49e-127">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="9c49e-127">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c49e-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9c49e-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9c49e-129">Эта операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку.</span><span class="sxs-lookup"><span data-stu-id="9c49e-129">This operation cannot complete because the instance, associated with the session, encountered a fatal error.</span></span> <span data-ttu-id="9c49e-130">Чтобы защитить целостность данных, необходимо отозвать доступ ко всем данным.</span><span class="sxs-lookup"><span data-stu-id="9c49e-130">It is required that access to all data be revoked in order to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9c49e-131"><strong>Windows 2000:</strong>  Эта ошибка не будет возвращена операционной системой Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9c49e-131"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c49e-132">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9c49e-132">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9c49e-133">Размер выделенной памяти на <em>прекпос</em> не является достаточным размером.</span><span class="sxs-lookup"><span data-stu-id="9c49e-133">The size of the allocated memory at <em>precpos</em> is not a sufficient size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c49e-134">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="9c49e-134">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="9c49e-135">Курсор в настоящий момент не находится в записи и не может вернуть позицию.</span><span class="sxs-lookup"><span data-stu-id="9c49e-135">The cursor is not currently on a record and cannot return a position.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c49e-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9c49e-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9c49e-137">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="9c49e-137">It is not possible to complete the operation because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c49e-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9c49e-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9c49e-139">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="9c49e-139">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="9c49e-140"><strong>Windows 2000:</strong>  Эта ошибка не будет возвращена операционной системой Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9c49e-140"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c49e-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9c49e-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9c49e-142">Операция не может быть завершена, так как экземпляр, связанный с сеансом, завершает работу.</span><span class="sxs-lookup"><span data-stu-id="9c49e-142">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c49e-143">При успешном выполнении приблизительное количество записей индекса, предшествующее текущей записи в индексе, возвращается в прекпос- \> центриеслт.</span><span class="sxs-lookup"><span data-stu-id="9c49e-143">On success, the approximate number of index entries preceding the current record in the index are returned in precpos-\>centriesLT.</span></span> <span data-ttu-id="9c49e-144">1 возвращается в прекпос- \> центриесинранже.</span><span class="sxs-lookup"><span data-stu-id="9c49e-144">1 is returned in precpos-\>centriesInRange.</span></span> <span data-ttu-id="9c49e-145">Приблизительное число записей в индексе возвращается в прекпос- \> центриестотал.</span><span class="sxs-lookup"><span data-stu-id="9c49e-145">The approximate number of entries in the index is returned in precpos-\>centriesTotal.</span></span>

<span data-ttu-id="9c49e-146">В случае сбоя в память, выделенную в *прекпос*, не вносятся изменения.</span><span class="sxs-lookup"><span data-stu-id="9c49e-146">On failure, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9c49e-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c49e-147">Remarks</span></span>

<span data-ttu-id="9c49e-148">Эта операция возвращает различные данные, когда обновления происходят непрерывно в таблице.</span><span class="sxs-lookup"><span data-stu-id="9c49e-148">This operation returns varying data when updates occur continuously on the table.</span></span> <span data-ttu-id="9c49e-149">Изменения в значениях не всегда будут соответствовать ожиданиям на основе знаний об обновлениях, так как значения являются приближениями на основе физических свойств индекса.</span><span class="sxs-lookup"><span data-stu-id="9c49e-149">The changes in the values will not always match expectations based on knowledge of the updates, since the values are approximations based on physical properties of the index.</span></span> <span data-ttu-id="9c49e-150">Изоляция транзакций не применяется к позициям из **жетжетрекордпоситион** , так как значения зависят от физических свойств индекса, которые не являются изолированными транзакциями.</span><span class="sxs-lookup"><span data-stu-id="9c49e-150">Transactional isolation does not apply to positions from **JetGetRecordPosition** since the values depend on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="9c49e-151">[JET_RECPOS](./jet-recpos-structure.md) не следует использовать для описания записи в таблице или перемещения записи, близкой к существующей записи.</span><span class="sxs-lookup"><span data-stu-id="9c49e-151">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="9c49e-152">Вместо этого необходимо извлечь закладки для существующей записи, а затем использовать ее для перемещения той же записи.</span><span class="sxs-lookup"><span data-stu-id="9c49e-152">Instead, bookmarks for an existing record should be retrieved and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9c49e-153">Требования</span><span class="sxs-lookup"><span data-stu-id="9c49e-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c49e-154"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9c49e-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c49e-155">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9c49e-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c49e-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9c49e-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c49e-157">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9c49e-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c49e-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9c49e-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c49e-159">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9c49e-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c49e-160"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="9c49e-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9c49e-161">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9c49e-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c49e-162"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="9c49e-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9c49e-163">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9c49e-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9c49e-164">См. также:</span><span class="sxs-lookup"><span data-stu-id="9c49e-164">See Also</span></span>

[<span data-ttu-id="9c49e-165">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9c49e-165">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="9c49e-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9c49e-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9c49e-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9c49e-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9c49e-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9c49e-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9c49e-169">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="9c49e-169">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="9c49e-170">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="9c49e-170">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="9c49e-171">жетготопоситион</span><span class="sxs-lookup"><span data-stu-id="9c49e-171">JetGotoPosition</span></span>](./jetgotoposition-function.md)  
[<span data-ttu-id="9c49e-172">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="9c49e-172">JetStopService</span></span>](./jetstopservice-function.md)
