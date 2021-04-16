---
description: Дополнительные сведения о функции Жетретриевеколумн
title: Функция JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703085"
---
# <a name="jetretrievecolumn-function"></a><span data-ttu-id="2585b-103">Функция JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="2585b-103">JetRetrieveColumn Function</span></span>


<span data-ttu-id="2585b-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2585b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumn-function"></a><span data-ttu-id="2585b-105">Функция JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="2585b-105">JetRetrieveColumn Function</span></span>

<span data-ttu-id="2585b-106">Функция **жетретриевеколумн** извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="2585b-106">The **JetRetrieveColumn** function retrieves a single column value from the current record.</span></span> <span data-ttu-id="2585b-107">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="2585b-107">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="2585b-108">Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора.</span><span class="sxs-lookup"><span data-stu-id="2585b-108">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="2585b-109">Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="2585b-109">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="2585b-110">Помимо получения фактического значения столбца, **жетретриевеколумн** можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</span><span class="sxs-lookup"><span data-stu-id="2585b-110">In addition to retrieving the actual column value, **JetRetrieveColumn** can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="2585b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2585b-111">Parameters</span></span>

<span data-ttu-id="2585b-112">*сесид*</span><span class="sxs-lookup"><span data-stu-id="2585b-112">*sesid*</span></span>

<span data-ttu-id="2585b-113">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="2585b-113">The session to use for this call.</span></span>

<span data-ttu-id="2585b-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="2585b-114">*tableid*</span></span>

<span data-ttu-id="2585b-115">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="2585b-115">The cursor to use for this call.</span></span>

<span data-ttu-id="2585b-116">*columnid*</span><span class="sxs-lookup"><span data-stu-id="2585b-116">*columnid*</span></span>

<span data-ttu-id="2585b-117">[JET_COLUMNID](./jet-columnid.md) столбца для извлечения.</span><span class="sxs-lookup"><span data-stu-id="2585b-117">The [JET_COLUMNID](./jet-columnid.md) of the column to retrieve.</span></span>

<span data-ttu-id="2585b-118">Можно указать значение *columnid* , равное 0 (нулю), которое само по себе не относится к какому-либо отдельному столбцу.</span><span class="sxs-lookup"><span data-stu-id="2585b-118">A *columnid* value of 0 (zero) can be given which does not itself refer to any individual column.</span></span> <span data-ttu-id="2585b-119">Если задано значение *columnid* 0 (ноль), все столбцы с тегами, разреженные и Многозначные столбцы рассматриваются как один столбец.</span><span class="sxs-lookup"><span data-stu-id="2585b-119">When *columnid* 0 (zero) is given, all tagged columns, sparse, and multi-valued columns are treated as a single column.</span></span> <span data-ttu-id="2585b-120">Это упрощает извлечение всех разреженных столбцов, имеющихся в записи.</span><span class="sxs-lookup"><span data-stu-id="2585b-120">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="2585b-121">*пвдата*</span><span class="sxs-lookup"><span data-stu-id="2585b-121">*pvData*</span></span>

<span data-ttu-id="2585b-122">Выходной буфер, который получает значение столбца.</span><span class="sxs-lookup"><span data-stu-id="2585b-122">The output buffer that receives the column value.</span></span>

<span data-ttu-id="2585b-123">*cbData*</span><span class="sxs-lookup"><span data-stu-id="2585b-123">*cbData*</span></span>

<span data-ttu-id="2585b-124">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="2585b-124">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="2585b-125">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="2585b-125">*pcbActual*</span></span>

<span data-ttu-id="2585b-126">Получает фактический размер значения столбца в байтах.</span><span class="sxs-lookup"><span data-stu-id="2585b-126">Receives the actual size, in bytes, of the column value.</span></span>

<span data-ttu-id="2585b-127">Если этот параметр имеет **значение NULL**, фактический размер значения столбца не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="2585b-127">If this parameter is **NULL**, then the actual size of the column value will not be returned.</span></span>

<span data-ttu-id="2585b-128">*грбит*</span><span class="sxs-lookup"><span data-stu-id="2585b-128">*grbit*</span></span>

