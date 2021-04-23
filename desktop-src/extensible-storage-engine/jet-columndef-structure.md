---
description: 'Дополнительные сведения: структура JET_COLUMNDEF'
title: Структура JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999629"
---
# <a name="jet_columndef-structure"></a><span data-ttu-id="043da-103">Структура JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="043da-103">JET_COLUMNDEF Structure</span></span>


<span data-ttu-id="043da-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="043da-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columndef-structure"></a><span data-ttu-id="043da-105">Структура JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="043da-105">JET_COLUMNDEF Structure</span></span>

<span data-ttu-id="043da-106">Структура **JET_COLUMNDEF** определяет данные, которые могут храниться в столбце.</span><span class="sxs-lookup"><span data-stu-id="043da-106">The **JET_COLUMNDEF** structure defines the data that can be stored in a column.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a><span data-ttu-id="043da-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="043da-107">Members</span></span>

<span data-ttu-id="043da-108">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="043da-108">**cbStruct**</span></span>

<span data-ttu-id="043da-109">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="043da-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="043da-110">Он должен иметь значение sizeof (JET_COLUMNDEF).</span><span class="sxs-lookup"><span data-stu-id="043da-110">It must be set to sizeof( JET_COLUMNDEF).</span></span>

<span data-ttu-id="043da-111">**columnid**</span><span class="sxs-lookup"><span data-stu-id="043da-111">**columnid**</span></span>

<span data-ttu-id="043da-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="043da-112">Reserved.</span></span> <span data-ttu-id="043da-113">значение **columnid** должно быть равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="043da-113">**columnid** must be set to 0 (zero).</span></span>

<span data-ttu-id="043da-114">**колтип**</span><span class="sxs-lookup"><span data-stu-id="043da-114">**coltyp**</span></span>

