---
description: Дополнительные сведения о функции Жетиндексрекордкаунт
title: Функция Жетиндексрекордкаунт
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539978"
---
# <a name="jetindexrecordcount-function"></a><span data-ttu-id="46e67-103">Функция Жетиндексрекордкаунт</span><span class="sxs-lookup"><span data-stu-id="46e67-103">JetIndexRecordCount Function</span></span>


<span data-ttu-id="46e67-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="46e67-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetindexrecordcount-function"></a><span data-ttu-id="46e67-105">Функция Жетиндексрекордкаунт</span><span class="sxs-lookup"><span data-stu-id="46e67-105">JetIndexRecordCount Function</span></span>

<span data-ttu-id="46e67-106">Функция **жетиндексрекордкаунт** подсчитывает количество записей в текущем индексе до текущей позиции вперед.</span><span class="sxs-lookup"><span data-stu-id="46e67-106">The **JetIndexRecordCount** function counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="46e67-107">Текущая позицией включается в число.</span><span class="sxs-lookup"><span data-stu-id="46e67-107">The current position is included in the count.</span></span> <span data-ttu-id="46e67-108">Число может быть больше, чем общее число записей в таблице, если текущий индекс находится над многозначным столбцом, а экземпляры столбца имеют несколько значений.</span><span class="sxs-lookup"><span data-stu-id="46e67-108">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="46e67-109">Если таблица пуста, для счетчика будет возвращено значение 0.</span><span class="sxs-lookup"><span data-stu-id="46e67-109">If the table is empty, then 0 will be returned for the count.</span></span>

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a><span data-ttu-id="46e67-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="46e67-110">Parameters</span></span>

<span data-ttu-id="46e67-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="46e67-111">*sesid*</span></span>

<span data-ttu-id="46e67-112">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="46e67-112">The session to use for this call.</span></span>

<span data-ttu-id="46e67-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="46e67-113">*tableid*</span></span>

<span data-ttu-id="46e67-114">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="46e67-114">The cursor to use for this call.</span></span>

<span data-ttu-id="46e67-115">*пкрек*</span><span class="sxs-lookup"><span data-stu-id="46e67-115">*pcrec*</span></span>

<span data-ttu-id="46e67-116">Указатель на длинное значение без знака для получения счетчика.</span><span class="sxs-lookup"><span data-stu-id="46e67-116">The pointer to an unsigned long value to receive the count.</span></span>

<span data-ttu-id="46e67-117">*крекмакс*</span><span class="sxs-lookup"><span data-stu-id="46e67-117">*crecMax*</span></span>

<span data-ttu-id="46e67-118">Максимальное число записей для подсчета.</span><span class="sxs-lookup"><span data-stu-id="46e67-118">The maximum number of records to count.</span></span> <span data-ttu-id="46e67-119">Значение *крекмакс* , равное 0, указывает на то, что число не ограничено.</span><span class="sxs-lookup"><span data-stu-id="46e67-119">A *crecMax* value of 0 indicates that the count is unlimited.</span></span>

### <a name="return-value"></a><span data-ttu-id="46e67-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46e67-120">Return Value</span></span>

<span data-ttu-id="46e67-121">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="46e67-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="46e67-122">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="46e67-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46e67-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="46e67-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="46e67-124">Описание</span><span class="sxs-lookup"><span data-stu-id="46e67-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46e67-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="46e67-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="46e67-126">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="46e67-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e67-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="46e67-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="46e67-128">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="46e67-128">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e67-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="46e67-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="46e67-130">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="46e67-130">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="46e67-131"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="46e67-131"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e67-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="46e67-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="46e67-133">Курсор в настоящий момент не находится в записи, и таблица не пуста.</span><span class="sxs-lookup"><span data-stu-id="46e67-133">The cursor is not currently on a record and the table is not empty.</span></span></p>
<p><span data-ttu-id="46e67-134"><strong>Windows XP, Windows Server 2003, windows 2000 Server и windows 2000 Professional:</strong>  Если курсор располагается на пустом индексе или диапазоне индекса, <strong>жетиндексрекордкаунт</strong> ошибочно возвращает JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="46e67-134"><strong>Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:</strong>  If the cursor is positioned on an empty index or index range then <strong>JetIndexRecordCount</strong> erroneously returns JET_errNoCurrentRecord.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e67-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="46e67-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="46e67-136">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="46e67-136">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e67-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="46e67-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="46e67-138">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="46e67-138">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e67-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="46e67-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="46e67-140">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="46e67-140">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="46e67-141"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="46e67-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e67-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="46e67-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="46e67-143">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="46e67-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="46e67-144">Если эта функция выполнена, точное число записей индекса, включая текущую и до *крекмакс* (если оно не равно 0), возвращается в неподписанном длинном виде, на который указывает *пкрек*.</span><span class="sxs-lookup"><span data-stu-id="46e67-144">If this function succeeds, the exact number of index entries including the current position and up to *crecMax* (if it is not 0), is returned in the unsigned long pointed to by *pcrec*.</span></span>

<span data-ttu-id="46e67-145">Если эта функция завершается ошибкой, в память, выделенную в *прекпос*, не вносятся изменения.</span><span class="sxs-lookup"><span data-stu-id="46e67-145">If this function fails, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="46e67-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46e67-146">Remarks</span></span>

