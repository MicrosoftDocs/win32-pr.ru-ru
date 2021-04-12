---
description: 'Дополнительные сведения: структура JET_INDEXLIST'
title: Структура JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346995"
---
# <a name="jet_indexlist-structure"></a><span data-ttu-id="fa609-103">Структура JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="fa609-103">JET_INDEXLIST Structure</span></span>


<span data-ttu-id="fa609-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fa609-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexlist-structure"></a><span data-ttu-id="fa609-105">Структура JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="fa609-105">JET_INDEXLIST Structure</span></span>

<span data-ttu-id="fa609-106">Структура **JET_INDEXLIST** содержит необходимые сведения для прохода по временной таблице, созданной функциями [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="fa609-106">The **JET_INDEXLIST** structure contains the necessary information to traverse a temporary table that is created by the [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) functions.</span></span> <span data-ttu-id="fa609-107">Каждая строка во временной таблице описывает столбец индекса.</span><span class="sxs-lookup"><span data-stu-id="fa609-107">Each row in the temporary table describes a column of an index.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a><span data-ttu-id="fa609-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="fa609-108">Members</span></span>

<span data-ttu-id="fa609-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="fa609-109">**cbStruct**</span></span>

<span data-ttu-id="fa609-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="fa609-110">The size of the structure in bytes.</span></span> <span data-ttu-id="fa609-111">Вызов API обновит это поле, поэтому вызывающий должен убедиться, что это значение соответствует sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="fa609-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="fa609-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="fa609-112">**tableid**</span></span>

<span data-ttu-id="fa609-113">Идентификатор созданной временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="fa609-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="fa609-114">За закрытие таблицы отвечает вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="fa609-114">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="fa609-115">**крекорд**</span><span class="sxs-lookup"><span data-stu-id="fa609-115">**cRecord**</span></span>

<span data-ttu-id="fa609-116">Количество записей во временной таблице, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="fa609-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="fa609-117">**колумнидиндекснаме**</span><span class="sxs-lookup"><span data-stu-id="fa609-117">**columnidindexname**</span></span>

<span data-ttu-id="fa609-118">Идентификатор столбца имени индекса.</span><span class="sxs-lookup"><span data-stu-id="fa609-118">The column identifier of the name of the index.</span></span>

<span data-ttu-id="fa609-119">Этот столбец является [JET_coltypTextом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-119">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-120">**колумнидгрбитиндекс**</span><span class="sxs-lookup"><span data-stu-id="fa609-120">**columnidgrbitIndex**</span></span>

<span data-ttu-id="fa609-121">Идентификатор столбца *грбитс* , используемого в индексе.</span><span class="sxs-lookup"><span data-stu-id="fa609-121">The column identifier of the *grbits* used on the index.</span></span> <span data-ttu-id="fa609-122">Список допустимых битов см. в разделе [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="fa609-122">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for a list of valid bits.</span></span>

<span data-ttu-id="fa609-123">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-123">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-124">**колумнидккэй**</span><span class="sxs-lookup"><span data-stu-id="fa609-124">**columnidcKey**</span></span>

<span data-ttu-id="fa609-125">Идентификатор столбца количества ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="fa609-125">The column identifier of the number of keys in the index.</span></span>

<span data-ttu-id="fa609-126">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-126">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-127">**колумнидцентри**</span><span class="sxs-lookup"><span data-stu-id="fa609-127">**columnidcEntry**</span></span>

<span data-ttu-id="fa609-128">Идентификатор столбца количества записей в индексе.</span><span class="sxs-lookup"><span data-stu-id="fa609-128">The column identifier of the number of entries in the index.</span></span>

<span data-ttu-id="fa609-129">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-129">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-130">**колумнидкпаже**</span><span class="sxs-lookup"><span data-stu-id="fa609-130">**columnidcPage**</span></span>

<span data-ttu-id="fa609-131">Идентификатор столбца количества страниц, используемых индексом. Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-131">The column identifier of the number of pages the index uses.This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-132">**колумнидкколумн**</span><span class="sxs-lookup"><span data-stu-id="fa609-132">**columnidcColumn**</span></span>

<span data-ttu-id="fa609-133">Идентификатор столбца общего числа столбцов, охватываемых индексом.</span><span class="sxs-lookup"><span data-stu-id="fa609-133">The column identifier of the total number of columns that the index spans.</span></span>

<span data-ttu-id="fa609-134">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-134">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-135">**колумнидиколумн**</span><span class="sxs-lookup"><span data-stu-id="fa609-135">**columnidiColumn**</span></span>

<span data-ttu-id="fa609-136">Идентификатор столбца для номера столбца в индексе.</span><span class="sxs-lookup"><span data-stu-id="fa609-136">The column identifier of the number of the columns in the index.</span></span> <span data-ttu-id="fa609-137">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="fa609-137">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="fa609-138">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-138">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa609-139">Значение</span><span class="sxs-lookup"><span data-stu-id="fa609-139">Value</span></span></p></th>
<th><p><span data-ttu-id="fa609-140">Значение</span><span class="sxs-lookup"><span data-stu-id="fa609-140">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa609-141">Циндексинфоколс</span><span class="sxs-lookup"><span data-stu-id="fa609-141">cIndexInfoCols</span></span><br />
<span data-ttu-id="fa609-142">15</span><span class="sxs-lookup"><span data-stu-id="fa609-142">15</span></span></p></td>
<td><p><span data-ttu-id="fa609-143">Указывает, что разрешены 15 столбцов.</span><span class="sxs-lookup"><span data-stu-id="fa609-143">Specifies that 15 columns are allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa609-144">кколумнинфоколс</span><span class="sxs-lookup"><span data-stu-id="fa609-144">cColumnInfoCols</span></span><br />
<span data-ttu-id="fa609-145">14</span><span class="sxs-lookup"><span data-stu-id="fa609-145">14</span></span></p></td>
<td><p><span data-ttu-id="fa609-146">Указывает, что разрешены 14 столбцов.</span><span class="sxs-lookup"><span data-stu-id="fa609-146">Specifies that 14 columns are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa609-147">кобжектинфоколс</span><span class="sxs-lookup"><span data-stu-id="fa609-147">cObjectInfoCols</span></span><br />
<span data-ttu-id="fa609-148">9</span><span class="sxs-lookup"><span data-stu-id="fa609-148">9</span></span></p></td>
<td><p><span data-ttu-id="fa609-149">Указывает, что разрешены 9 столбцов.</span><span class="sxs-lookup"><span data-stu-id="fa609-149">Specifies that 9 columns are allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fa609-150">**колумнидколумнид**</span><span class="sxs-lookup"><span data-stu-id="fa609-150">**columnidcolumnid**</span></span>

<span data-ttu-id="fa609-151">Идентификатор столбца индексируемого столбца. Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="fa609-151">The column identifier of the column that is indexed.For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="fa609-152">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-152">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-153">**колумнидколтип**</span><span class="sxs-lookup"><span data-stu-id="fa609-153">**columnidcoltyp**</span></span>

<span data-ttu-id="fa609-154">Идентификатор столбца колтип индексируемого столбца.</span><span class="sxs-lookup"><span data-stu-id="fa609-154">The column identifier of the coltyp of the column which is indexed.</span></span> <span data-ttu-id="fa609-155">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="fa609-155">For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="fa609-156">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-156">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-157">**колумнидкаунтри**</span><span class="sxs-lookup"><span data-stu-id="fa609-157">**columnidCountry**</span></span>

<span data-ttu-id="fa609-158">Идентификатор столбца с кодом страны индексируемого столбца.</span><span class="sxs-lookup"><span data-stu-id="fa609-158">The column identifier of the country code of the column that is indexed.</span></span> <span data-ttu-id="fa609-159">Код страны является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="fa609-159">The country code is deprecated.</span></span>

<span data-ttu-id="fa609-160">Этот столбец является [JET_coltypShortом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-160">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-161">**колумнидлангид**</span><span class="sxs-lookup"><span data-stu-id="fa609-161">**columnidLangid**</span></span>

<span data-ttu-id="fa609-162">Идентификатор столбца идентификатора языка (LCID), в котором был создан индекс.</span><span class="sxs-lookup"><span data-stu-id="fa609-162">The column identifier of the language identifier (LCID) under which the index was created.</span></span> <span data-ttu-id="fa609-163">Дополнительные сведения см. в разделе [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-163">For more information, see [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<span data-ttu-id="fa609-164">Этот столбец является [JET_coltypShortом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-164">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-165">**колумнидкп**</span><span class="sxs-lookup"><span data-stu-id="fa609-165">**columnidCp**</span></span>

<span data-ttu-id="fa609-166">Идентификатор столбца кодовой страницы, под которой был создан индекс.</span><span class="sxs-lookup"><span data-stu-id="fa609-166">The column identifier of the code page under which the index was created.</span></span> <span data-ttu-id="fa609-167">Дополнительные сведения см. в разделе [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-167">For more information, see [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span></span>

<span data-ttu-id="fa609-168">Этот столбец является [JET_coltypShortом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-168">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-169">**колумнидколлате**</span><span class="sxs-lookup"><span data-stu-id="fa609-169">**columnidCollate**</span></span>

<span data-ttu-id="fa609-170">Идентификатор столбца для последовательности параметров сортировки, в которой был создан индекс.</span><span class="sxs-lookup"><span data-stu-id="fa609-170">The column identifier of the collation sequence under which the index was created.</span></span> <span data-ttu-id="fa609-171">Последовательность параметров сортировки является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="fa609-171">The collation sequence is deprecated.</span></span>

<span data-ttu-id="fa609-172">Этот столбец является [JET_coltypShortом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-172">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-173">**колумнидгрбитколумн**</span><span class="sxs-lookup"><span data-stu-id="fa609-173">**columnidgrbitColumn**</span></span>

<span data-ttu-id="fa609-174">Идентификатор столбца *грбитс* , который применяется к порядку столбца в индексе.</span><span class="sxs-lookup"><span data-stu-id="fa609-174">The column identifier of the *grbits* that apply to the order of the column in the index.</span></span>

<span data-ttu-id="fa609-175">Данные для этого столбца можно упорядочить как JET_bitKeyAscending или JET_bitKeyDescending.</span><span class="sxs-lookup"><span data-stu-id="fa609-175">The data for this column can be ordered as JET_bitKeyAscending or JET_bitKeyDescending.</span></span> <span data-ttu-id="fa609-176">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-176">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="fa609-177">Например, индекс, определенный как "-Столбец1 \\ 0 + Столбец2 \\ 0", будет иметь JET_bitKeyDescending "Столбец1" и JET_bitKeyAscending "Столбец2".</span><span class="sxs-lookup"><span data-stu-id="fa609-177">For example, an index defined as "-column1\\0+column2\\0" will have JET_bitKeyDescending for "column1", and JET_bitKeyAscending for "column2".</span></span>

<span data-ttu-id="fa609-178">Для этого элемента допустимы следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="fa609-178">The following options are valid for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa609-179">Значение</span><span class="sxs-lookup"><span data-stu-id="fa609-179">Value</span></span></p></th>
<th><p><span data-ttu-id="fa609-180">Значение</span><span class="sxs-lookup"><span data-stu-id="fa609-180">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa609-181">JET_bitKeyAscending</span><span class="sxs-lookup"><span data-stu-id="fa609-181">JET_bitKeyAscending</span></span></p></td>
<td><p><span data-ttu-id="fa609-182">Сегмент индекса в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="fa609-182">An index segment in ascending order.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa609-183">JET_bitKeyDescending</span><span class="sxs-lookup"><span data-stu-id="fa609-183">JET_bitKeyDescending</span></span></p></td>
<td><p><span data-ttu-id="fa609-184">Сегмент индекса в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="fa609-184">An index segment in descending order.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fa609-185">**колумнидколумннаме**</span><span class="sxs-lookup"><span data-stu-id="fa609-185">**columnidcolumnname**</span></span>

<span data-ttu-id="fa609-186">Идентификатор столбца имени столбца.</span><span class="sxs-lookup"><span data-stu-id="fa609-186">The column identifier of the name of the column.</span></span>

<span data-ttu-id="fa609-187">Этот столбец является [JET_coltypTextом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-187">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa609-188">**колумнидлкмапфлагс**</span><span class="sxs-lookup"><span data-stu-id="fa609-188">**columnidLCMapFlags**</span></span>

<span data-ttu-id="fa609-189">Идентификатор столбца флагов, которые используются для создания индекса.</span><span class="sxs-lookup"><span data-stu-id="fa609-189">The column identifier of the flags that are used to create the index.</span></span> <span data-ttu-id="fa609-190">Дополнительные сведения см. в разделе **двмапфлагс** статьи [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-190">For more information, see the **dwMapFlags** section of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span></span>

<span data-ttu-id="fa609-191">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa609-191">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="fa609-192">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa609-192">Remarks</span></span>

<span data-ttu-id="fa609-193">Каждая строка во временной таблице соответствует столбцу в определенном индексе.</span><span class="sxs-lookup"><span data-stu-id="fa609-193">Each row in the temporary table corresponds to a column in a particular index.</span></span>

<span data-ttu-id="fa609-194">Например, индекс "+ A \\ 0 + B 0 + \\ C 0 + \\ D 0 + \\ E \\ 0" больше пяти столбцов, и он займет пять строк во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="fa609-194">For example, the index "+A\\0+B\\0+C\\0+D\\0+E\\0" is more than five columns, and it will occupy five rows in the temporary table.</span></span> <span data-ttu-id="fa609-195">Каждая из этих пяти строк будет иметь значение 5 в столбце, идентифицируемом по столбцу columnid.</span><span class="sxs-lookup"><span data-stu-id="fa609-195">Each of these five rows will have a value of 5 in the column that is identified by columnid column.</span></span> <span data-ttu-id="fa609-196">Однако каждая строка будет иметь разное значение для столбца columnid, в диапазоне от 0 до 4.</span><span class="sxs-lookup"><span data-stu-id="fa609-196">But each row will have a different value for columnid column, ranging from 0 to 4.</span></span>

<span data-ttu-id="fa609-197">Число ключей в определенном индексе соответствует числу уникальных значений, для которых вызывающий может выполнить поиск и получить точное соответствие.</span><span class="sxs-lookup"><span data-stu-id="fa609-197">The number of keys in a particular index corresponds to the number of unique values for which a caller can seek and get an exact match.</span></span> <span data-ttu-id="fa609-198">Число записей — это количество строк, совпадающих с индексом.</span><span class="sxs-lookup"><span data-stu-id="fa609-198">The number of entries is the number of rows that an index matches.</span></span> <span data-ttu-id="fa609-199">Если индекс имеет ограничение уникальности, число ключей равно числу записей.</span><span class="sxs-lookup"><span data-stu-id="fa609-199">If an index has a uniqueness constraint, then the number of keys is equal to the number of entries.</span></span> <span data-ttu-id="fa609-200">Например, если таблица содержит следующие сведения и индекс создается для столбца с именем "ключ", то существует три ключа (100, 200 и 500), но есть четыре записи ("this", "-", "a" и "example").</span><span class="sxs-lookup"><span data-stu-id="fa609-200">For example, if a table contains the following information and an index is created over the column named "key", then there are three keys (100, 200, and 500), but there are four entries ("this", "is", "an", and "example").</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa609-201">Ключ</span><span class="sxs-lookup"><span data-stu-id="fa609-201">Key</span></span></p></th>
<th><p><span data-ttu-id="fa609-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="fa609-202">Entry</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa609-203">100</span><span class="sxs-lookup"><span data-stu-id="fa609-203">100</span></span></p></td>
<td><p><span data-ttu-id="fa609-204">&quot;this&quot;</span><span class="sxs-lookup"><span data-stu-id="fa609-204">&quot;this&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa609-205">100</span><span class="sxs-lookup"><span data-stu-id="fa609-205">100</span></span></p></td>
<td><p><span data-ttu-id="fa609-206">&quot;is&quot;</span><span class="sxs-lookup"><span data-stu-id="fa609-206">&quot;is&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa609-207">200</span><span class="sxs-lookup"><span data-stu-id="fa609-207">200</span></span></p></td>
<td><p><span data-ttu-id="fa609-208">&quot;ранне&quot;</span><span class="sxs-lookup"><span data-stu-id="fa609-208">&quot;an&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa609-209">500</span><span class="sxs-lookup"><span data-stu-id="fa609-209">500</span></span></p></td>
<td><p><span data-ttu-id="fa609-210">&quot;example&quot;</span><span class="sxs-lookup"><span data-stu-id="fa609-210">&quot;example&quot;</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="fa609-211">Требования</span><span class="sxs-lookup"><span data-stu-id="fa609-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa609-212"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="fa609-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fa609-213">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fa609-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa609-214"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fa609-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fa609-215">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fa609-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa609-216"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fa609-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fa609-217">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fa609-217">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fa609-218">См. также:</span><span class="sxs-lookup"><span data-stu-id="fa609-218">See Also</span></span>

[<span data-ttu-id="fa609-219">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="fa609-219">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="fa609-220">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="fa609-220">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="fa609-221">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="fa609-221">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="fa609-222">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fa609-222">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fa609-223">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fa609-223">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fa609-224">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="fa609-224">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="fa609-225">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fa609-225">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fa609-226">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fa609-226">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fa609-227">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="fa609-227">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="fa609-228">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="fa609-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="fa609-229">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="fa609-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
