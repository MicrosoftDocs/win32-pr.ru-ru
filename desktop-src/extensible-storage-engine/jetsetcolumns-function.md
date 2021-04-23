---
description: Дополнительные сведения о функции Жетсетколумнс
title: Функция JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143516"
---
# <a name="jetsetcolumns-function"></a><span data-ttu-id="f187d-103">Функция JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="f187d-103">JetSetColumns Function</span></span>


<span data-ttu-id="f187d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f187d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumns-function"></a><span data-ttu-id="f187d-105">Функция JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="f187d-105">JetSetColumns Function</span></span>

<span data-ttu-id="f187d-106">Функция **жетсетколумнс** похожа на поведение [жетсетколумн](./jetsetcolumn-function.md) , но позволяет приложению задавать несколько значений столбцов в одной операции.</span><span class="sxs-lookup"><span data-stu-id="f187d-106">The **JetSetColumns** function is similar in behavior to [JetSetColumn](./jetsetcolumn-function.md) but allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="f187d-107">Массив структур [JET_SETCOLUMN](./jet-setcolumn-structure.md) используется для описания набора значений столбцов, которые необходимо задать, а также для описания входных буферов для каждого устанавливаемого значения столбца.</span><span class="sxs-lookup"><span data-stu-id="f187d-107">An array of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="f187d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f187d-108">Parameters</span></span>

<span data-ttu-id="f187d-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="f187d-109">*sesid*</span></span>

<span data-ttu-id="f187d-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f187d-110">The session to use for this call.</span></span>

<span data-ttu-id="f187d-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="f187d-111">*tableid*</span></span>

<span data-ttu-id="f187d-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f187d-112">The cursor to use for this call.</span></span>

<span data-ttu-id="f187d-113">*псетколумн*</span><span class="sxs-lookup"><span data-stu-id="f187d-113">*psetcolumn*</span></span>