<span data-ttu-id="46e67-147">Если таблица не пуста, то курсор должен быть размещен на записи, с которой начинается подсчет.</span><span class="sxs-lookup"><span data-stu-id="46e67-147">If the table is not empty, then the cursor should be positioned onto the record from which to begin the count.</span></span> <span data-ttu-id="46e67-148">Количество будет включать эту запись и подсчитывать до заданного предела в *крекмакс*.</span><span class="sxs-lookup"><span data-stu-id="46e67-148">The count will include this record, and count forward up to the given limit in *crecMax*.</span></span> <span data-ttu-id="46e67-149">Если значение *крекмакс* равно 0, операция будет продолжать подсчета до конца индекса.</span><span class="sxs-lookup"><span data-stu-id="46e67-149">If *crecMax* is 0 then the operation will continue counting until the end of the index.</span></span>

<span data-ttu-id="46e67-150">Диапазоны индексов можно использовать для создания искусственных ограничений на конец индекса для счетчика.</span><span class="sxs-lookup"><span data-stu-id="46e67-150">Index ranges can be used to construct artificial end-of-index limitations for the count.</span></span> <span data-ttu-id="46e67-151">Таким образом, поддиапазоны индекса можно полностью подсчитать.</span><span class="sxs-lookup"><span data-stu-id="46e67-151">In this way, subranges of an index can be counted exactly.</span></span> <span data-ttu-id="46e67-152">Курсор должен располагаться в первой строке диапазона.</span><span class="sxs-lookup"><span data-stu-id="46e67-152">The cursor should be positioned to the first row in the range.</span></span> <span data-ttu-id="46e67-153">Должен быть выполнен конец ключа диапазона, а затем [жетсетиндексранже](./jetsetindexrange-function.md) должен использоваться для задания верхнего диапазона, включающего или исключительного.</span><span class="sxs-lookup"><span data-stu-id="46e67-153">The end of the range key should be made and then [JetSetIndexRange](./jetsetindexrange-function.md) should be used to set the upper range, either inclusively or exclusively.</span></span> <span data-ttu-id="46e67-154">Наконец, **жетиндексрекордкаунт** должен быть вызван для точного подсчета диапазона.</span><span class="sxs-lookup"><span data-stu-id="46e67-154">Lastly, **JetIndexRecordCount** should be called to exactly count the range.</span></span>

<span data-ttu-id="46e67-155">**Жетиндексрекордкаунт** подчиняется семантике транзакции и возвращает счетчик, который является точным для этого конкретного сеанса в текущем состоянии транзакции.</span><span class="sxs-lookup"><span data-stu-id="46e67-155">**JetIndexRecordCount** obeys transaction semantics and returns a count that is accurate for this particular session in its current transactional state.</span></span>

<span data-ttu-id="46e67-156">**Жетиндексрекордкаунт** обращается к конечным страницам индекса для точного подсчета записей.</span><span class="sxs-lookup"><span data-stu-id="46e67-156">**JetIndexRecordCount** accesses index leaf pages in order to exactly count entries.</span></span> <span data-ttu-id="46e67-157">Следовательно, она может выполнять большую часть операций ввода-вывода и может быть достаточно высокой.</span><span class="sxs-lookup"><span data-stu-id="46e67-157">Consequently, it can perform a great deal of I/O and can be slow.</span></span> <span data-ttu-id="46e67-158">Для предотвращения чрезмерной нагрузки следует использовать ограничение *крекмакс* .</span><span class="sxs-lookup"><span data-stu-id="46e67-158">The *crecMax* limitation should be used to prevent excessive load.</span></span> <span data-ttu-id="46e67-159">Если диапазон большой, то можно будет подсчитать диапазон приблизительным способом с помощью [жетжетрекордпоситион](./jetgetrecordposition-function.md).</span><span class="sxs-lookup"><span data-stu-id="46e67-159">If a range is large, then it might be possible to count the range in an approximated fashion using [JetGetRecordPosition](./jetgetrecordposition-function.md).</span></span>

<span data-ttu-id="46e67-160">**Windows XP, Windows Server 2003, windows 2000 Server и windows 2000 Professional:**  Если курсор располагается на пустом индексе или диапазоне индекса, **жетиндексрекордкаунт** возвращает JET_errNoCurrentRecord, а не возвращается число записей, равное нулю.</span><span class="sxs-lookup"><span data-stu-id="46e67-160">**Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:**  If the cursor is positioned on an empty index or index range then **JetIndexRecordCount** erroneously returns JET_errNoCurrentRecord rather than returning a record count of zero.</span></span> <span data-ttu-id="46e67-161">Приложение должно проверить, пуст ли индекс или диапазон индекса в этом случае.</span><span class="sxs-lookup"><span data-stu-id="46e67-161">The application should check to see if the index or index range is empty in this case.</span></span>

#### <a name="requirements"></a><span data-ttu-id="46e67-162">Требования</span><span class="sxs-lookup"><span data-stu-id="46e67-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46e67-163"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="46e67-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="46e67-164">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="46e67-164">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e67-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="46e67-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="46e67-166">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="46e67-166">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e67-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="46e67-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="46e67-168">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="46e67-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e67-169"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="46e67-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="46e67-170">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="46e67-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e67-171"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="46e67-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="46e67-172">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="46e67-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="46e67-173">См. также:</span><span class="sxs-lookup"><span data-stu-id="46e67-173">See Also</span></span>

[<span data-ttu-id="46e67-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="46e67-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="46e67-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="46e67-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="46e67-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="46e67-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="46e67-177">жетжетрекордпоситион</span><span class="sxs-lookup"><span data-stu-id="46e67-177">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="46e67-178">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="46e67-178">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="46e67-179">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="46e67-179">JetStopService</span></span>](./jetstopservice-function.md)
