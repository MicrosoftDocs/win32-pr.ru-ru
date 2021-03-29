---
description: Дополнительные сведения о функции Жетупдате
title: Функция JetUpdate
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897661"
---
# <a name="jetupdate-function"></a><span data-ttu-id="554b3-103">Функция JetUpdate</span><span class="sxs-lookup"><span data-stu-id="554b3-103">JetUpdate Function</span></span>


<span data-ttu-id="554b3-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="554b3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate-function"></a><span data-ttu-id="554b3-105">Функция JetUpdate</span><span class="sxs-lookup"><span data-stu-id="554b3-105">JetUpdate Function</span></span>

<span data-ttu-id="554b3-106">Функция **жетупдате** выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки.</span><span class="sxs-lookup"><span data-stu-id="554b3-106">The **JetUpdate** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="554b3-107">Удаление строки таблицы выполняется путем вызова [жетделете](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="554b3-107">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="554b3-108">**Жетупдате** является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="554b3-108">**JetUpdate** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="554b3-109">Обновление начинается с вызова [жетпрепареупдате](./jetprepareupdate-function.md) , а затем путем вызова [жетсетколумн](./jetsetcolumn-function.md) или [жетсетколумнс](./jetsetcolumns-function.md) один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="554b3-109">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="554b3-110">Наконец, для завершения операции обновления вызывается **жетупдате** .</span><span class="sxs-lookup"><span data-stu-id="554b3-110">Finally, **JetUpdate** is called to complete the update operation.</span></span> <span data-ttu-id="554b3-111">Индексы обновляются только в **жетупдате** или [JetUpdate2](./jetupdate2-function.md), а не во время [жетсетколумн](./jetsetcolumn-function.md) или [жетсетколумнс](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="554b3-111">Indexes are updated only by **JetUpdate** or [JetUpdate2](./jetupdate2-function.md), and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="554b3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="554b3-112">Parameters</span></span>

<span data-ttu-id="554b3-113">*сесид*</span><span class="sxs-lookup"><span data-stu-id="554b3-113">*sesid*</span></span>

<span data-ttu-id="554b3-114">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="554b3-114">The session to use for this call.</span></span>

<span data-ttu-id="554b3-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="554b3-115">*tableid*</span></span>

<span data-ttu-id="554b3-116">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="554b3-116">The cursor to use for this call.</span></span>

<span data-ttu-id="554b3-117">*пвбукмарк*</span><span class="sxs-lookup"><span data-stu-id="554b3-117">*pvBookmark*</span></span>

<span data-ttu-id="554b3-118">Указатель на возвращаемую закладку для вставленной строки.</span><span class="sxs-lookup"><span data-stu-id="554b3-118">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="554b3-119">*кббукмарк*</span><span class="sxs-lookup"><span data-stu-id="554b3-119">*cbBookmark*</span></span>

<span data-ttu-id="554b3-120">Размер буфера, на который указывает *пвбукмарк*.</span><span class="sxs-lookup"><span data-stu-id="554b3-120">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="554b3-121">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="554b3-121">*pcbActual*</span></span>

<span data-ttu-id="554b3-122">Возвращаемый размер закладки для вставляемой строки, возвращенной в *пвбукмарк*.</span><span class="sxs-lookup"><span data-stu-id="554b3-122">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

### <a name="return-value"></a><span data-ttu-id="554b3-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="554b3-123">Return Value</span></span>

<span data-ttu-id="554b3-124">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="554b3-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="554b3-125">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="554b3-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="554b3-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="554b3-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="554b3-127">Описание</span><span class="sxs-lookup"><span data-stu-id="554b3-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="554b3-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="554b3-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="554b3-129">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="554b3-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-130">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="554b3-130">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="554b3-131">Заданный буфер для закладки записи недостаточно велик для хранения закладки записи.</span><span class="sxs-lookup"><span data-stu-id="554b3-131">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="554b3-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="554b3-133">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="554b3-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-134">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="554b3-134">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="554b3-135">То же, что и JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="554b3-135">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-136">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="554b3-136">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="554b3-137">Операция обновления требует увеличения размера файла базы данных или выделения файла журнала, но диск, на котором находится файл базы данных или ряд журналов, заполнен.</span><span class="sxs-lookup"><span data-stu-id="554b3-137">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="554b3-138">Кроме того, файл базы данных находится на томе в формате FAT32, а файл базы данных уже 4GBytes, ограничение на количество файлов для FAT32.</span><span class="sxs-lookup"><span data-stu-id="554b3-138">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="554b3-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="554b3-140">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="554b3-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="554b3-141"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="554b3-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="554b3-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="554b3-143">Данный параметр <em>подготовки</em> в функции <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a> не является допустимым флагом.</span><span class="sxs-lookup"><span data-stu-id="554b3-143">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-144">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="554b3-144">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="554b3-145">Ключ индекса для этой записи является дубликатом другого ключа индекса для другой записи, уже наданнымся в таблице, и индекс не допускает дублирования.</span><span class="sxs-lookup"><span data-stu-id="554b3-145">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-146">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="554b3-146">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="554b3-147">Вставленная или обновленная запись имеет один или несколько индексов, для которых созданный ключ превысил максимально допустимый размер.</span><span class="sxs-lookup"><span data-stu-id="554b3-147">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="554b3-148">В результате операция не смогла предотвратить усечение ключа.</span><span class="sxs-lookup"><span data-stu-id="554b3-148">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-149">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="554b3-149">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="554b3-150">Вставленная или обновленная запись имеет индексируемый многозначный столбец с двумя или более значениями, идентичными в пределах ключа максимальной длины, установленного для индекса.</span><span class="sxs-lookup"><span data-stu-id="554b3-150">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="554b3-151">В результате запись содержит две идентичные записи в индексе, что недопустимо.</span><span class="sxs-lookup"><span data-stu-id="554b3-151">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="554b3-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="554b3-153">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="554b3-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-154">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="554b3-154">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="554b3-155">Один или несколько столбцов вставляемой записи или в обновленном состоянии заменяемой записи имеют <strong>значение NULL</strong> , что нарушает определенное ограничение для этих столбцов.</span><span class="sxs-lookup"><span data-stu-id="554b3-155">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-156">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="554b3-156">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="554b3-157">Один или несколько индексов не позволяют разрешить ключ <strong>null</strong> , а вставленное или обновленное состояние заменяемой записи нарушает это заданное ограничение.</span><span class="sxs-lookup"><span data-stu-id="554b3-157">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-158">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="554b3-158">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="554b3-159">Операция замены записи обновила первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="554b3-159">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="554b3-160">Обновления первичных ключевых столбцов должны выполняться путем удаления существующей записи и вставки новой записи с нужными данными.</span><span class="sxs-lookup"><span data-stu-id="554b3-160">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="554b3-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="554b3-162">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="554b3-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="554b3-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="554b3-164">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="554b3-164">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="554b3-165"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="554b3-165"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="554b3-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="554b3-167">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="554b3-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-168">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="554b3-168">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="554b3-169">Попытка обновления недействительна в пределах транзакции, доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="554b3-169">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="554b3-170">Транзакция только для чтения — это транзакция, которая была запущена с помощью вызова <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> с JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="554b3-170">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="554b3-171"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="554b3-171"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-172">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="554b3-172">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="554b3-173"><a href="gg269339(v=exchg.10).md">Жетпрепареупдате</a> был вызван с JET_prepCancel, но курсор не был в подготовленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="554b3-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-174">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="554b3-174">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="554b3-175">Не удалось выполнить операцию, так как недостаточно памяти для удержания транзакционных сведений об обновлении.</span><span class="sxs-lookup"><span data-stu-id="554b3-175">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-176">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="554b3-176">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="554b3-177">Другой сеанс ранее заблокировал запись для обновления.</span><span class="sxs-lookup"><span data-stu-id="554b3-177">Another session has previously locked the record for update.</span></span> <span data-ttu-id="554b3-178">Обновление, которое попыталось этот сеанс, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="554b3-178">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="554b3-179">При успешном выполнении операция открытия обновления курсора завершается.</span><span class="sxs-lookup"><span data-stu-id="554b3-179">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="554b3-180">Если для таблицы определен автоматически увеличивающийся столбец, то это значение устанавливается для вставленных записей.</span><span class="sxs-lookup"><span data-stu-id="554b3-180">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="554b3-181">Если для таблицы определен столбец версии, то его значение инициализируется для вновь вставленных записей или увеличивается каждый раз при замене записи.</span><span class="sxs-lookup"><span data-stu-id="554b3-181">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="554b3-182">Обновляются все индексы, включая кластеризованные и некластеризованные индексы.</span><span class="sxs-lookup"><span data-stu-id="554b3-182">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="554b3-183">В случае сбоя изменения какого либо типа не вносятся в базу данных.</span><span class="sxs-lookup"><span data-stu-id="554b3-183">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="554b3-184">Перед вставкой и до замены функции обратного вызова могут быть вызваны, но после вызовов INSERT и After replace не будут вызываться, так как Последнее не может привести к сбою обновления.</span><span class="sxs-lookup"><span data-stu-id="554b3-184">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="554b3-185">Буфер копирования курсора остается в подготовленном состоянии, чтобы можно было постепенно устранить проблемы, вызвавшие ошибки, и повторить операцию обновления.</span><span class="sxs-lookup"><span data-stu-id="554b3-185">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="554b3-186">Комментарии</span><span class="sxs-lookup"><span data-stu-id="554b3-186">Remarks</span></span>

<span data-ttu-id="554b3-187">Функции обратного вызова могут быть зарегистрированы для вызова до или после инструкции INSERT, а также до или после обновления.</span><span class="sxs-lookup"><span data-stu-id="554b3-187">Callback functions can be registered to be called before or after insert, and before or after update.</span></span>

<span data-ttu-id="554b3-188">Ограничения размера записи применяются [жетсетколумн](./jetsetcolumn-function.md), а не в общем **жетупдате**.</span><span class="sxs-lookup"><span data-stu-id="554b3-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by **JetUpdate**.</span></span>

<span data-ttu-id="554b3-189">Важно понимать влияние выполнения большого количества операций обновления в рамках одной транзакции.</span><span class="sxs-lookup"><span data-stu-id="554b3-189">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="554b3-190">Каждое обновление базы данных должно быть отслеживанием ядра СУБД в хранилище версий.</span><span class="sxs-lookup"><span data-stu-id="554b3-190">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="554b3-191">Хранилище версий содержит активную запись всех различных версий каждой записи или записи индекса в базе данных, которые могут быть видны всем активным транзакциям.</span><span class="sxs-lookup"><span data-stu-id="554b3-191">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="554b3-192">Эти версии используются для поддержки управления параллелизмом с несколькими версиями, используемого ядром СУБД для поддержки транзакций с использованием изоляции моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="554b3-192">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="554b3-193">После того, как ядро СУБД исчерпало ресурсы, используемые для хранения этих версий, оно больше не сможет принять дальнейшие изменения до тех пор, пока некоторые транзакции не разрешают высвободить эти ресурсы.</span><span class="sxs-lookup"><span data-stu-id="554b3-193">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="554b3-194">Если обработчик находится в этом состоянии, все обновления будут завершаться с JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="554b3-194">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="554b3-195">Ресурсы, доступные ядру СУБД для хранения этих версий, можно контролировать с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с [JET_paramMaxVerPages](./resource-parameters.md) и [JET_paramGlobalMinVerPages](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="554b3-195">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramMaxVerPages](./resource-parameters.md) and [JET_paramGlobalMinVerPages](./resource-parameters.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="554b3-196">Требования</span><span class="sxs-lookup"><span data-stu-id="554b3-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="554b3-197"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="554b3-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="554b3-198">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="554b3-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-199"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="554b3-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="554b3-200">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="554b3-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-201"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="554b3-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="554b3-202">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="554b3-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554b3-203"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="554b3-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="554b3-204">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="554b3-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554b3-205"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="554b3-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="554b3-206">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="554b3-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="554b3-207">См. также:</span><span class="sxs-lookup"><span data-stu-id="554b3-207">See Also</span></span>

[<span data-ttu-id="554b3-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="554b3-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="554b3-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="554b3-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="554b3-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="554b3-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="554b3-211">жетделете</span><span class="sxs-lookup"><span data-stu-id="554b3-211">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="554b3-212">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="554b3-212">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="554b3-213">жетрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="554b3-213">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="554b3-214">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="554b3-214">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="554b3-215">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="554b3-215">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="554b3-216">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="554b3-216">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="554b3-217">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="554b3-217">JetSetColumns</span></span>](./jetsetcolumns-function.md)  
[<span data-ttu-id="554b3-218">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="554b3-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="554b3-219">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="554b3-219">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
