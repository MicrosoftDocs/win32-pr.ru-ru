---
description: 'Дополнительные сведения: структура JET_COLUMNLIST'
title: Структура JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711312"
---
# <a name="jet_columnlist-structure"></a><span data-ttu-id="d38c5-103">Структура JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="d38c5-103">JET_COLUMNLIST Structure</span></span>


<span data-ttu-id="d38c5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d38c5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnlist-structure"></a><span data-ttu-id="d38c5-105">Структура JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="d38c5-105">JET_COLUMNLIST Structure</span></span>

<span data-ttu-id="d38c5-106">Структура **JET_COLUMNLIST** содержит сведения, необходимые для прохода по временной таблице, созданной функциями [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="d38c5-106">The **JET_COLUMNLIST** structure contains the information necessary to traverse the temporary table that is created by the [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions.</span></span> <span data-ttu-id="d38c5-107">Каждая строка во временной таблице описывает столбец в таблице, указанной в вызове API.</span><span class="sxs-lookup"><span data-stu-id="d38c5-107">Each row in the temporary table describes a column in the table given in the API call.</span></span> <span data-ttu-id="d38c5-108">Эта структура используется только с [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-108">This structure is used with only with [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a><span data-ttu-id="d38c5-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="d38c5-109">Members</span></span>

<span data-ttu-id="d38c5-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="d38c5-110">**cbStruct**</span></span>

<span data-ttu-id="d38c5-111">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="d38c5-111">The size of the structure in bytes.</span></span> <span data-ttu-id="d38c5-112">Вызов API обновит это поле, поэтому вызывающий должен убедиться, что это значение соответствует sizeof (JET_COLUMNLIST).</span><span class="sxs-lookup"><span data-stu-id="d38c5-112">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_COLUMNLIST ).</span></span>

<span data-ttu-id="d38c5-113">**TableID**</span><span class="sxs-lookup"><span data-stu-id="d38c5-113">**tableid**</span></span>

<span data-ttu-id="d38c5-114">Идентификатор созданной временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="d38c5-114">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="d38c5-115">За закрытие таблицы отвечает вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="d38c5-115">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="d38c5-116">**крекорд**</span><span class="sxs-lookup"><span data-stu-id="d38c5-116">**cRecord**</span></span>

<span data-ttu-id="d38c5-117">Количество записей во временной таблице, созданных вызовом API.</span><span class="sxs-lookup"><span data-stu-id="d38c5-117">The number of records in the temporary table that was created by the API call.</span></span>

<span data-ttu-id="d38c5-118">**колумнидпресентатионордер**</span><span class="sxs-lookup"><span data-stu-id="d38c5-118">**columnidPresentationOrder**</span></span>

<span data-ttu-id="d38c5-119">Идентификатор столбца для порядка представления.</span><span class="sxs-lookup"><span data-stu-id="d38c5-119">The column identifier of the presentation order.</span></span>

<span data-ttu-id="d38c5-120">Порядок представления используется для сортировки строк временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="d38c5-120">The presentation order is used to sort the rows of the temporary table.</span></span> <span data-ttu-id="d38c5-121">Порядок представления является фиксированным [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-121">The presentation order is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="d38c5-122">Если указанный уровень информации не является компактным, он также помечается как JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="d38c5-122">If the information level that was specified was not a compact level, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="d38c5-123">**колумнидколумннаме**</span><span class="sxs-lookup"><span data-stu-id="d38c5-123">**columnidcolumnname**</span></span>

<span data-ttu-id="d38c5-124">Идентификатор столбца имени столбца.</span><span class="sxs-lookup"><span data-stu-id="d38c5-124">The column identifier of the name of the column.</span></span>

<span data-ttu-id="d38c5-125">Если указанный уровень информации не является компактным, он также помечается как JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="d38c5-125">If the information level specified was not compact, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="d38c5-126">**колумнидколумнид**</span><span class="sxs-lookup"><span data-stu-id="d38c5-126">**columnidcolumnid**</span></span>

<span data-ttu-id="d38c5-127">Идентификатор столбца идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="d38c5-127">The column identifier of the column identifier.</span></span>

<span data-ttu-id="d38c5-128">Идентификатор столбца является фиксированным [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-128">The column identifier is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-129">**колумнидколтип**</span><span class="sxs-lookup"><span data-stu-id="d38c5-129">**columnidcoltyp**</span></span>

<span data-ttu-id="d38c5-130">Идентификатор столбца типа.</span><span class="sxs-lookup"><span data-stu-id="d38c5-130">The column identifier of the column type.</span></span>

<span data-ttu-id="d38c5-131">Тип столбца является фиксированным [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-131">The column type is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-132">**колумнидкаунтри**</span><span class="sxs-lookup"><span data-stu-id="d38c5-132">**columnidCountry**</span></span>

<span data-ttu-id="d38c5-133">Идентификатор столбца кода страны.</span><span class="sxs-lookup"><span data-stu-id="d38c5-133">The column identifier of the country code.</span></span>

<span data-ttu-id="d38c5-134">Код страны является фиксированной [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-134">The country code is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-135">**колумнидлангид**</span><span class="sxs-lookup"><span data-stu-id="d38c5-135">**columnidLangid**</span></span>

<span data-ttu-id="d38c5-136">Идентификатор столбца идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="d38c5-136">The column identifier of the language identifier.</span></span>

<span data-ttu-id="d38c5-137">Идентификатор языка является фиксированным [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-137">The language identifier is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-138">**колумнидкп**</span><span class="sxs-lookup"><span data-stu-id="d38c5-138">**columnidCp**</span></span>

<span data-ttu-id="d38c5-139">Идентификатор столбца кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="d38c5-139">The column identifier of the code page.</span></span>

<span data-ttu-id="d38c5-140">Кодовая страница является фиксированной [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-140">The code page is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-141">**колумнидколлате**</span><span class="sxs-lookup"><span data-stu-id="d38c5-141">**columnidCollate**</span></span>

<span data-ttu-id="d38c5-142">Идентификатор столбца для последовательности параметров сортировки.</span><span class="sxs-lookup"><span data-stu-id="d38c5-142">The column identifier of the collation sequence.</span></span>

<span data-ttu-id="d38c5-143">Последовательность параметров сортировки является фиксированной [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-143">The collation sequence is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-144">**колумнидкбмакс**</span><span class="sxs-lookup"><span data-stu-id="d38c5-144">**columnidcbMax**</span></span>

<span data-ttu-id="d38c5-145">Идентификатор столбца поля **кбмакс** .</span><span class="sxs-lookup"><span data-stu-id="d38c5-145">The column identifier of the **cbMax** field.</span></span>

<span data-ttu-id="d38c5-146">**Кбмакс** является фиксированной [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-146">The **cbMax** is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-147">**колумнидгрбит**</span><span class="sxs-lookup"><span data-stu-id="d38c5-147">**columnidgrbit**</span></span>

<span data-ttu-id="d38c5-148">Идентификатор столбца *грбитс* столбца.</span><span class="sxs-lookup"><span data-stu-id="d38c5-148">The column identifier of the *grbits* of the column.</span></span> <span data-ttu-id="d38c5-149">Поле *грбит* является фиксированной [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-149">The *grbit* field is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="d38c5-150">Дополнительные сведения об этих битах см. в разделе [JET_COLUMNDEF](./jet-columndef-structure.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-150">For more information about these bits, see [JET_COLUMNDEF](./jet-columndef-structure.md).</span></span>

<span data-ttu-id="d38c5-151">Ниже приведены возможные значения для **колумнидгрбит**.</span><span class="sxs-lookup"><span data-stu-id="d38c5-151">The following are possible values for **columnidgrbit**:</span></span>

<span data-ttu-id="d38c5-152">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="d38c5-152">JET_bitColumnTagged</span></span>

<span data-ttu-id="d38c5-153">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="d38c5-153">JET_bitColumnFixed</span></span>

<span data-ttu-id="d38c5-154">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="d38c5-154">JET_bitColumnUpdatable</span></span>

<span data-ttu-id="d38c5-155">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="d38c5-155">JET_bitColumnNotNULL</span></span>

<span data-ttu-id="d38c5-156">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="d38c5-156">JET_bitColumnAutoincrement</span></span>

<span data-ttu-id="d38c5-157">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="d38c5-157">JET_bitColumnVersion</span></span>

<span data-ttu-id="d38c5-158">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="d38c5-158">JET_bitColumnMultiValued</span></span>

<span data-ttu-id="d38c5-159">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d38c5-159">JET_bitColumnEscrowUpdate</span></span>

<span data-ttu-id="d38c5-160">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="d38c5-160">JET_bitColumnFinalize</span></span>

<span data-ttu-id="d38c5-161">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="d38c5-161">JET_bitColumnDeleteOnZero</span></span>

<span data-ttu-id="d38c5-162">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="d38c5-162">JET_bitColumnUserDefinedDefault</span></span>

<span data-ttu-id="d38c5-163">**колумниддефаулт**</span><span class="sxs-lookup"><span data-stu-id="d38c5-163">**columnidDefault**</span></span>

<span data-ttu-id="d38c5-164">Идентификатор столбца значения по умолчанию для столбца.</span><span class="sxs-lookup"><span data-stu-id="d38c5-164">The column identifier of the default value of the column.</span></span>

<span data-ttu-id="d38c5-165">Значение по умолчанию — [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-165">The default value is a [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-166">**колумнидбасетабленаме**</span><span class="sxs-lookup"><span data-stu-id="d38c5-166">**columnidBaseTableName**</span></span>

<span data-ttu-id="d38c5-167">Идентификатор столбца имени таблицы, из которой была получена таблица.</span><span class="sxs-lookup"><span data-stu-id="d38c5-167">The column identifier of the name of the table from which the table was derived.</span></span>

<span data-ttu-id="d38c5-168">Имя таблицы является [JET_coltypTextом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-168">The table name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-169">**колумнидбасеколумннаме**</span><span class="sxs-lookup"><span data-stu-id="d38c5-169">**columnidBaseColumnName**</span></span>

<span data-ttu-id="d38c5-170">Идентификатор столбца имени столбца, из которого был получен столбец.</span><span class="sxs-lookup"><span data-stu-id="d38c5-170">The column identifier of the name of the column from which the column was derived.</span></span>

<span data-ttu-id="d38c5-171">Имя столбца является [JET_coltypTextом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-171">The column name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="d38c5-172">**колумниддефинитионнаме**</span><span class="sxs-lookup"><span data-stu-id="d38c5-172">**columnidDefinitionName**</span></span>

<span data-ttu-id="d38c5-173">Идентификатор столбца имени определения столбца.</span><span class="sxs-lookup"><span data-stu-id="d38c5-173">The column identifier of the name of the column definition.</span></span>

<span data-ttu-id="d38c5-174">Имя определения столбца является [JET_coltypTextом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-174">The column definition name is a [JET_coltypText](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="d38c5-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d38c5-175">Remarks</span></span>

<span data-ttu-id="d38c5-176">По умолчанию порядок строк во временной таблице сортируется по имени столбца.</span><span class="sxs-lookup"><span data-stu-id="d38c5-176">By default, the order of the rows in the temporary table is sorted by the name of the column.</span></span> <span data-ttu-id="d38c5-177">Его также можно отсортировать по идентификатору столбца.</span><span class="sxs-lookup"><span data-stu-id="d38c5-177">It can also be sorted by column identifier.</span></span> <span data-ttu-id="d38c5-178">Дополнительные сведения о сортировке по идентификатору столбца см. в разделе [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="d38c5-178">For more information about how to sort by column identifier, see [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

<span data-ttu-id="d38c5-179">Вызов [жетжетколумнинфо](./jetgetcolumninfo-function.md) или [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) может указывать компактную форму результатов.</span><span class="sxs-lookup"><span data-stu-id="d38c5-179">The call to [JetGetColumnInfo](./jetgetcolumninfo-function.md) or [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) might specify a compact form of results.</span></span> <span data-ttu-id="d38c5-180">Если какие-либо столбцы были унаследованы из таблицы шаблонов, в результате сжатия не будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="d38c5-180">If any columns have been inherited from a template table, the compact results will not store them.</span></span>

### <a name="requirements"></a><span data-ttu-id="d38c5-181">Требования</span><span class="sxs-lookup"><span data-stu-id="d38c5-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d38c5-182"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d38c5-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d38c5-183">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d38c5-183">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d38c5-184"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d38c5-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d38c5-185">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d38c5-185">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d38c5-186"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d38c5-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d38c5-187">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d38c5-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d38c5-188">См. также:</span><span class="sxs-lookup"><span data-stu-id="d38c5-188">See Also</span></span>

[<span data-ttu-id="d38c5-189">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="d38c5-189">JET_COLTYP</span></span>](./jet-coltyp.md)

[<span data-ttu-id="d38c5-190">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="d38c5-190">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)

[<span data-ttu-id="d38c5-191">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d38c5-191">JET_COLUMNID</span></span>](./jet-columnid.md)

[<span data-ttu-id="d38c5-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d38c5-192">JET_ERR</span></span>](./jet-err.md)

[<span data-ttu-id="d38c5-193">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d38c5-193">JET_GRBIT</span></span>](./jet-grbit.md)

[<span data-ttu-id="d38c5-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d38c5-194">JET_SESID</span></span>](./jet-sesid.md)

[<span data-ttu-id="d38c5-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d38c5-195">JET_TABLEID</span></span>](./jet-tableid.md)

[<span data-ttu-id="d38c5-196">жетжетколумнинфо</span><span class="sxs-lookup"><span data-stu-id="d38c5-196">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)

[<span data-ttu-id="d38c5-197">жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="d38c5-197">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