<span data-ttu-id="2585b-129">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, в том числе ноль или более следующих:</span><span class="sxs-lookup"><span data-stu-id="2585b-129">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2585b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2585b-130">Value</span></span></p></th>
<th><p><span data-ttu-id="2585b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2585b-131">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2585b-132">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="2585b-132">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="2585b-133">Этот флаг заставляет столбец извлечь измененное значение, а не исходное значение.</span><span class="sxs-lookup"><span data-stu-id="2585b-133">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="2585b-134">Если значение не было изменено, то извлекается исходное значение.</span><span class="sxs-lookup"><span data-stu-id="2585b-134">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="2585b-135">Таким образом, значение, которое еще не было вставлено или Обновлено, может быть получено во время операции вставки или обновления записи.</span><span class="sxs-lookup"><span data-stu-id="2585b-135">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-136">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="2585b-136">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="2585b-137">Этот параметр используется для извлечения значений столбцов из индекса, если это возможно, без обращения к записи.</span><span class="sxs-lookup"><span data-stu-id="2585b-137">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="2585b-138">Таким образом, необязательная Загрузка записей может быть продолжена, если нужные данные будут доступны из самих записей индекса.</span><span class="sxs-lookup"><span data-stu-id="2585b-138">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="2585b-139">В случаях, когда исходное значение столбца не может быть получено из индекса из-за необратимых преобразований или усечения данных, доступ к записи будет осуществляться, а данные будут извлечены как обычные.</span><span class="sxs-lookup"><span data-stu-id="2585b-139">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="2585b-140">Это параметр производительности, и его следует указывать только в том случае, если вероятно, что значение столбца может быть извлечено из индекса.</span><span class="sxs-lookup"><span data-stu-id="2585b-140">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="2585b-141">Этот параметр не следует указывать, если текущим индексом является кластеризованный индекс, поскольку записи индекса для кластеризованного или первичного индекса являются записями.</span><span class="sxs-lookup"><span data-stu-id="2585b-141">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="2585b-142">Этот бит не может быть установлен, если также задано JET_bitRetrieveFromPrimaryBookmark.</span><span class="sxs-lookup"><span data-stu-id="2585b-142">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-143">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="2585b-143">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="2585b-144">Этот параметр используется для извлечения значений столбцов из закладки индекса и может отличаться от значения индекса, если столбец отображается как в первичном, так и в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="2585b-144">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="2585b-145">Этот параметр не следует указывать, если текущий индекс является кластеризованным или первичным индексом.</span><span class="sxs-lookup"><span data-stu-id="2585b-145">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="2585b-146">Этот бит не может быть установлен, если также задано JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="2585b-146">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-147">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="2585b-147">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="2585b-148">Этот параметр используется для получения порядкового номера значения столбца с несколькими значениями в претинфо- &gt; итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="2585b-148">This option is used to retrieve the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="2585b-149">Поле Итагсекуенце обычно является входным для извлечения значений столбца с несколькими значениями из записи.</span><span class="sxs-lookup"><span data-stu-id="2585b-149">The itagSequence field is commonly an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="2585b-150">Однако при извлечении значений из индекса также можно связать запись индекса с определенным порядковым номером и получить также этот порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="2585b-150">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="2585b-151">Получение порядкового номера может быть дорогостоящей операцией, и ее следует выполнять только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="2585b-151">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-152">JET_bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="2585b-152">JET_bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="2585b-153">Этот параметр используется для извлечения значений <strong>null</strong> в столбцах с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="2585b-153">This option is used to retrieve multi-valued column <strong>NULL</strong> values.</span></span> <span data-ttu-id="2585b-154">Если этот параметр не указан, значения <strong>null</strong> в столбцах с несколькими значениями будут пропускаться автоматически.</span><span class="sxs-lookup"><span data-stu-id="2585b-154">If this option is not specified, multi-valued column <strong>NULL</strong> values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-155">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="2585b-155">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="2585b-156">Этот параметр влияет только на столбцы с несколькими значениями и приводит к возвращению значения <strong>null</strong> , если запрошенный порядковый номер равен 1, а значения для столбца в записи не заданы.</span><span class="sxs-lookup"><span data-stu-id="2585b-156">This option affects only multi-valued columns and causes a <strong>NULL</strong> value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-157">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="2585b-157">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="2585b-158">Этот флаг предназначен только для внутреннего использования и не предназначен для использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="2585b-158">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-159">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="2585b-159">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="2585b-160">Этот флаг предназначен только для внутреннего использования и не предназначен для использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="2585b-160">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-161">JET_bitRetrieveTuple</span><span class="sxs-lookup"><span data-stu-id="2585b-161">JET_bitRetrieveTuple</span></span></p></td>
<td><p><span data-ttu-id="2585b-162">Этот флаг разрешает извлечение сегмента кортежа в индексе.</span><span class="sxs-lookup"><span data-stu-id="2585b-162">This flag will allow the retrieval of a tuple segment of the index.</span></span> <span data-ttu-id="2585b-163">Этот бит должен быть указан с JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="2585b-163">This bit must be specified with JET_bitRetrieveFromIndex.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2585b-164">*претинфо*</span><span class="sxs-lookup"><span data-stu-id="2585b-164">*pretinfo*</span></span>