<span data-ttu-id="f187d-114">Указатель на массив из одной или нескольких структур [JET_SETCOLUMN](./jet-setcolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="f187d-114">A pointer to an array of one or more [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures.</span></span> <span data-ttu-id="f187d-115">Каждая структура включает в себя описания того, какое значение столбца следует задать и откуда получать данные о столбцах для задания.</span><span class="sxs-lookup"><span data-stu-id="f187d-115">Each structure includes descriptions of which column value to set and from where to get column data to set.</span></span>

<span data-ttu-id="f187d-116">*ксетколумн*</span><span class="sxs-lookup"><span data-stu-id="f187d-116">*csetcolumn*</span></span>

<span data-ttu-id="f187d-117">Число структур [JET_SETCOLUMN](./jet-setcolumn-structure.md) в массиве, заданном параметром *псетколумн*.</span><span class="sxs-lookup"><span data-stu-id="f187d-117">The number of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures in the array given by *psetcolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="f187d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f187d-118">Return Value</span></span>

<span data-ttu-id="f187d-119">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="f187d-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f187d-120">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f187d-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f187d-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f187d-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="f187d-122">Описание</span><span class="sxs-lookup"><span data-stu-id="f187d-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f187d-123">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="f187d-123">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="f187d-124">Указанный идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="f187d-124">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f187d-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f187d-126">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="f187d-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-127">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="f187d-127">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="f187d-128">То же, что и JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="f187d-128">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-129">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="f187d-129">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="f187d-130">Столбец, описываемый данным <em>columnid</em> , не существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="f187d-130">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-131">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="f187d-131">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="f187d-132">Предпринята недопустимая попытка обновить значение Long во время операции вставки копирования удаление исходного обновления.</span><span class="sxs-lookup"><span data-stu-id="f187d-132">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-133">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="f187d-133">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="f187d-134">Данные значений столбцов, заданных во входном буфере, превышают ограничение по размеру либо естественным для столбца фиксированной длины, либо настроены для текстовых или двоичных столбцов фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="f187d-134">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="f187d-135">Эта ошибка также возвращается при передаче более 1024 байт данных для длинного столбца и установке флага JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="f187d-135">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f187d-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f187d-137">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="f187d-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f187d-138">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f187d-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="f187d-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="f187d-140">Заданный размер данных значения столбца не соответствует типу данных фиксированной длины, который является естественным.</span><span class="sxs-lookup"><span data-stu-id="f187d-140">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-141">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="f187d-141">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="f187d-142">Предпринята недопустимая попытка обновить столбец автоинкремента во время операции вставки или обновления либо обновить столбец версии во время операции замены.</span><span class="sxs-lookup"><span data-stu-id="f187d-142">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-143">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="f187d-143">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="f187d-144">Указанные параметры неизвестны или являются недопустимым сочетанием известных битовых параметров.</span><span class="sxs-lookup"><span data-stu-id="f187d-144">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f187d-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f187d-146">Заданный псетинфо- &gt; кбструкт не является допустимым размером для структуры <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="f187d-146">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-147">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="f187d-147">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f187d-148">Операция задания столбца попыталась создать повторяющееся значение и указать либо JET_bitSetUniqueMultiValues, либо JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="f187d-148">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-149">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f187d-149">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f187d-150">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="f187d-150">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-151">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="f187d-151">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f187d-152">Предпринята недопустимая попытка обновить значение длинного столбца, если вызывающий сеанс не был в транзакции.</span><span class="sxs-lookup"><span data-stu-id="f187d-152">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-153">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="f187d-153">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="f187d-154">Предпринята недопустимая попытка установить ненулевое значение NULL для столбца.</span><span class="sxs-lookup"><span data-stu-id="f187d-154">An illegal attempt was made to set a non-NULL column to NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-155">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="f187d-155">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="f187d-156">Значение столбца не может быть присвоено значению во входном буфере, так как оно привело к превышению ограничения на размер страницы.</span><span class="sxs-lookup"><span data-stu-id="f187d-156">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="f187d-157">Столбцы типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> можно хранить отдельно от оставшихся данных записи.</span><span class="sxs-lookup"><span data-stu-id="f187d-157">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="f187d-158">Однако другие столбцы должны храниться вместе с записью, что может привести к превышению ограничения на размер записи.</span><span class="sxs-lookup"><span data-stu-id="f187d-158">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="f187d-159">Даже для длинных столбцов требуется 5-байтное пространство внутри записи в качестве компоновки, что также может привести к возвращению JET_errRecordTooBig.</span><span class="sxs-lookup"><span data-stu-id="f187d-159">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f187d-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f187d-161">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="f187d-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f187d-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f187d-163">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="f187d-163">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="f187d-164">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f187d-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f187d-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f187d-166">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="f187d-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-167">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="f187d-167">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="f187d-168">Курсор в настоящее время не находится в процессе вставки новой записи или обновления существующей записи.</span><span class="sxs-lookup"><span data-stu-id="f187d-168">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="f187d-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="f187d-170">Значение столбца во входном буфере превысило максимальную заданную длину для столбца переменной длины и было усечено.</span><span class="sxs-lookup"><span data-stu-id="f187d-170">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f187d-171">При успешном выполнении для каждого столбца, описанного в псетколумнс, требуемая часть значения столбца задается данными, скопированными из входного буфера.</span><span class="sxs-lookup"><span data-stu-id="f187d-171">On success, for each column described in the psetcolumns, the desired portion of the column value is set with data copied from the input buffer.</span></span> <span data-ttu-id="f187d-172">Набор данных столбца мог быть усечен, если превышена максимальная длина, указанная для столбца переменной длины.</span><span class="sxs-lookup"><span data-stu-id="f187d-172">The column data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="f187d-173">В случае сбоя положение курсора остается неизменным, и данные значения столбца не обновляются в буфере копирования.</span><span class="sxs-lookup"><span data-stu-id="f187d-173">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f187d-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f187d-174">Remarks</span></span>

<span data-ttu-id="f187d-175">Если любая отдельная операция с набором столбцов возвращает ошибку, то вся операция **жетсетколумнс** возвратит ошибку.</span><span class="sxs-lookup"><span data-stu-id="f187d-175">If any individual set column operation returns an error then the whole **JetSetColumns** operation will return an error.</span></span> <span data-ttu-id="f187d-176">Обычно предупреждения возвращаются в псетколумнс- \> Error, а не в коде возврата этой функции.</span><span class="sxs-lookup"><span data-stu-id="f187d-176">Warnings, in general, are returned in the psetcolumns-\>error and not in the return code from this function.</span></span> <span data-ttu-id="f187d-177">Однако если в последнем наборе столбцов есть предупреждение, это предупреждение будет возвращаться из самого **жетсетколумнс** .</span><span class="sxs-lookup"><span data-stu-id="f187d-177">However, if the last column set has a warning, then this warning will be returned from **JetSetColumns** itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f187d-178">Требования</span><span class="sxs-lookup"><span data-stu-id="f187d-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f187d-179"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f187d-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f187d-180">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f187d-180">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-181"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f187d-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f187d-182">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f187d-182">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-183"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f187d-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f187d-184">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f187d-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f187d-185"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="f187d-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f187d-186">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f187d-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f187d-187"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="f187d-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f187d-188">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f187d-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f187d-189">См. также:</span><span class="sxs-lookup"><span data-stu-id="f187d-189">See Also</span></span>

[<span data-ttu-id="f187d-190">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="f187d-190">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="f187d-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f187d-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f187d-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f187d-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f187d-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f187d-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f187d-194">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="f187d-194">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="f187d-195">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="f187d-195">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="f187d-196">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="f187d-196">JetSetColumn</span></span>](./jetsetcolumn-function.md)
