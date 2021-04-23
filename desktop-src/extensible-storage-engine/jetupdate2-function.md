---
description: Дополнительные сведения о функции JetUpdate2
title: Функция JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809005"
---
# <a name="jetupdate2-function"></a><span data-ttu-id="e9213-103">Функция JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="e9213-103">JetUpdate2 Function</span></span>


<span data-ttu-id="e9213-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e9213-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate2-function"></a><span data-ttu-id="e9213-105">Функция JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="e9213-105">JetUpdate2 Function</span></span>

<span data-ttu-id="e9213-106">Функция **JetUpdate2** выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки.</span><span class="sxs-lookup"><span data-stu-id="e9213-106">The **JetUpdate2** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="e9213-107">Эта функция содержит список параметров *грбит* , которые можно задать при выполнении обновления.</span><span class="sxs-lookup"><span data-stu-id="e9213-107">This function contains a list of *grbit* options that can be set while performing an update.</span></span> <span data-ttu-id="e9213-108">Удаление строки таблицы выполняется путем вызова [жетделете](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="e9213-108">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="e9213-109">**Windows server 2003: JetUpdate2** появился в windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9213-109">**Windows Server 2003:  JetUpdate2** is introduced in Windows Server 2003.</span></span>

<span data-ttu-id="e9213-110">**JetUpdate2** является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="e9213-110">**JetUpdate2** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="e9213-111">Обновление начинается с вызова [жетпрепареупдате](./jetprepareupdate-function.md) , а затем путем вызова [жетсетколумн](./jetsetcolumn-function.md) или [жетсетколумнс](./jetsetcolumns-function.md) один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="e9213-111">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="e9213-112">Наконец, для завершения операции обновления вызывается **JetUpdate2** .</span><span class="sxs-lookup"><span data-stu-id="e9213-112">Finally, **JetUpdate2** is called to complete the update operation.</span></span> <span data-ttu-id="e9213-113">Индексы обновляются только в [жетупдате](./jetupdate-function.md) или **JetUpdate2**, а не во время [жетсетколумн](./jetsetcolumn-function.md) или [жетсетколумнс](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="e9213-113">Indexes are updated only by [JetUpdate](./jetupdate-function.md) or **JetUpdate2**, and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e9213-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9213-114">Parameters</span></span>

<span data-ttu-id="e9213-115">*сесид*</span><span class="sxs-lookup"><span data-stu-id="e9213-115">*sesid*</span></span>

<span data-ttu-id="e9213-116">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e9213-116">The session to use for this call.</span></span>

<span data-ttu-id="e9213-117">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e9213-117">*tableid*</span></span>

<span data-ttu-id="e9213-118">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e9213-118">The cursor to use for this call.</span></span>

<span data-ttu-id="e9213-119">*пвбукмарк*</span><span class="sxs-lookup"><span data-stu-id="e9213-119">*pvBookmark*</span></span>

<span data-ttu-id="e9213-120">Указатель на возвращаемую закладку для вставленной строки.</span><span class="sxs-lookup"><span data-stu-id="e9213-120">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="e9213-121">*кббукмарк*</span><span class="sxs-lookup"><span data-stu-id="e9213-121">*cbBookmark*</span></span>

<span data-ttu-id="e9213-122">Размер буфера, на который указывает *пвбукмарк*.</span><span class="sxs-lookup"><span data-stu-id="e9213-122">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="e9213-123">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="e9213-123">*pcbActual*</span></span>

<span data-ttu-id="e9213-124">Возвращаемый размер закладки для вставляемой строки, возвращенной в *пвбукмарк*.</span><span class="sxs-lookup"><span data-stu-id="e9213-124">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

<span data-ttu-id="e9213-125">*грбит*</span><span class="sxs-lookup"><span data-stu-id="e9213-125">*grbit*</span></span>

<span data-ttu-id="e9213-126">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e9213-126">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9213-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e9213-127">Value</span></span></p></th>
<th><p><span data-ttu-id="e9213-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e9213-128">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9213-129">JET_bitUpdateCheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="e9213-129">JET_bitUpdateCheckESE97Compatibility</span></span></p></td>
<td><p><span data-ttu-id="e9213-130">Этот флаг приводит к тому, что обновление возвращает ошибку, если в версии ESE для Windows 2000 не было возможно, что применяет меньшее максимальное число экземпляров столбцов с несколькими значениями в каждой записи, чем в более поздних версиях ESE.</span><span class="sxs-lookup"><span data-stu-id="e9213-130">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="e9213-131">Это важно только для приложений, которые хотят реплицировать данные между приложениями, размещенными в Windows 2000, и приложениями, размещенными на Windows Server 2003 или более поздних версиях ESE.</span><span class="sxs-lookup"><span data-stu-id="e9213-131">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows Server 2003, or later versions of ESE.</span></span> <span data-ttu-id="e9213-132">Это не должно быть необходимо для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="e9213-132">It should not be necessary for most applications.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e9213-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9213-133">Return Value</span></span>

<span data-ttu-id="e9213-134">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="e9213-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e9213-135">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e9213-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9213-136">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e9213-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="e9213-137">Описание</span><span class="sxs-lookup"><span data-stu-id="e9213-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9213-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e9213-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e9213-139">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e9213-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-140">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="e9213-140">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="e9213-141">Заданный буфер для закладки записи недостаточно велик для хранения закладки записи.</span><span class="sxs-lookup"><span data-stu-id="e9213-141">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-142">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e9213-142">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e9213-143">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="e9213-143">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-144">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="e9213-144">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="e9213-145">Операция обновления требует увеличения размера файла базы данных или выделения файла журнала, но диск, на котором находится файл базы данных или ряд журналов, заполнен.</span><span class="sxs-lookup"><span data-stu-id="e9213-145">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="e9213-146">Кроме того, файл базы данных находится на томе в формате FAT32, а файл базы данных уже 4GBytes, ограничение на количество файлов для FAT32.</span><span class="sxs-lookup"><span data-stu-id="e9213-146">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e9213-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e9213-148">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="e9213-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e9213-149"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e9213-149"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e9213-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e9213-151">Данный параметр <em>подготовки</em> в функции <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a> не является допустимым флагом.</span><span class="sxs-lookup"><span data-stu-id="e9213-151">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-152">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="e9213-152">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="e9213-153">Ключ индекса для этой записи является дубликатом другого ключа индекса для другой записи, уже наданнымся в таблице, и индекс не допускает дублирования.</span><span class="sxs-lookup"><span data-stu-id="e9213-153">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-154">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="e9213-154">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="e9213-155">Вставленная или обновленная запись имеет один или несколько индексов, для которых созданный ключ превысил максимально допустимый размер.</span><span class="sxs-lookup"><span data-stu-id="e9213-155">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="e9213-156">В результате операция не смогла предотвратить усечение ключа.</span><span class="sxs-lookup"><span data-stu-id="e9213-156">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-157">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="e9213-157">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="e9213-158">Вставленная или обновленная запись имеет индексируемый многозначный столбец с двумя или более значениями, идентичными в пределах ключа максимальной длины, установленного для индекса.</span><span class="sxs-lookup"><span data-stu-id="e9213-158">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="e9213-159">В результате запись содержит две идентичные записи в индексе, что недопустимо.</span><span class="sxs-lookup"><span data-stu-id="e9213-159">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e9213-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e9213-161">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="e9213-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-162">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="e9213-162">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="e9213-163">Один или несколько столбцов вставляемой записи или в обновленном состоянии заменяемой записи имеют <strong>значение NULL</strong> , что нарушает определенное ограничение для этих столбцов.</span><span class="sxs-lookup"><span data-stu-id="e9213-163">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-164">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="e9213-164">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="e9213-165">Один или несколько индексов не позволяют разрешить ключ <strong>null</strong> , а вставленное или обновленное состояние заменяемой записи нарушает это заданное ограничение.</span><span class="sxs-lookup"><span data-stu-id="e9213-165">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-166">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="e9213-166">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="e9213-167">Операция замены записи обновила первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="e9213-167">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="e9213-168">Обновления первичных ключевых столбцов должны выполняться путем удаления существующей записи и вставки новой записи с нужными данными.</span><span class="sxs-lookup"><span data-stu-id="e9213-168">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-169">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e9213-169">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e9213-170">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="e9213-170">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-171">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e9213-171">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e9213-172">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="e9213-172">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e9213-173"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e9213-173"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e9213-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e9213-175">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="e9213-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-176">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="e9213-176">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="e9213-177"><a href="gg269339(v=exchg.10).md">Жетпрепареупдате</a> был вызван с JET_prepCancel, но курсор не был в подготовленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e9213-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-178">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e9213-178">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e9213-179">Операция замены записи, для которой не была выделена блокировка записи, может столкнуться с конфликтом записи во время обновления.</span><span class="sxs-lookup"><span data-stu-id="e9213-179">A record replacement operation for which a write lock was not already allocated can encounter a write conflict at the time of update.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e9213-180">При успешном выполнении операция открытия обновления курсора завершается.</span><span class="sxs-lookup"><span data-stu-id="e9213-180">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="e9213-181">Если для таблицы определен автоматически увеличивающийся столбец, то это значение устанавливается для вставленных записей.</span><span class="sxs-lookup"><span data-stu-id="e9213-181">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="e9213-182">Если для таблицы определен столбец версии, то его значение инициализируется для вновь вставленных записей или увеличивается каждый раз при замене записи.</span><span class="sxs-lookup"><span data-stu-id="e9213-182">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="e9213-183">Обновляются все индексы, включая кластеризованные и некластеризованные индексы.</span><span class="sxs-lookup"><span data-stu-id="e9213-183">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="e9213-184">В случае сбоя изменения какого либо типа не вносятся в базу данных.</span><span class="sxs-lookup"><span data-stu-id="e9213-184">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="e9213-185">Перед вставкой и до замены функции обратного вызова могут быть вызваны, но после вызовов INSERT и After replace не будут вызываться, так как Последнее не может привести к сбою обновления.</span><span class="sxs-lookup"><span data-stu-id="e9213-185">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="e9213-186">Буфер копирования курсора остается в подготовленном состоянии, чтобы можно было постепенно устранить проблемы, вызвавшие ошибки, и повторить операцию обновления.</span><span class="sxs-lookup"><span data-stu-id="e9213-186">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e9213-187">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9213-187">Remarks</span></span>

<span data-ttu-id="e9213-188">Ограничения размера записи применяются [жетсетколумн](./jetsetcolumn-function.md), а не в общем [жетупдате](./jetupdate-function.md).</span><span class="sxs-lookup"><span data-stu-id="e9213-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by [JetUpdate](./jetupdate-function.md).</span></span> <span data-ttu-id="e9213-189">Единственным исключением является использование флага совместимости JET_bitUpdateCheckESE97Compatibility.</span><span class="sxs-lookup"><span data-stu-id="e9213-189">The only exception is when the JET_bitUpdateCheckESE97Compatibility compatibility flag is being used.</span></span> <span data-ttu-id="e9213-190">В этом случае проверяется вся запись, так как отдельная операция [жетсетколумн](./jetsetcolumn-function.md) , которая превышает это ограничение, может быть компенсироваться последующим вызовом [жетсетколумн](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="e9213-190">In this case, the whole record is checked since an individual [JetSetColumn](./jetsetcolumn-function.md) operation that exceeded the limit may be compensated by a subsequent call to [JetSetColumn](./jetsetcolumn-function.md).</span></span>

<span data-ttu-id="e9213-191">Дополнительные сведения см. в разделе "Примечания" в [жетупдате](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e9213-191">See the Remarks section in [JetUpdate](./jetupdate-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e9213-192">Требования</span><span class="sxs-lookup"><span data-stu-id="e9213-192">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9213-193"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e9213-193"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e9213-194">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e9213-194">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-195"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e9213-195"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e9213-196">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9213-196">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-197"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e9213-197"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e9213-198">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e9213-198">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9213-199"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="e9213-199"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e9213-200">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e9213-200">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9213-201"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="e9213-201"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e9213-202">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e9213-202">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e9213-203">См. также:</span><span class="sxs-lookup"><span data-stu-id="e9213-203">See Also</span></span>

[<span data-ttu-id="e9213-204">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e9213-204">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e9213-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e9213-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e9213-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e9213-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e9213-207">жетделете</span><span class="sxs-lookup"><span data-stu-id="e9213-207">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="e9213-208">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="e9213-208">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="e9213-209">жетрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="e9213-209">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="e9213-210">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="e9213-210">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="e9213-211">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="e9213-211">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="e9213-212">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="e9213-212">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="e9213-213">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="e9213-213">JetSetColumns</span></span>](./jetsetcolumns-function.md)