<span data-ttu-id="043da-115">Тип столбца (например, текст, двоичный или числовой).</span><span class="sxs-lookup"><span data-stu-id="043da-115">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="043da-116">Дополнительные сведения см. в разделе [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="043da-116">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="043da-117">**вкаунтри**</span><span class="sxs-lookup"><span data-stu-id="043da-117">**wCountry**</span></span>

<span data-ttu-id="043da-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="043da-118">Reserved.</span></span> <span data-ttu-id="043da-119">**вкаунтри** должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="043da-119">**wCountry** must be set to 0 (zero).</span></span>

<span data-ttu-id="043da-120">**langid**</span><span class="sxs-lookup"><span data-stu-id="043da-120">**langid**</span></span>

<span data-ttu-id="043da-121">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="043da-121">Obsolete.</span></span> <span data-ttu-id="043da-122">значение **LangID** должно быть равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="043da-122">**langid** should be set to 0 (zero).</span></span>

<span data-ttu-id="043da-123">**cp**</span><span class="sxs-lookup"><span data-stu-id="043da-123">**cp**</span></span>

<span data-ttu-id="043da-124">Кодовая страница для столбца.</span><span class="sxs-lookup"><span data-stu-id="043da-124">The code page for the column.</span></span> <span data-ttu-id="043da-125">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="043da-125">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="043da-126">Нулевое значение означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="043da-126">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="043da-127">Если столбец не является текстовым столбцом, кодовая страница автоматически получает значение 0.</span><span class="sxs-lookup"><span data-stu-id="043da-127">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="043da-128">**вколлате**</span><span class="sxs-lookup"><span data-stu-id="043da-128">**wCollate**</span></span>

<span data-ttu-id="043da-129">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="043da-129">Reserved.</span></span> <span data-ttu-id="043da-130">**вколлате** должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="043da-130">**wCollate** must be set to 0 (zero).</span></span>

<span data-ttu-id="043da-131">**кбмакс**</span><span class="sxs-lookup"><span data-stu-id="043da-131">**cbMax**</span></span>

<span data-ttu-id="043da-132">Максимальная длина (в байтах) столбца переменной длины или длина столбца фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="043da-132">The maximum length, in bytes, of a variable-length column, or the length of a fixed-length column.</span></span>

<span data-ttu-id="043da-133">**грбит**</span><span class="sxs-lookup"><span data-stu-id="043da-133">**grbit**</span></span>

<span data-ttu-id="043da-134">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="043da-134">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="043da-135">Значение</span><span class="sxs-lookup"><span data-stu-id="043da-135">Value</span></span></p></th>
<th><p><span data-ttu-id="043da-136">Значение</span><span class="sxs-lookup"><span data-stu-id="043da-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="043da-137">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="043da-137">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="043da-138">Столбец будет исправлен.</span><span class="sxs-lookup"><span data-stu-id="043da-138">The column will be fixed.</span></span> <span data-ttu-id="043da-139">Он всегда будет использовать один и тот же объем пространства в строке независимо от объема данных, сохраняемых в столбце.</span><span class="sxs-lookup"><span data-stu-id="043da-139">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="043da-140">JET_bitColumnFixed нельзя использовать с JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="043da-140">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="043da-141">Этот бит не может использоваться с длинными значениями ( <strong>JET_coltypLongText</strong> и <strong>JET_coltypLongBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="043da-141">This bit cannot be used with long values (that is <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="043da-142">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="043da-142">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="043da-143">Столбец будет помечен как.</span><span class="sxs-lookup"><span data-stu-id="043da-143">The column will be tagged.</span></span> <span data-ttu-id="043da-144">Помеченные столбцы не занимают место в базе данных, если они не содержат данных.</span><span class="sxs-lookup"><span data-stu-id="043da-144">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="043da-145">Этот бит не может использоваться с JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="043da-145">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="043da-146">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="043da-146">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="043da-147">Для этого столбца никогда не должно быть задано значение NULL.</span><span class="sxs-lookup"><span data-stu-id="043da-147">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="043da-148">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="043da-148">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="043da-149">Столбец представляет собой столбец версии, указывающий версию строки.</span><span class="sxs-lookup"><span data-stu-id="043da-149">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="043da-150">Значение этого столбца начинается с нуля и будет автоматически увеличиваться для каждого обновления в строке.</span><span class="sxs-lookup"><span data-stu-id="043da-150">The value of this column starts at zero and will be automatically incremented for each update on the row.</span></span></p>
<p><span data-ttu-id="043da-151">Этот бит можно применить только к <strong>JET_coltypLong</strong> столбцам.</span><span class="sxs-lookup"><span data-stu-id="043da-151">This bit can only be applied to <strong>JET_coltypLong</strong> columns.</span></span> <span data-ttu-id="043da-152">Этот бит не может использоваться с JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate или JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="043da-152">This bit cannot be used with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, or JET_bitColumnTagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="043da-153">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="043da-153">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="043da-154">Столбец будет автоматически увеличиваться.</span><span class="sxs-lookup"><span data-stu-id="043da-154">The column will automatically be incremented.</span></span> <span data-ttu-id="043da-155">Число является увеличивающимся числом и гарантированно уникально в пределах таблицы.</span><span class="sxs-lookup"><span data-stu-id="043da-155">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="043da-156">Однако числа могут не быть непрерывными.</span><span class="sxs-lookup"><span data-stu-id="043da-156">The numbers, however, might not be continuous.</span></span> <span data-ttu-id="043da-157">Например, если в таблицу вставляются пять строк, &quot; &quot; столбец AutoIncrement может содержать значения {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="043da-157">For example, if five rows are inserted into a table, the &quot;autoincrement&quot; column could contain the values { 1, 2, 6, 7, 8 }.</span></span> <span data-ttu-id="043da-158">Этот бит можно использовать только для столбцов типа <strong>JET_coltypLong</strong> или <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="043da-158">This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p>
<p><span data-ttu-id="043da-159"><strong>Windows 2000:  </strong> В Windows 2000 этот бит можно использовать только для столбцов типа <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="043da-159"><strong>Windows 2000:  </strong>In Windows 2000, this bit can only be used on columns of type <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="043da-160">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="043da-160">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="043da-161">Этот бит допустим только для вызовов <a href="gg269215(v=exchg.10).md">жетжетколумнинфо</a>.</span><span class="sxs-lookup"><span data-stu-id="043da-161">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="043da-162">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="043da-162">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="043da-163">Этот бит допустим только для вызовов <a href="gg294118(v=exchg.10).md">жетопентабле</a>.</span><span class="sxs-lookup"><span data-stu-id="043da-163">This bit is valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="043da-164">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="043da-164">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="043da-165">Этот бит допустим только для вызовов <a href="gg269211(v=exchg.10).md">жетопентемптабле</a>.</span><span class="sxs-lookup"><span data-stu-id="043da-165">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="043da-166">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="043da-166">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="043da-167">Столбец может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="043da-167">The column can be multi-valued.</span></span> <span data-ttu-id="043da-168">Столбец с несколькими значениями может иметь ноль, одно или несколько связанных с ним значений.</span><span class="sxs-lookup"><span data-stu-id="043da-168">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="043da-169">Различные значения в столбце с несколькими значениями идентифицируются по числу, называемому элементом <strong>итагсекуенце</strong> , который относится к различным структурам, включая: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>и <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="043da-169">The various values in a multi-valued column are identified by a number called the <strong>itagSequence</strong> member, which belongs to various structures, including: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, and <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="043da-170">Столбцы с несколькими значениями должны быть помечены как столбцы. Это значит, что они не могут быть столбцами фиксированной длины или переменной длины.</span><span class="sxs-lookup"><span data-stu-id="043da-170">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="043da-171">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="043da-171">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="043da-172">Указывает, что столбец является столбцом депонирования обновлений.</span><span class="sxs-lookup"><span data-stu-id="043da-172">Specifies that a column is an escrow update column.</span></span> <span data-ttu-id="043da-173">Столбец депонированного обновления может обновляться параллельно разными сеансами с <a href="gg294125(v=exchg.10).md">жетескровупдате</a> и поддерживать согласованность транзакций.</span><span class="sxs-lookup"><span data-stu-id="043da-173">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will maintain transactional consistency.</span></span> <span data-ttu-id="043da-174">Столбец депонированного обновления также должен соответствовать следующим условиям.</span><span class="sxs-lookup"><span data-stu-id="043da-174">An escrow update column must also meet the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="043da-175">Столбец депонированного обновления может быть создан только в том случае, если таблица пуста.</span><span class="sxs-lookup"><span data-stu-id="043da-175">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="043da-176">Столбец депонированного обновления должен иметь тип <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="043da-176">An escrow update column must be of type <strong>JET_coltypLong</strong>.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="043da-177">Столбец депонированного обновления должен иметь значение по умолчанию ( <strong>кбдефаулт</strong> должно быть положительным).</span><span class="sxs-lookup"><span data-stu-id="043da-177">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="043da-178">JET_bitColumnEscrowUpdate нельзя использовать в сочетании с JET_bitColumnTagged, JET_bitColumnVersion или JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="043da-178">JET_bitColumnEscrowUpdate cannot be used in conjunction with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="043da-179">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="043da-179">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="043da-180">Столбец будет создан в без сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="043da-180">The column will be created in an without version information.</span></span> <span data-ttu-id="043da-181">Это означает, что другие транзакции, пытающиеся добавить столбец с тем же именем, завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="043da-181">This means that other transactions that attempt to add a column with the same name will fail.</span></span> <span data-ttu-id="043da-182">Этот бит удобен только для <a href="gg294122(v=exchg.10).md">жетаддколумн</a>.</span><span class="sxs-lookup"><span data-stu-id="043da-182">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="043da-183">Его нельзя использовать в транзакции.</span><span class="sxs-lookup"><span data-stu-id="043da-183">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="043da-184">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="043da-184">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="043da-185">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="043da-185">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="043da-186">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="043da-186">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="043da-187">Вместо JET_bitColumnFinalize используйте JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="043da-187">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="043da-188">JET_bitColumnFinalize, что столбец может быть завершен.</span><span class="sxs-lookup"><span data-stu-id="043da-188">JET_bitColumnFinalize that a column can be finalized.</span></span> <span data-ttu-id="043da-189">Если столбец, который может быть завершен, имеет столбец депонированного обновления, который достигает нуля, строка будет удалена.</span><span class="sxs-lookup"><span data-stu-id="043da-189">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="043da-190">В будущих версиях вместо этого могут вызываться функции обратного вызова (Дополнительные сведения см. в разделе <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="043da-190">Future versions might invoke a callback function instead (For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="043da-191">Столбец, который может быть завершен, должен быть столбцом типа "условно Update".</span><span class="sxs-lookup"><span data-stu-id="043da-191">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="043da-192">JET_bitColumnFinalize нельзя использовать с JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="043da-192">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="043da-193">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="043da-193">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="043da-194">Значение по умолчанию для столбца будет предоставлено функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="043da-194">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="043da-195">См. <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="043da-195">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="043da-196">Столбец, содержащий определяемое пользователем значение по умолчанию, должен быть столбцом с тегами.</span><span class="sxs-lookup"><span data-stu-id="043da-196">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="043da-197">Указание JET_bitColumnUserDefinedDefault означает, что <strong>пвдефаулт</strong> должен указывать на структуру <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , а для <strong>кбдефаулт</strong> должно быть задано значение sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span><span class="sxs-lookup"><span data-stu-id="043da-197">Specifying JET_bitColumnUserDefinedDefault means that <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span></span></p>
<ul>
<li><p><span data-ttu-id="043da-198">JET_bitColumnUserDefinedDefault нельзя использовать в сочетании с JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero или JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="043da-198">JET_bitColumnUserDefinedDefault cannot be used in conjunction with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="043da-199">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="043da-199">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="043da-200">Столбец является столбцом депонированного обновления, и когда он достигает нуля, запись будет удалена.</span><span class="sxs-lookup"><span data-stu-id="043da-200">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="043da-201">Обычно для столбца, который может быть завершен, можно использовать его как поле счетчика ссылок, а когда поле достигает нуля, запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="043da-201">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="043da-202">JET_bitColumnDeleteOnZero связана с JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="043da-202">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="043da-203">Столбец Deleted-on-Zero должен быть столбцом депонированного обновления.</span><span class="sxs-lookup"><span data-stu-id="043da-203">A Delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="043da-204">JET_bitColumnDeleteOnZero нельзя использовать с JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="043da-204">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="043da-205">JET_bitColumnDeleteOnZero нельзя использовать с пользовательскими столбцами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="043da-205">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="043da-206">Требования</span><span class="sxs-lookup"><span data-stu-id="043da-206">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="043da-207"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="043da-207"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="043da-208">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="043da-208">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="043da-209"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="043da-209"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="043da-210">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="043da-210">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="043da-211"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="043da-211"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="043da-212">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="043da-212">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="043da-213">См. также:</span><span class="sxs-lookup"><span data-stu-id="043da-213">See Also</span></span>

[<span data-ttu-id="043da-214">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="043da-214">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="043da-215">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="043da-215">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="043da-216">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="043da-216">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="043da-217">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="043da-217">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="043da-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="043da-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="043da-219">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="043da-219">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="043da-220">жетаддколумн</span><span class="sxs-lookup"><span data-stu-id="043da-220">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="043da-221">жетескровупдате</span><span class="sxs-lookup"><span data-stu-id="043da-221">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="043da-222">жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="043da-222">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="043da-223">жетопентемптабле</span><span class="sxs-lookup"><span data-stu-id="043da-223">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="043da-224">JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="043da-224">JetOpenTempTable2</span></span>](./jetopentemptable2-function.md)  
[<span data-ttu-id="043da-225">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="043da-225">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)  
[<span data-ttu-id="043da-226">жетренамеколумн</span><span class="sxs-lookup"><span data-stu-id="043da-226">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