<span data-ttu-id="2585b-165">Если *претинфо* имеет **значение NULL** , функция ведет себя так, как будто *итагсекуенце* равен 1 и *иблонгвалуе* 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="2585b-165">If *pretinfo* is give as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="2585b-166">Это приводит к извлечению столбца для получения первого значения многозначного столбца, а также для получения длинных данных со смещением 0 (нулем).</span><span class="sxs-lookup"><span data-stu-id="2585b-166">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

<span data-ttu-id="2585b-167">Этот параметр используется для предоставления одного или нескольких из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="2585b-167">This parameter is used to provide one or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2585b-168">Значение</span><span class="sxs-lookup"><span data-stu-id="2585b-168">Value</span></span></p></th>
<th><p><span data-ttu-id="2585b-169">Значение</span><span class="sxs-lookup"><span data-stu-id="2585b-169">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2585b-170">иблонгвалуе</span><span class="sxs-lookup"><span data-stu-id="2585b-170">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="2585b-171">Предоставляет двоичное смещение в длинном значении столбца при извлечении части значения столбца.</span><span class="sxs-lookup"><span data-stu-id="2585b-171">Gives a binary offset into a long column value when retrieving a portion of a column value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-172">итагсекуенце</span><span class="sxs-lookup"><span data-stu-id="2585b-172">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="2585b-173">Возвращает порядковый номер нужного значения столбца с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="2585b-173">Gives the sequence number of the desired multi-valued column value.</span></span> <span data-ttu-id="2585b-174">Обратите внимание, что это поле задается только в том случае, если указано JET_bitRetrieveTag.</span><span class="sxs-lookup"><span data-stu-id="2585b-174">Note that this field is only set if the JET_bitRetrieveTag is specified.</span></span> <span data-ttu-id="2585b-175">В противном случае он не изменяется.</span><span class="sxs-lookup"><span data-stu-id="2585b-175">Otherwise, it is unmodified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-176">колумниднексттагжед</span><span class="sxs-lookup"><span data-stu-id="2585b-176">columnidNextTagged</span></span></p></td>
<td><p><span data-ttu-id="2585b-177">Возвращает идентификатор возвращенного значения столбца при извлечении всех столбцов с тегами, разреженных и многозначных, с использованием передачи <em>columnid</em> 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="2585b-177">Returns the column ID of the returned column value when retrieving all tagged, sparse and multi-valued, columns using passing <em>columnid</em> of 0 (zero).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2585b-178">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2585b-178">Return Value</span></span>

