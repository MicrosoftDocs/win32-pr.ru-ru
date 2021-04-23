---
description: Дополнительные сведения о функции Жетжетбукмарк
title: Функция Жетжетбукмарк
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156807"
---
# <a name="jetgetbookmark-function"></a><span data-ttu-id="bada1-103">Функция Жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="bada1-103">JetGetBookmark Function</span></span>


<span data-ttu-id="bada1-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bada1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetbookmark-function"></a><span data-ttu-id="bada1-105">Функция Жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="bada1-105">JetGetBookmark Function</span></span>

<span data-ttu-id="bada1-106">Функция **жетжетбукмарк** извлекает закладку для записи, связанной с элементом индекса, в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="bada1-106">The **JetGetBookmark** function retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="bada1-107">Эту закладку можно использовать для перемещения курсора обратно в ту же запись с помощью [жетготобукмарк](./jetgotobookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="bada1-107">This bookmark can then be used to reposition that cursor back to the same record using [JetGoToBookmark](./jetgotobookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="bada1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bada1-108">Parameters</span></span>

<span data-ttu-id="bada1-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="bada1-109">*sesid*</span></span>

<span data-ttu-id="bada1-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="bada1-110">The session to use for this call.</span></span>

<span data-ttu-id="bada1-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="bada1-111">*tableid*</span></span>

<span data-ttu-id="bada1-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="bada1-112">The cursor to use for this call.</span></span>

<span data-ttu-id="bada1-113">*пвбукмарк*</span><span class="sxs-lookup"><span data-stu-id="bada1-113">*pvBookmark*</span></span>

<span data-ttu-id="bada1-114">Выходной буфер, получающий закладку.</span><span class="sxs-lookup"><span data-stu-id="bada1-114">The output buffer that receives the bookmark.</span></span>

<span data-ttu-id="bada1-115">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="bada1-115">*cbMax*</span></span>

<span data-ttu-id="bada1-116">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="bada1-116">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="bada1-117">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="bada1-117">*pcbActual*</span></span>

<span data-ttu-id="bada1-118">Фактический размер закладки в байтах.</span><span class="sxs-lookup"><span data-stu-id="bada1-118">The actual size, in bytes, of the bookmark.</span></span>

<span data-ttu-id="bada1-119">Если этот параметр имеет **значение NULL** , фактический размер закладки не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="bada1-119">If this parameter is **NULL** then the actual size of the bookmark will not be returned.</span></span>

<span data-ttu-id="bada1-120">Если выходной буфер слишком мал, фактический размер закладки все равно будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="bada1-120">If the output buffer is too small, the actual size of the bookmark will still be returned.</span></span> <span data-ttu-id="bada1-121">Это означает, что это число будет больше, чем размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="bada1-121">That means that this number will be larger than the size of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="bada1-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bada1-122">Return Value</span></span>

<span data-ttu-id="bada1-123">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="bada1-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bada1-124">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bada1-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bada1-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bada1-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="bada1-126">Описание</span><span class="sxs-lookup"><span data-stu-id="bada1-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bada1-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bada1-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bada1-128">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bada1-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bada1-129">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="bada1-129">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="bada1-130">Операция успешно завершена, но выходной буфер слишком мал для получения всей закладки.</span><span class="sxs-lookup"><span data-stu-id="bada1-130">The operation completed successfully, but the output buffer was too small to receive the entire bookmark.</span></span> <span data-ttu-id="bada1-131">Выходной буфер заполнен объемом заданной закладки.</span><span class="sxs-lookup"><span data-stu-id="bada1-131">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="bada1-132">При запросе также возвращается фактический размер закладки.</span><span class="sxs-lookup"><span data-stu-id="bada1-132">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bada1-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bada1-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bada1-134">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="bada1-134">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bada1-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bada1-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bada1-136">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="bada1-136">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="bada1-137"><strong>Windows XP:  </strong> Эти возвращаемые значения появились в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bada1-137"><strong>Windows XP:  </strong>This return values is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bada1-138">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="bada1-138">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="bada1-139">Курсор не располагается на записи.</span><span class="sxs-lookup"><span data-stu-id="bada1-139">The cursor is not positioned on a record.</span></span> <span data-ttu-id="bada1-140">Это может произойти по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="bada1-140">This can happen for many different reasons.</span></span> <span data-ttu-id="bada1-141">Например, это произойдет, если курсор помещается после последней записи текущего индекса.</span><span class="sxs-lookup"><span data-stu-id="bada1-141">For example, this will happen if the cursor is positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bada1-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bada1-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bada1-143">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="bada1-143">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bada1-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bada1-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bada1-145">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="bada1-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bada1-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bada1-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bada1-147">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="bada1-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="bada1-148"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bada1-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bada1-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bada1-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bada1-150">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="bada1-150">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bada1-151">Если эта функция выполнена, закладка для записи, связанной с записью индекса в текущей позиции курсора, будет возвращена в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="bada1-151">If this function succeeds, the bookmark for the record that is associated with the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="bada1-152">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bada1-152">No change to the database state will occur.</span></span>

<span data-ttu-id="bada1-153">Если эта функция завершается ошибкой, состояние выходного буфера и фактический размер закладки будут неопределенными, если не была возвращена JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="bada1-153">If this function fails, the state of the output buffer and the actual size of the bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="bada1-154">В случае, если возвращается JET_errBufferTooSmall, выходной буфер будет содержать столько закладок, сколько будет помещаться в предоставленное пространство, и фактический размер закладки будет неточным.</span><span class="sxs-lookup"><span data-stu-id="bada1-154">In the event that JET_errBufferTooSmall is returned, the output buffer will contain as much of the bookmark as will fit in the space provided and the actual size of the bookmark will be accurate.</span></span> <span data-ttu-id="bada1-155">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bada1-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bada1-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bada1-156">Remarks</span></span>

<span data-ttu-id="bada1-157">Закладки обычно должны рассматриваться как непрозрачные фрагменты данных.</span><span class="sxs-lookup"><span data-stu-id="bada1-157">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="bada1-158">Для использования внутренней структуры этих данных не нужно предпринимать никаких попыток.</span><span class="sxs-lookup"><span data-stu-id="bada1-158">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="bada1-159">Однако для всех закладок ESENT справедливы следующие условия:</span><span class="sxs-lookup"><span data-stu-id="bada1-159">However, the following conditions are true of all ESENT bookmarks:</span></span>

  - <span data-ttu-id="bada1-160">Закладка однозначно определяет запись в заданной таблице.</span><span class="sxs-lookup"><span data-stu-id="bada1-160">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="bada1-161">Закладка записи не изменится в течение времени существования этой записи.</span><span class="sxs-lookup"><span data-stu-id="bada1-161">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="bada1-162">Закладка записи совпадает с ключом записи на первичном индексе таблицы, содержащей эту запись.</span><span class="sxs-lookup"><span data-stu-id="bada1-162">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="bada1-163">Если в этой таблице не определен первичный индекс, ядро СУБД создаст собственную закладку для записи.</span><span class="sxs-lookup"><span data-stu-id="bada1-163">If no primary index is defined over that table the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="bada1-164">Закладки можно сравнить друг с другом с помощью функции [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) , чтобы установить их относительное упорядочение в первичном индексе по таблице исходных записей.</span><span class="sxs-lookup"><span data-stu-id="bada1-164">Bookmarks can be compared against each other using the [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) function to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="bada1-165">Если для этой таблицы не определен первичный индекс, не имеет смысла использовать относительный порядок закладок из этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="bada1-165">If no primary index is defined over that table, it is not meaningful to use the relative ordering of bookmarks from that table.</span></span>

  - <span data-ttu-id="bada1-166">Нет смысла сравнивать закладки записей из разных таблиц друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bada1-166">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="bada1-167">Длина закладки всегда меньше или равна JET_cbBookmarkMost (256) байт до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bada1-167">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length, prior to Windows Vista.</span></span>
    
<span data-ttu-id="bada1-168">**Windows Vista:** В Windows Vista и более поздних выпусках закладки могут быть больше JET_cbBookmarkMost (256) байт.</span><span class="sxs-lookup"><span data-stu-id="bada1-168">**Windows Vista:** On Windows Vista and later releases, bookmarks can be larger than JET_cbBookmarkMost (256) bytes.</span></span> <span data-ttu-id="bada1-169">Максимальный размер закладки равен текущему значению JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="bada1-169">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bada1-170">Требования</span><span class="sxs-lookup"><span data-stu-id="bada1-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bada1-171"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="bada1-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bada1-172">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bada1-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bada1-173"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bada1-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bada1-174">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bada1-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bada1-175"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bada1-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bada1-176">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bada1-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bada1-177"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="bada1-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bada1-178">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bada1-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bada1-179"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="bada1-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bada1-180">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bada1-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bada1-181">См. также:</span><span class="sxs-lookup"><span data-stu-id="bada1-181">See Also</span></span>

[<span data-ttu-id="bada1-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bada1-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bada1-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bada1-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bada1-184">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bada1-184">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bada1-185">жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="bada1-185">JetGoToBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="bada1-186">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="bada1-186">JetStopService</span></span>](./jetstopservice-function.md)  
<span data-ttu-id="bada1-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="bada1-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
