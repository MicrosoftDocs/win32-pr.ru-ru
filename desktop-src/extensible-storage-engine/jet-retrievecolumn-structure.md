---
description: 'Дополнительные сведения: структура JET_RETRIEVECOLUMN'
title: Структура JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701663"
---
# <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="6f5e3-103">Структура JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6f5e3-103">JET_RETRIEVECOLUMN Structure</span></span>


<span data-ttu-id="6f5e3-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6f5e3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="6f5e3-105">Структура JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6f5e3-105">JET_RETRIEVECOLUMN Structure</span></span>

<span data-ttu-id="6f5e3-106">Структура **JET_RETRIEVECOLUMN** содержит входные и выходные параметры для [жетретриевеколумнс](./jetretrievecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="6f5e3-106">The **JET_RETRIEVECOLUMN** structure contains input and output parameters for [JetRetrieveColumns](./jetretrievecolumns-function.md).</span></span> <span data-ttu-id="6f5e3-107">Поля в структуре описывают извлекаемое значение столбца, способ его извлечения и место сохранения результатов.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a><span data-ttu-id="6f5e3-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="6f5e3-108">Members</span></span>

<span data-ttu-id="6f5e3-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-109">**columnid**</span></span>

<span data-ttu-id="6f5e3-110">Идентификатор столбца для извлекаемого столбца.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-110">The column identifier for the column to retrieve.</span></span>

<span data-ttu-id="6f5e3-111">**пвдата**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-111">**pvData**</span></span>

<span data-ttu-id="6f5e3-112">Указатель для начала хранения данных, извлекаемых из значения столбца.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-112">A pointer to begin storing data that is retrieved from the column value.</span></span>

<span data-ttu-id="6f5e3-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-113">**cbData**</span></span>

<span data-ttu-id="6f5e3-114">Размер выделения, начиная с **пвдата**, в байтах.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-114">The size of allocation beginning at **pvData**, in bytes.</span></span> <span data-ttu-id="6f5e3-115">Операция получения столбца не будет хранить больше данных в **пвдата** , чем **cbData**.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-115">The retrieve column operation will not store more data at **pvData** than **cbData**.</span></span>

<span data-ttu-id="6f5e3-116">**кбактуал**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-116">**cbActual**</span></span>

<span data-ttu-id="6f5e3-117">Размер данных в байтах, получаемый операцией извлечения столбца.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-117">The size, in bytes, of data that is retrieved by a retrieve column operation.</span></span>

<span data-ttu-id="6f5e3-118">**грбит**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-118">**grbit**</span></span>

<span data-ttu-id="6f5e3-119">Группа битов, содержащая параметры для извлечения столбца, которые содержат ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-119">A group of bits that contain the options for column retrieval, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f5e3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6f5e3-120">Value</span></span></p></th>
<th><p><span data-ttu-id="6f5e3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6f5e3-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f5e3-122">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="6f5e3-122">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="6f5e3-123">Извлекает измененное значение вместо исходного значения.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-123">Retrieves the modified value instead of the original value.</span></span> <span data-ttu-id="6f5e3-124">Если значение не было изменено, то извлекается исходное значение.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-124">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="6f5e3-125">Таким образом, значение, которое еще не было вставлено или Обновлено, может быть извлечено при вставке или обновлении записи.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-125">In this way, a value that has not yet been inserted or updated can be retrieved when a record is inserted or updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5e3-126">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="6f5e3-126">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="6f5e3-127">Возвращает значения столбцов из индекса без доступа к записи, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-127">Retrieves column values from the index without accessing the record, if possible.</span></span> <span data-ttu-id="6f5e3-128">Таким образом, необязательная Загрузка записей может быть продолжена, если нужные данные будут доступны из самих записей индекса.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-128">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="6f5e3-129">В случаях, когда исходное значение столбца не может быть получено из индекса из-за необратимых преобразований или усечения данных, доступ к записи будет осуществляться, а данные будут извлечены как обычные.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-129">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="6f5e3-130">Это параметр производительности, и его следует указывать только в том случае, если вероятно, что значение столбца может быть извлечено из индекса.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-130">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="6f5e3-131">Этот параметр не следует указывать, если текущим индексом является кластеризованный индекс, поскольку записи индекса для кластеризованного или первичного индекса являются записями.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-131">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="6f5e3-132">Этот бит не может быть установлен, если также задано JET_bitRetrieveFromPrimaryBookmark.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-132">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5e3-133">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="6f5e3-133">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="6f5e3-134">Извлекает значения столбцов из закладки индекса и может отличаться от значения индекса, если столбец отображается как в первичном, так и в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-134">Retrieves column values from the index bookmark, and can differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="6f5e3-135">Этот параметр не следует указывать, если текущий индекс является кластеризованным или первичным индексом.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-135">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="6f5e3-136">Этот бит не может быть установлен, если также задано JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-136">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5e3-137">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="6f5e3-137">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="6f5e3-138">Извлекает порядковый номер значения столбца с несколькими значениями в претинфо- &gt; итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-138">Retrieves the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="6f5e3-139">В поле Итагсекуенце часто используются входные данные для получения значений столбцов с несколькими значениями из записи.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-139">The itagSequence field is often used an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="6f5e3-140">Однако при извлечении значений из индекса также можно связать запись индекса с определенным порядковым номером и получить также этот порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-140">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="6f5e3-141">Получение порядкового номера может быть дорогостоящей операцией, и ее следует выполнять только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-141">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5e3-142">JET_ Битретриевенулл</span><span class="sxs-lookup"><span data-stu-id="6f5e3-142">JET_ bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="6f5e3-143">Извлекает значения NULL для столбцов с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-143">Retrieves multi-valued column NULL values.</span></span> <span data-ttu-id="6f5e3-144">Если этот параметр не указан, значения NULL в столбцах с несколькими значениями будут пропускаться автоматически.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-144">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5e3-145">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="6f5e3-145">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="6f5e3-146">Приводит к возвращению значения NULL, если запрошенный порядковый номер равен 1, а значения для столбца в записи отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-146">Causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span> <span data-ttu-id="6f5e3-147">Этот параметр влияет только на столбцы с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-147">This option affects only multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5e3-148">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="6f5e3-148">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="6f5e3-149">Этот флаг предназначен только для внутреннего использования и не предназначен для использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-149">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5e3-150">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="6f5e3-150">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="6f5e3-151">Этот флаг предназначен только для внутреннего использования и не предназначен для использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-151">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6f5e3-152">**иблонгвалуе**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-152">**ibLongValue**</span></span>

<span data-ttu-id="6f5e3-153">Смещение для первого байта, получаемого из столбца типа [JET_coltypLongBinary](./jet-coltyp.md) или [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="6f5e3-153">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="6f5e3-154">**итагсекуенце**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-154">**itagSequence**</span></span>

<span data-ttu-id="6f5e3-155">Порядковый номер значений, содержащихся в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-155">The sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="6f5e3-156">**итагсекуенце** здесь в **JET_RETRIEVECOLUMN** может быть 0.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-156">**itagSequence** here in the **JET_RETRIEVECOLUMN** can be 0.</span></span> <span data-ttu-id="6f5e3-157">Если значение **итагсекуенце** равно 0, то вместо данных столбца возвращается число экземпляров многозначного столбца.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-157">If the **itagSequence** is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span> <span data-ttu-id="6f5e3-158">Значение **итагсекуенце** , равное 0, не может использоваться в вызовах [жетретриевеколумн](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="6f5e3-158">An **itagSequence** value of 0 cannot be used in calls to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="6f5e3-159">**колумниднексттагжед**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-159">**columnidNextTagged**</span></span>

<span data-ttu-id="6f5e3-160">Значение **columnid** столбца с тегом, многозначным или разреженным столбцом, когда все столбцы с тегами извлекаются путем передачи 0 в качестве значения **columnid** в [жетретриевеколумн](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="6f5e3-160">The **columnid** of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the **columnid** to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="6f5e3-161">**Err**</span><span class="sxs-lookup"><span data-stu-id="6f5e3-161">**err**</span></span>

<span data-ttu-id="6f5e3-162">Коды ошибок и предупреждения, возвращаемые при извлечении столбца.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-162">Error codes and warnings returned from the retrieval of the column.</span></span>

### <a name="requirements"></a><span data-ttu-id="6f5e3-163">Требования</span><span class="sxs-lookup"><span data-stu-id="6f5e3-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f5e3-164"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="6f5e3-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5e3-165">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5e3-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6f5e3-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5e3-167">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5e3-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6f5e3-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5e3-169">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6f5e3-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6f5e3-170">См. также:</span><span class="sxs-lookup"><span data-stu-id="6f5e3-170">See Also</span></span>

[<span data-ttu-id="6f5e3-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="6f5e3-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="6f5e3-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="6f5e3-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="6f5e3-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6f5e3-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6f5e3-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6f5e3-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6f5e3-175">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6f5e3-175">JET_RETRIEVECOLUMN</span></span>]()  
[<span data-ttu-id="6f5e3-176">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="6f5e3-176">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="6f5e3-177">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="6f5e3-177">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