<span data-ttu-id="2585b-179">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="2585b-179">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2585b-180">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2585b-180">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2585b-181">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2585b-181">Return code</span></span></p></th>
<th><p><span data-ttu-id="2585b-182">Описание</span><span class="sxs-lookup"><span data-stu-id="2585b-182">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2585b-183">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2585b-183">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2585b-184">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2585b-184">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-185">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="2585b-185">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="2585b-186">Указанный идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="2585b-186">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-187">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="2585b-187">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="2585b-188">Недопустимое значение порядкового номера столбца с несколькими значениями было передано в претинфо- &gt; итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="2585b-188">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="2585b-189">Допустимые значения для порядковых номеров значений столбца с несколькими значениями: 1 или более.</span><span class="sxs-lookup"><span data-stu-id="2585b-189">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="2585b-190">Значение 0 (ноль) недопустимо для этой функции.</span><span class="sxs-lookup"><span data-stu-id="2585b-190">A value of 0 (zero) is invalid for this function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2585b-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2585b-192">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="2585b-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-193">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="2585b-193">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="2585b-194">Столбец, описываемый данным <em>columnid</em> , не существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="2585b-194">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-195">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="2585b-195">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="2585b-196">Столбцы, индексируемые как подстроки, не могут быть извлечены из индекса, так как в каждой записи индекса обычно содержится только небольшая часть столбца.</span><span class="sxs-lookup"><span data-stu-id="2585b-196">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-197">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2585b-197">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2585b-198">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="2585b-198">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="2585b-199">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="2585b-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-200">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="2585b-200">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="2585b-201">В некоторых случаях буфер, заданный для столбца получения, должен иметь достаточный размер, чтобы вернуть любой объем значения столбца.</span><span class="sxs-lookup"><span data-stu-id="2585b-201">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="2585b-202">Например, депонированные обновляемые столбцы настраиваются таким образом, чтобы они были согласованы в транзакционном контексте вызывающего сеанса, и эта корректировка требует наличия буфера, предоставленного вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="2585b-202">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="2585b-203">Если предоставлено недостаточное место в буфере, возвращается JET_errInvalidBufferSize и данные столбца не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="2585b-203">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-204">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2585b-204">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2585b-205">Один или несколько указанных параметров неверны.</span><span class="sxs-lookup"><span data-stu-id="2585b-205">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="2585b-206">Это может произойти, если размер ретинфо. Кбструкт меньше, чем <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="2585b-206">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-207">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="2585b-207">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="2585b-208">Указанные параметры неизвестны или являются недопустимым сочетанием известных битовых параметров.</span><span class="sxs-lookup"><span data-stu-id="2585b-208">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-209">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="2585b-209">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="2585b-210">Курсор не располагается на записи.</span><span class="sxs-lookup"><span data-stu-id="2585b-210">The cursor is not positioned on a record.</span></span> <span data-ttu-id="2585b-211">Это может произойти по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="2585b-211">This can happen for many different reasons.</span></span> <span data-ttu-id="2585b-212">Например, это произойдет, если курсор находится в данный момент после последней записи в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="2585b-212">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-213">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2585b-213">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2585b-214">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="2585b-214">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-215">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2585b-215">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2585b-216">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="2585b-216">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-217">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="2585b-217">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="2585b-218">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="2585b-218">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="2585b-219"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="2585b-219"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-220">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2585b-220">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2585b-221">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="2585b-221">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-222">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="2585b-222">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="2585b-223">Не удалось получить значение полного столбца, так как размер данного буфера меньше размера столбца.</span><span class="sxs-lookup"><span data-stu-id="2585b-223">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-224">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="2585b-224">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="2585b-225">Полученное значение столбца равно <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="2585b-225">The column value retrieved is <strong>NULL</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2585b-226">При успешном выполнении значение столбца для данного столбца копируется в заданный буфер.</span><span class="sxs-lookup"><span data-stu-id="2585b-226">On success, the column value for the given column, is copied into the given buffer.</span></span> <span data-ttu-id="2585b-227">Значение меньше всех значений столбца копируется с предупреждением, JET_wrnBufferTruncated возвращается.</span><span class="sxs-lookup"><span data-stu-id="2585b-227">Less than all of the column value is copied with the warning JET_wrnBufferTruncated is returned.</span></span> <span data-ttu-id="2585b-228">Если было задано значение *пкбактуал* , возвращается фактический размер значения столбца.</span><span class="sxs-lookup"><span data-stu-id="2585b-228">If the *pcbActual* was given, the actual size of the column value is returned.</span></span> <span data-ttu-id="2585b-229">Обратите внимание, что значения **null** имеют нулевую длину и, таким словами, задают возвращаемый размер равным 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="2585b-229">Note that **NULL** values have 0 (zero) length and will thus set the returned size to 0 (zero).</span></span> <span data-ttu-id="2585b-230">Если извлеченным столбцом был многозначный столбец, а JET_bitReturnTag *претинфо* был задан как параметр, то порядковый номер значения столбца возвращается в претинфо- \> итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="2585b-230">If the column retrieved was a multi-valued column, and *pretinfo* was given, and JET_bitReturnTag was set as an option, then the sequence number of the column value is returned in pretinfo-\>itagSequence.</span></span>

