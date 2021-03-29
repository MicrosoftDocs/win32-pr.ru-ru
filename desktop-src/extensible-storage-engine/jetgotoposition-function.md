---
description: Дополнительные сведения о функции Жетготопоситион
title: Функция Жетготопоситион
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808440"
---
# <a name="jetgotoposition-function"></a><span data-ttu-id="3b486-103">Функция Жетготопоситион</span><span class="sxs-lookup"><span data-stu-id="3b486-103">JetGotoPosition Function</span></span>


<span data-ttu-id="3b486-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b486-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotoposition-function"></a><span data-ttu-id="3b486-105">Функция Жетготопоситион</span><span class="sxs-lookup"><span data-stu-id="3b486-105">JetGotoPosition Function</span></span>

<span data-ttu-id="3b486-106">Функция **жетготопоситион** перемещает курсор на новое место, которое представляет собой часть пути по текущему индексу.</span><span class="sxs-lookup"><span data-stu-id="3b486-106">The **JetGotoPosition** function moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="3b486-107">Дробная часть приблизительно равна следующей:</span><span class="sxs-lookup"><span data-stu-id="3b486-107">The fraction is approximately equal to the following:</span></span>

<span data-ttu-id="3b486-108">прекпос- \> центриеслт/прекпос- \> центриестотал</span><span class="sxs-lookup"><span data-stu-id="3b486-108">precpos-\>centriesLT/precpos-\>centriesTotal</span></span>

<span data-ttu-id="3b486-109">Эта операция выполняется в ответ на ввод поля полосы прокрутки пользователя, полученного при попытке пользователя отобразить данные, которые начинаются с помощью набора данных.</span><span class="sxs-lookup"><span data-stu-id="3b486-109">This operation is performed in response to user scroll box input that is received when the user attempts to show data that starts part way through a data set.</span></span>

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a><span data-ttu-id="3b486-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b486-110">Parameters</span></span>

<span data-ttu-id="3b486-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="3b486-111">*sesid*</span></span>

<span data-ttu-id="3b486-112">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="3b486-112">The session to use for this call.</span></span>

<span data-ttu-id="3b486-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="3b486-113">*tableid*</span></span>

<span data-ttu-id="3b486-114">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="3b486-114">The cursor to use for this call.</span></span>

<span data-ttu-id="3b486-115">*прекпос*</span><span class="sxs-lookup"><span data-stu-id="3b486-115">*precpos*</span></span>

<span data-ttu-id="3b486-116">Описание доли, используемой при размещении курсора в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="3b486-116">The description of the fraction to use in positioning the cursor in the current index.</span></span>

### <a name="return-value"></a><span data-ttu-id="3b486-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b486-117">Return Value</span></span>

<span data-ttu-id="3b486-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="3b486-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3b486-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3b486-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b486-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3b486-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="3b486-121">Описание</span><span class="sxs-lookup"><span data-stu-id="3b486-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b486-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3b486-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3b486-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3b486-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b486-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3b486-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3b486-125">Не удалось выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="3b486-125">The operation could not complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b486-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3b486-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3b486-127">Не удалось выполнить операцию, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="3b486-127">The operation could not complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3b486-128"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b486-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b486-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3b486-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3b486-130">Заданный прекпос- &gt; кбструкт не является допустимым размером для структуры <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> , или прекпос- &gt; центриеслт больше прекпос- &gt; центриестотал.</span><span class="sxs-lookup"><span data-stu-id="3b486-130">The given precpos-&gt;cbStruct is not a valid size for the <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> structure, or precpos-&gt;centriesLT is greater than precpos-&gt;centriesTotal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b486-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3b486-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3b486-132">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="3b486-132">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b486-133">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="3b486-133">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="3b486-134">Эта ошибка будет возвращена, если индекс пуст.</span><span class="sxs-lookup"><span data-stu-id="3b486-134">This error will be returned if the index is empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b486-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3b486-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3b486-136">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="3b486-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b486-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3b486-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3b486-138">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="3b486-138">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="3b486-139"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b486-139"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b486-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3b486-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3b486-141">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="3b486-141">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b486-142">Если эта функция завершилась с ошибкой, курсор перемещается на текущую запись, которая является долей пути, где дробь прекпос- \> центриеслт делится на прекпос- \> центриестотал.</span><span class="sxs-lookup"><span data-stu-id="3b486-142">If this function succeeds, the cursor is moved to a current record that is a fraction of the way through the index where the fraction is precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="3b486-143">Если эта функция завершается ошибкой, расположение курсора остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="3b486-143">If this function fails, the cursor location is left unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3b486-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b486-144">Remarks</span></span>

<span data-ttu-id="3b486-145">Эта операция перемещает курсор через таблицу в позицию в следующей приблизительной точке: прекпос- \> центриеслт, деленную на прекпос- \> центриестотал.</span><span class="sxs-lookup"><span data-stu-id="3b486-145">This operation moves the cursor through the table to a position at the following approximate point: precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="3b486-146">При постоянном обновлении таблицы Последующие вызовы с тем же [JET_RECPOS](./jet-recpos-structure.md) могут перемещать курсор на разные позиции в индексе до и после предыдущей позиции.</span><span class="sxs-lookup"><span data-stu-id="3b486-146">When updates are occurring continuously on the table, subsequent calls with the same [JET_RECPOS](./jet-recpos-structure.md) can move the cursor to different positions in the index, both before and after the previous position.</span></span> <span data-ttu-id="3b486-147">Изоляция транзакций не применяется к размещению по [JET_RECPOS](./jet-recpos-structure.md) , поскольку она зависит от физических свойств индекса, которые не изолированы от транзакции.</span><span class="sxs-lookup"><span data-stu-id="3b486-147">Transactional isolation does not apply to positioning through [JET_RECPOS](./jet-recpos-structure.md) since it depends on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="3b486-148">[JET_RECPOS](./jet-recpos-structure.md) не следует использовать для описания записи в таблице или перемещения записи, близкой к существующей записи.</span><span class="sxs-lookup"><span data-stu-id="3b486-148">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="3b486-149">Вместо этого закладки для существующей записи должны быть получены после первоначального **жетготопоситион** , а затем использоваться для перемещения той же записи.</span><span class="sxs-lookup"><span data-stu-id="3b486-149">Instead, bookmarks for an existing record should be retrieved after an initial **JetGotoPosition** and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3b486-150">Требования</span><span class="sxs-lookup"><span data-stu-id="3b486-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b486-151"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="3b486-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b486-152">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3b486-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b486-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3b486-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b486-154">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3b486-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b486-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3b486-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b486-156">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3b486-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b486-157"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="3b486-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3b486-158">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3b486-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b486-159"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="3b486-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3b486-160">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3b486-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3b486-161">См. также:</span><span class="sxs-lookup"><span data-stu-id="3b486-161">See Also</span></span>

[<span data-ttu-id="3b486-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="3b486-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="3b486-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3b486-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3b486-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3b486-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3b486-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3b486-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3b486-166">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="3b486-166">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="3b486-167">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="3b486-167">JET_SETINFO</span></span>](./jet-setinfo-structure.md)
