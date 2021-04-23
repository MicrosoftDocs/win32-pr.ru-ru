---
description: 'Дополнительные сведения: структура JET_COLUMNBASE'
title: Структура JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674411"
---
# <a name="jet_columnbase-structure"></a><span data-ttu-id="adf3b-103">Структура JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="adf3b-103">JET_COLUMNBASE Structure</span></span>


<span data-ttu-id="adf3b-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="adf3b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnbase-structure"></a><span data-ttu-id="adf3b-105">Структура JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="adf3b-105">JET_COLUMNBASE Structure</span></span>

<span data-ttu-id="adf3b-106">Структура **JET_COLUMNBASE** описывает параметры базового столбца.</span><span class="sxs-lookup"><span data-stu-id="adf3b-106">The **JET_COLUMNBASE** structure describes the parameters of a base column.</span></span> <span data-ttu-id="adf3b-107">Функции [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) используют структуру **JET_COLUMNBASE** .</span><span class="sxs-lookup"><span data-stu-id="adf3b-107">The [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions use the **JET_COLUMNBASE** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a><span data-ttu-id="adf3b-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="adf3b-108">Members</span></span>

<span data-ttu-id="adf3b-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="adf3b-109">**cbStruct**</span></span>

<span data-ttu-id="adf3b-110">Размер этой структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="adf3b-110">The size of this structure, in bytes.</span></span> <span data-ttu-id="adf3b-111">Задайте для **кбструкт** значение sizeof (JET_COLUMNBASE).</span><span class="sxs-lookup"><span data-stu-id="adf3b-111">Set **cbStruct** to sizeof( JET_COLUMNBASE ).</span></span>

<span data-ttu-id="adf3b-112">**columnid**</span><span class="sxs-lookup"><span data-stu-id="adf3b-112">**columnid**</span></span>

<span data-ttu-id="adf3b-113">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="adf3b-113">Reserved.</span></span> <span data-ttu-id="adf3b-114">Установите значение **columnid** равным 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="adf3b-114">Set **columnid** to 0 (zero).</span></span>

<span data-ttu-id="adf3b-115">**колтип**</span><span class="sxs-lookup"><span data-stu-id="adf3b-115">**coltyp**</span></span>

<span data-ttu-id="adf3b-116">Тип столбца (например, текст, двоичный или числовой).</span><span class="sxs-lookup"><span data-stu-id="adf3b-116">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="adf3b-117">Дополнительные сведения см. в разделе [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="adf3b-117">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="adf3b-118">**вкаунтри**</span><span class="sxs-lookup"><span data-stu-id="adf3b-118">**wCountry**</span></span>

<span data-ttu-id="adf3b-119">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="adf3b-119">Reserved.</span></span> <span data-ttu-id="adf3b-120">Задайте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="adf3b-120">Set to 0 (zero).</span></span>

<span data-ttu-id="adf3b-121">**langid**</span><span class="sxs-lookup"><span data-stu-id="adf3b-121">**langid**</span></span>

<span data-ttu-id="adf3b-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="adf3b-122">Reserved.</span></span> <span data-ttu-id="adf3b-123">Задайте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="adf3b-123">Set to 0 (zero).</span></span>

<span data-ttu-id="adf3b-124">**cp**</span><span class="sxs-lookup"><span data-stu-id="adf3b-124">**cp**</span></span>

<span data-ttu-id="adf3b-125">Кодовая страница для столбца.</span><span class="sxs-lookup"><span data-stu-id="adf3b-125">The code page for the column.</span></span> <span data-ttu-id="adf3b-126">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="adf3b-126">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="adf3b-127">Нулевое значение означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="adf3b-127">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="adf3b-128">Если столбец не является текстовым столбцом, кодовая страница автоматически устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="adf3b-128">If the column is not a text column, the code page is automatically set to zero.</span></span>

<span data-ttu-id="adf3b-129">**вфиллер**</span><span class="sxs-lookup"><span data-stu-id="adf3b-129">**wFiller**</span></span>

<span data-ttu-id="adf3b-130">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="adf3b-130">Reserved.</span></span> <span data-ttu-id="adf3b-131">Задайте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="adf3b-131">Set to 0 (zero).</span></span>

<span data-ttu-id="adf3b-132">**кбмакс**</span><span class="sxs-lookup"><span data-stu-id="adf3b-132">**cbMax**</span></span>

<span data-ttu-id="adf3b-133">Максимальная длина (в байтах) столбца переменной длины или фактической длины в байтах для столбца фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="adf3b-133">The maximum length, in bytes, of a variable-length column, or the actual length, in bytes, of a fixed-length column.</span></span>

<span data-ttu-id="adf3b-134">**грбит**</span><span class="sxs-lookup"><span data-stu-id="adf3b-134">**grbit**</span></span>

<span data-ttu-id="adf3b-135">Параметры для столбца, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="adf3b-135">Options for the column, including zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adf3b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="adf3b-136">Value</span></span></p></th>
<th><p><span data-ttu-id="adf3b-137">Значение</span><span class="sxs-lookup"><span data-stu-id="adf3b-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-138">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="adf3b-138">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="adf3b-139">Столбец является фиксированным и занимает один и тот же объем пространства в строке независимо от объема содержащихся в ней данных.</span><span class="sxs-lookup"><span data-stu-id="adf3b-139">The column is fixed and occupies the same amount of space in a row regardless of how much data it contains.</span></span> <span data-ttu-id="adf3b-140">JET_bitColumnFixed нельзя сочетать с JET_bitColumnTagged и не может использоваться, если для элемента <strong>колтип</strong> задано значение <strong>JET_coltypLongText</strong> или <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="adf3b-140">JET_bitColumnFixed cannot be combined with JET_bitColumnTagged, and cannot be used when the <strong>coltyp</strong> member is set to <strong>JET_coltypLongText</strong> or <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-141">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="adf3b-141">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="adf3b-142">Столбец помечается и занимает место в базе данных только в том случае, если содержит данные.</span><span class="sxs-lookup"><span data-stu-id="adf3b-142">The column is tagged and occupies space in the database only if it contains data.</span></span> <span data-ttu-id="adf3b-143">JET_bitColumnTagged нельзя сочетать с JET_bitColumnFixed, JET_bitColumnVersion или JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="adf3b-143">JET_bitColumnTagged cannot be combined with JET_bitColumnFixed, JET_bitColumnVersion, or JET_bitColumnEscrowUpdate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-144">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="adf3b-144">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="adf3b-145">Для этого столбца не должно быть задано значение <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="adf3b-145">The column must not be set to a <strong>NULL</strong> value.</span></span></p>
<p><span data-ttu-id="adf3b-146">JET_bitColumnNotNULL нельзя сочетать с JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="adf3b-146">JET_bitColumnNotNULL cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-147">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="adf3b-147">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="adf3b-148">Столбец представляет собой столбец версии, указывающий версию строки.</span><span class="sxs-lookup"><span data-stu-id="adf3b-148">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="adf3b-149">Значение этого столбца начинается с нуля и автоматически увеличивается на единицу при каждом обновлении строки.</span><span class="sxs-lookup"><span data-stu-id="adf3b-149">The value of this column starts at zero and is automatically incremented for each update of the row.</span></span></p>
<p><span data-ttu-id="adf3b-150">JET_bitColumnVersion можно использовать только в том случае, если элемент <strong>колтип</strong> имеет значение <strong>JET_coltypLong</strong> и не может сочетаться с JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged или JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="adf3b-150">JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> and cannot be combined with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged, or JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-151">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="adf3b-151">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="adf3b-152">Столбец автоматически увеличивается.</span><span class="sxs-lookup"><span data-stu-id="adf3b-152">The column is automatically incremented.</span></span> <span data-ttu-id="adf3b-153">Число является увеличивающимся числом и гарантированно уникально в пределах таблицы.</span><span class="sxs-lookup"><span data-stu-id="adf3b-153">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="adf3b-154">Однако числа могут не быть последовательными.</span><span class="sxs-lookup"><span data-stu-id="adf3b-154">The numbers, however, may not be sequential.</span></span> <span data-ttu-id="adf3b-155">Например, если в таблицу вставляются пять строк, то автоматически увеличивающийся столбец может содержать значения {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="adf3b-155">For example, if five rows are inserted into a table, the automatically incremented column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="adf3b-156">JET_bitColumnAutoincrement можно использовать только в том случае, если элемент <strong>колтип</strong> имеет значение <strong>JET_coltypLong</strong> или <strong>JET_coltypCurrency</strong> и не может сочетаться с JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault или JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="adf3b-156">JET_bitColumnAutoincrement can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong> and cannot be combined with JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault, or JET_bitColumnVersion.</span></span></p>
<p><span data-ttu-id="adf3b-157"><strong>Windows 2000:  </strong> JET_bitColumnVersion можно использовать, только если для элемента <strong>колтип</strong> задано значение <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="adf3b-157"><strong>Windows 2000:  </strong>JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-158">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="adf3b-158">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="adf3b-159">Допустимо только для вызовов <a href="gg269215(v=exchg.10).md">жетжетколумнинфо</a>.</span><span class="sxs-lookup"><span data-stu-id="adf3b-159">Valid only for calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span> <span data-ttu-id="adf3b-160">JET_bitColumnUpdatable нельзя сочетать с JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="adf3b-160">JET_bitColumnUpdatable cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-161">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="adf3b-161">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="adf3b-162">Допускается только для вызовов <a href="gg294118(v=exchg.10).md">жетопентабле</a>.</span><span class="sxs-lookup"><span data-stu-id="adf3b-162">Valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-163">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="adf3b-163">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="adf3b-164">Допускается только для вызовов <a href="gg269211(v=exchg.10).md">жетопентемптабле</a>.</span><span class="sxs-lookup"><span data-stu-id="adf3b-164">Valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-165">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="adf3b-165">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="adf3b-166">Столбец может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="adf3b-166">The column can be multi-valued.</span></span> <span data-ttu-id="adf3b-167">Столбец с несколькими значениями может иметь ноль, одно или несколько связанных с ним значений.</span><span class="sxs-lookup"><span data-stu-id="adf3b-167">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="adf3b-168">Различные значения в столбце с несколькими значениями идентифицируются по числу в элементе <strong>итагсекуенце</strong> различных структур, например <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="adf3b-168">The various values in a multi-valued column are identified by a number in the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="adf3b-169">Столбцы с несколькими значениями должны быть помечены как столбцы. Это значит, что они не могут быть столбцами фиксированной или переменной длины.</span><span class="sxs-lookup"><span data-stu-id="adf3b-169">Multi-valued columns must be tagged columns; that is, they may not be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-170">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="adf3b-170">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="adf3b-171">Указывает, что столбец является столбцом депонированного обновления, который может обновляться параллельно различными сеансами с <a href="gg294125(v=exchg.10).md">жетескровупдате</a> и будет иметь согласованность транзакций.</span><span class="sxs-lookup"><span data-stu-id="adf3b-171">Specifies that a column is an escrow update column that can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will have transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="adf3b-172">Столбец депонированного обновления может быть создан только в том случае, если таблица пуста.</span><span class="sxs-lookup"><span data-stu-id="adf3b-172">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="adf3b-173">Для столбца депонированного обновления элемент <strong>колтип</strong> должен иметь значение <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="adf3b-173">For an escrow update column, the <strong>coltyp</strong> member must be set to <strong>JET_coltypLong.</strong></span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="adf3b-174">Столбец депонированного обновления должен иметь значение по умолчанию ( <strong>кбдефаулт</strong> должно быть положительным).</span><span class="sxs-lookup"><span data-stu-id="adf3b-174">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="adf3b-175">JET_bitColumnEscrowUpdate нельзя сочетать с JET_bitColumnTagged, JET_bitColumnVersion или JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="adf3b-175">JET_bitColumnEscrowUpdate cannot be combined with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-176">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="adf3b-176">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="adf3b-177">Столбец создается без номера версии.</span><span class="sxs-lookup"><span data-stu-id="adf3b-177">The column is created without a version number.</span></span> <span data-ttu-id="adf3b-178">Это означает, что другие транзакции, пытающиеся добавить столбец с тем же именем, завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="adf3b-178">This means that other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="adf3b-179">JET_bitColumnUnversioned используется только с <a href="gg294122(v=exchg.10).md">жетаддколумн</a>.</span><span class="sxs-lookup"><span data-stu-id="adf3b-179">JET_bitColumnUnversioned is used only with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="adf3b-180">Его нельзя использовать в транзакции.</span><span class="sxs-lookup"><span data-stu-id="adf3b-180">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-181">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="adf3b-181">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="adf3b-182">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="adf3b-182">Reserved for future use.</span></span></p>
<p><span data-ttu-id="adf3b-183">JET_bitColumnMaybeNull нельзя сочетать с JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="adf3b-183">JET_bitColumnMaybeNull cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-184">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="adf3b-184">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="adf3b-185">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="adf3b-185">Do not use.</span></span> <span data-ttu-id="adf3b-186">Вместо этого используйте JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="adf3b-186">Use JET_bitColumnDeleteOnZero instead.</span></span></p>
<p><span data-ttu-id="adf3b-187">Столбец может быть завершен.</span><span class="sxs-lookup"><span data-stu-id="adf3b-187">The column can be finalized.</span></span> <span data-ttu-id="adf3b-188">Столбец, который может быть завершен, — это столбец депонированного обновления, который приводит к удалению строки, когда столбец достигает нуля.</span><span class="sxs-lookup"><span data-stu-id="adf3b-188">A column that can be finalized is an escrow update column that causes the row to be deleted when the column reaches zero.</span></span> <span data-ttu-id="adf3b-189">В будущих версиях вместо этого могут вызываться функции обратного вызова (см. <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="adf3b-189">Future versions may invoke a callback function instead (See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="adf3b-190">Столбец, который может быть завершен, должен быть столбцом типа "условно Update".</span><span class="sxs-lookup"><span data-stu-id="adf3b-190">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="adf3b-191">JET_bitColumnFinalize нельзя сочетать с JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="adf3b-191">JET_bitColumnFinalize cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-192">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="adf3b-192">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="adf3b-193">Значение по умолчанию для столбца будет предоставлено функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="adf3b-193">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="adf3b-194">См. <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="adf3b-194">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="adf3b-195">Столбец, содержащий определяемое пользователем значение по умолчанию, должен быть столбцом с тегами.</span><span class="sxs-lookup"><span data-stu-id="adf3b-195">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="adf3b-196">Если указано JET_bitColumnUserDefinedDefault, <strong>пвдефаулт</strong> должен указывать на структуру <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , а для <strong>кбдефаулт</strong> должно быть задано значение sizeof (JET_USERDEFINEDDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="adf3b-196">If JET_bitColumnUserDefinedDefault is specified, the <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( JET_USERDEFINEDDEFAULT ).</span></span></p>
<p><span data-ttu-id="adf3b-197">JET_bitColumnUserDefinedDefault не могут сочетаться с JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero или JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="adf3b-197">JET_bitColumnUserDefinedDefault cannot be combined with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-198">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="adf3b-198">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="adf3b-199">Столбец является столбцом депонированного обновления, и когда он достигает нуля, запись будет удалена.</span><span class="sxs-lookup"><span data-stu-id="adf3b-199">The column is an escrow update column and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="adf3b-200">Как правило, при удалении столбцов с удалением на нуль используются поля счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="adf3b-200">A common use for delete-on-zero columns is as reference count fields.</span></span> <span data-ttu-id="adf3b-201">Когда число ссылок становится равным нулю, запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="adf3b-201">When the number of references fall to zero, the record is deleted.</span></span> <span data-ttu-id="adf3b-202">Столбец Deleted-on-Zero должен быть столбцом депонированного обновления.</span><span class="sxs-lookup"><span data-stu-id="adf3b-202">A delete-on-zero column must be an escrow update column.</span></span></p>
<p><span data-ttu-id="adf3b-203">JET_bitColumnDeleteOnZero заменяет JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="adf3b-203">JET_bitColumnDeleteOnZero replaces JET_bitColumnFinalize.</span></span></p>
<p><span data-ttu-id="adf3b-204">JET_bitColumnDeleteOnZero нельзя сочетать с JET_bitColumnFinalize или JET_bitColumnUserDefinedDefault и не может использоваться с пользовательскими столбцами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="adf3b-204">JET_bitColumnDeleteOnZero cannot be combined with JET_bitColumnFinalize or JET_bitColumnUserDefinedDefault, and cannot be used with user-defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adf3b-205">**сзбасетабленаме**</span><span class="sxs-lookup"><span data-stu-id="adf3b-205">**szBaseTableName**</span></span>

<span data-ttu-id="adf3b-206">Таблица, из которой текущая таблица наследует свою DDL.</span><span class="sxs-lookup"><span data-stu-id="adf3b-206">The table from which the current table inherits its DDL.</span></span>

<span data-ttu-id="adf3b-207">**сзбасеколумннаме**</span><span class="sxs-lookup"><span data-stu-id="adf3b-207">**szBaseColumnName**</span></span>

<span data-ttu-id="adf3b-208">Имя столбца в таблице шаблонов.</span><span class="sxs-lookup"><span data-stu-id="adf3b-208">The name of the column in the template table.</span></span>

### <a name="remarks"></a><span data-ttu-id="adf3b-209">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adf3b-209">Remarks</span></span>

<span data-ttu-id="adf3b-210">**JET_COLUMNBASE** содержит большую часть тех же сведений, что и [JET_COLUMNDEF](./jet-columndef-structure.md), но добавляет строковые поля для описания базовой таблицы (если использовалась иерархическая DDL).</span><span class="sxs-lookup"><span data-stu-id="adf3b-210">**JET_COLUMNBASE** contains much of the same information as [JET_COLUMNDEF](./jet-columndef-structure.md), but it adds string fields to describe the base table (if a hierarchical DDL was used).</span></span>

### <a name="requirements"></a><span data-ttu-id="adf3b-211">Требования</span><span class="sxs-lookup"><span data-stu-id="adf3b-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-212"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="adf3b-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="adf3b-213">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="adf3b-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-214"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="adf3b-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="adf3b-215">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="adf3b-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf3b-216"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="adf3b-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="adf3b-217">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="adf3b-217">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf3b-218"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="adf3b-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="adf3b-219">Реализуется как <strong>JET_COLUMNBASE_W</strong> (Юникод) и <strong>JET_COLUMNBASE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="adf3b-219">Implemented as <strong>JET_COLUMNBASE_W</strong> (Unicode) and <strong>JET_COLUMNBASE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="adf3b-220">См. также:</span><span class="sxs-lookup"><span data-stu-id="adf3b-220">See Also</span></span>

[<span data-ttu-id="adf3b-221">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="adf3b-221">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="adf3b-222">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="adf3b-222">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="adf3b-223">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="adf3b-223">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="adf3b-224">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="adf3b-224">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="adf3b-225">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="adf3b-225">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="adf3b-226">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="adf3b-226">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="adf3b-227">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="adf3b-227">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="adf3b-228">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="adf3b-228">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="adf3b-229">жетжетколумнинфо</span><span class="sxs-lookup"><span data-stu-id="adf3b-229">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="adf3b-230">жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="adf3b-230">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="adf3b-231">жетренамеколумн</span><span class="sxs-lookup"><span data-stu-id="adf3b-231">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