<span data-ttu-id="2585b-231">В случае сбоя положение курсора остается неизменным и данные не копируются в предоставленный буфер.</span><span class="sxs-lookup"><span data-stu-id="2585b-231">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2585b-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2585b-232">Remarks</span></span>

<span data-ttu-id="2585b-233">Этот вызов используется только один раз для получения данных фиксированного или известного размера для столбцов, не являющихся многозначными.</span><span class="sxs-lookup"><span data-stu-id="2585b-233">This call is used just once to retrieve data of fixed or known size for non-multi-valued columns.</span></span> <span data-ttu-id="2585b-234">Однако, если данные столбца имеют неизвестный размер, этот вызов обычно используется дважды.</span><span class="sxs-lookup"><span data-stu-id="2585b-234">However, when column data is of unknown size, this call is typically used twice.</span></span> <span data-ttu-id="2585b-235">Сначала вызывается метод, чтобы определить размер данных, чтобы он мог выделить необходимое дисковое пространство.</span><span class="sxs-lookup"><span data-stu-id="2585b-235">It is called first to determine the size of the data so it can allocate the necessary storage space.</span></span> <span data-ttu-id="2585b-236">Затем выполняется тот же вызов для получения данных столбца.</span><span class="sxs-lookup"><span data-stu-id="2585b-236">Then, the same call is made again to retrieve the column data.</span></span> <span data-ttu-id="2585b-237">Если фактическое число значений неизвестно, так как столбец является многозначным, вызов обычно используется три раза.</span><span class="sxs-lookup"><span data-stu-id="2585b-237">When the actual number of values is unknown, because a column is multi-valued, the call is typically used three times.</span></span> <span data-ttu-id="2585b-238">Сначала необходимо получить количество значений, а затем дважды больше, чтобы выделить память и получить реальные данные.</span><span class="sxs-lookup"><span data-stu-id="2585b-238">First to get the number of values and then twice more to allocate storage and retrieve the actual data.</span></span>

<span data-ttu-id="2585b-239">Извлечение всех значений для многозначного столбца можно выполнить, повторно вызвав эту функцию с претинфо- \> итагсекуенце значением, начинающимся с 1 и увеличивая при каждом последующем вызове.</span><span class="sxs-lookup"><span data-stu-id="2585b-239">Retrieving all the values for a multi-valued column can be done by repeatedly calling this function with a pretinfo-\>itagSequence value beginning at 1 and increasing on each subsequent call.</span></span> <span data-ttu-id="2585b-240">Значение последнего столбца известно для извлечения при возвращении JET_wrnColumnNull из функции.</span><span class="sxs-lookup"><span data-stu-id="2585b-240">The last column value is known to be retrieved when a JET_wrnColumnNull is returned from the function.</span></span> <span data-ttu-id="2585b-241">Обратите внимание, что этот метод не может быть выполнен, если в последовательности значений столбца с несколькими значениями заданы явные значения **null** , так как эти значения будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="2585b-241">Note that this method cannot be done if the multi-value column has explicit **NULL** values set in its value sequence, since these values would be skipped.</span></span> <span data-ttu-id="2585b-242">Если приложению требуется получить все значения столбцов с несколькими значениями, в том числе явно заданные в **null**, необходимо использовать [жетретриевеколумнс](./jetretrievecolumns-function.md) вместо **жетретриевеколумн**.</span><span class="sxs-lookup"><span data-stu-id="2585b-242">If an application desires to retrieve all multi-valued column values, including those explicitly set to **NULL**, then [JetRetrieveColumns](./jetretrievecolumns-function.md) must be used instead of **JetRetrieveColumn**.</span></span> <span data-ttu-id="2585b-243">Обратите внимание, что эта функция не возвращает число значений для многозначной функции, если задано значение *итагсекуенце* 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="2585b-243">Note that this function does not return the number of values for a multi-valued function when an *itagSequence* value of 0 (zero) is given.</span></span> <span data-ttu-id="2585b-244">Только [жетретриевеколумнс](./jetretrievecolumns-function.md) возвращает количество значений значения столбца, если передано значение *итагсекуенце* 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="2585b-244">Only [JetRetrieveColumns](./jetretrievecolumns-function.md) will return the number of values of a column value when an *itagSequence* value of 0 (zero) is passed.</span></span>

<span data-ttu-id="2585b-245">Если эта функция вызывается на уровне транзакции 0 (ноль), например, вызывающий сеанс не находится в транзакции, то транзакция открывается и закрывается в функции.</span><span class="sxs-lookup"><span data-stu-id="2585b-245">If this function is called at transaction level 0 (zero), for example, the calling session is not itself in a transaction, then a transaction is opened and closed within the function.</span></span> <span data-ttu-id="2585b-246">Целью этого является возврат последовательных результатов в случае, если длинное значение охватывает страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="2585b-246">The purpose of this is to return consistent results in the case that a long value spans database pages.</span></span> <span data-ttu-id="2585b-247">Обратите внимание, что транзакция освобождается между вызовами функций и серией вызовов этой функции, если сеанс не находится в транзакции, может возвращать данные, обновленные после первого вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="2585b-247">Note that the transaction is released between function calls and a series of calls to this function when the session is not in a transaction may return data updated after the first call to this function.</span></span>

<span data-ttu-id="2585b-248">Значение столбца по умолчанию будет извлечено, если для столбца не задано явно другое значение, если не задан параметр JET_bitRetrieveIgnoreDefault.</span><span class="sxs-lookup"><span data-stu-id="2585b-248">The default column value will be retrieved when the column has not been set explicitly to another value, unless the JET_bitRetrieveIgnoreDefault option is set.</span></span>

<span data-ttu-id="2585b-249">Получение значения столбца AutoIncrement из буфера копирования до вставки является распространенным средством идентификации записи, уникальной для компоновки при вставке нормализованных данных в несколько таблиц.</span><span class="sxs-lookup"><span data-stu-id="2585b-249">Retrieving the autoincrement column value from the copy buffer prior to insert is a common means of identifying a record uniquely for linkage when inserting normalized data into multiple tables.</span></span> <span data-ttu-id="2585b-250">Значение автоприращения выделяется при начале операции вставки и может быть извлечено из буфера копирования в любое время до завершения обновления.</span><span class="sxs-lookup"><span data-stu-id="2585b-250">The autoincrement value is allocated when the insert operation begins and can be retrieved from the copy buffer at any time until the update is complete.</span></span>

<span data-ttu-id="2585b-251">При извлечении всех столбцов с тегами, многозначными и разреженными столбцами путем установки параметра *columnid* в значение 0 (ноль) столбцы извлекаются в порядке *columnid* с наименьшего значения *columnid* до высшего значения *columnid*.</span><span class="sxs-lookup"><span data-stu-id="2585b-251">When retrieving all tagged, multi-valued, and sparse columns, by setting *columnid* to 0 (zero), columns are retrieved in *columnid* order from lowest *columnid* to highest *columnid*.</span></span> <span data-ttu-id="2585b-252">Каждый раз при получении значений столбцов возвращается тот же порядок значений столбцов.</span><span class="sxs-lookup"><span data-stu-id="2585b-252">The same order of column values is returned each time column values are retrieved.</span></span> <span data-ttu-id="2585b-253">Порядок является детерминированным.</span><span class="sxs-lookup"><span data-stu-id="2585b-253">The order is deterministic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2585b-254">Требования</span><span class="sxs-lookup"><span data-stu-id="2585b-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2585b-255"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="2585b-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2585b-256">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2585b-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2585b-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2585b-258">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2585b-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2585b-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2585b-260">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="2585b-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2585b-261"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="2585b-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2585b-262">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2585b-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2585b-263"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="2585b-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2585b-264">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2585b-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2585b-265">См. также:</span><span class="sxs-lookup"><span data-stu-id="2585b-265">See Also</span></span>

[<span data-ttu-id="2585b-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="2585b-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="2585b-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2585b-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2585b-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2585b-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2585b-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2585b-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2585b-270">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="2585b-270">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="2585b-271">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="2585b-271">JetSetColumn</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="2585b-272">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="2585b-272">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
