---
description: 'Дополнительные сведения: структура JET_COLUMNCREATE'
title: Структура JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693310"
---
# <a name="jet_columncreate-structure"></a><span data-ttu-id="6c439-103">Структура JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="6c439-103">JET_COLUMNCREATE Structure</span></span>


<span data-ttu-id="6c439-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6c439-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columncreate-structure"></a><span data-ttu-id="6c439-105">Структура JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="6c439-105">JET_COLUMNCREATE Structure</span></span>

<span data-ttu-id="6c439-106">Структура **JET_COLUMNCREATE** описывает столбец, который создается в базе данных.</span><span class="sxs-lookup"><span data-stu-id="6c439-106">The **JET_COLUMNCREATE** structure describes a column to create in a database.</span></span>

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a><span data-ttu-id="6c439-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="6c439-107">Members</span></span>

<span data-ttu-id="6c439-108">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="6c439-108">**cbStruct**</span></span>

<span data-ttu-id="6c439-109">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="6c439-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="6c439-110">Это поле должно быть инициализировано в **sizeof (JET_COLUMNCREATE)**.</span><span class="sxs-lookup"><span data-stu-id="6c439-110">This field must be initialized to **sizeof( JET_COLUMNCREATE )**.</span></span>

<span data-ttu-id="6c439-111">**сзколумннаме**</span><span class="sxs-lookup"><span data-stu-id="6c439-111">**szColumnName**</span></span>

<span data-ttu-id="6c439-112">Имя создаваемого столбца.</span><span class="sxs-lookup"><span data-stu-id="6c439-112">The name of the column to create.</span></span> <span data-ttu-id="6c439-113">Имя должно соответствовать следующим критериям:</span><span class="sxs-lookup"><span data-stu-id="6c439-113">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="6c439-114">Длина должна быть меньше JET_cbNameMost символов, не включая завершающее значение NULL.</span><span class="sxs-lookup"><span data-stu-id="6c439-114">It must be fewer than JET_cbNameMost characters in length, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c439-115">Он должен содержать только символы из следующих наборов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей квадратной скобки ( \] ), т. е. символов ASCII 0x20, 0x22 до 0x7F.</span><span class="sxs-lookup"><span data-stu-id="6c439-115">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c439-116">Оно не может начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="6c439-116">It cannot begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c439-117">Он должен содержать по крайней мере один символ, не являющийся пробелом.</span><span class="sxs-lookup"><span data-stu-id="6c439-117">It must contain at least one non-space character.</span></span>

<span data-ttu-id="6c439-118">**колтип**</span><span class="sxs-lookup"><span data-stu-id="6c439-118">**coltyp**</span></span>

<span data-ttu-id="6c439-119">Тип столбца (например, текст, двоичный или числовой).</span><span class="sxs-lookup"><span data-stu-id="6c439-119">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="6c439-120">Дополнительные сведения см. в разделе [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="6c439-120">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="6c439-121">**кбмакс**</span><span class="sxs-lookup"><span data-stu-id="6c439-121">**cbMax**</span></span>

<span data-ttu-id="6c439-122">Максимальная длина (в байтах) столбца переменной длины.</span><span class="sxs-lookup"><span data-stu-id="6c439-122">The maximum length, in bytes, of a variable-length column.</span></span> <span data-ttu-id="6c439-123">Длина столбца для столбцов фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="6c439-123">The length of the column for fixed-length columns.</span></span>

<span data-ttu-id="6c439-124">**грбит**</span><span class="sxs-lookup"><span data-stu-id="6c439-124">**grbit**</span></span>

<span data-ttu-id="6c439-125">Группа битов, содержащая параметры для этой структуры, которые содержат ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6c439-125">A group of bits that contain the options for this structure, and which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c439-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6c439-126">Value</span></span></p></th>
<th><p><span data-ttu-id="6c439-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6c439-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c439-128">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="6c439-128">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="6c439-129">Столбец является фиксированным.</span><span class="sxs-lookup"><span data-stu-id="6c439-129">The column is fixed.</span></span> <span data-ttu-id="6c439-130">Он всегда будет использовать один и тот же объем пространства в строке независимо от объема данных, сохраняемых в столбце.</span><span class="sxs-lookup"><span data-stu-id="6c439-130">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="6c439-131">JET_bitColumnFixed нельзя использовать с JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="6c439-131">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="6c439-132">Этот бит не может использоваться с длинными значениями, такими как <strong>JET_coltypLongText</strong> и <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c439-132">This bit cannot be used with long values such as <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-133">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="6c439-133">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="6c439-134">Столбец помечен как тег.</span><span class="sxs-lookup"><span data-stu-id="6c439-134">The column is tagged.</span></span> <span data-ttu-id="6c439-135">Помеченные столбцы не занимают место в базе данных, если они не содержат данных.</span><span class="sxs-lookup"><span data-stu-id="6c439-135">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="6c439-136">Этот бит не может использоваться с JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="6c439-136">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c439-137">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="6c439-137">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="6c439-138">Для этого столбца никогда не должно быть задано значение NULL.</span><span class="sxs-lookup"><span data-stu-id="6c439-138">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-139">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="6c439-139">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="6c439-140">Столбец автоматически увеличивается.</span><span class="sxs-lookup"><span data-stu-id="6c439-140">The column is automatically incremented.</span></span> <span data-ttu-id="6c439-141">Число является увеличивающимся числом и гарантированно уникально в пределах таблицы.</span><span class="sxs-lookup"><span data-stu-id="6c439-141">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="6c439-142">Однако это число может не быть непрерывным.</span><span class="sxs-lookup"><span data-stu-id="6c439-142">The number, however, might not be continuous.</span></span> <span data-ttu-id="6c439-143">Например, если в таблицу вставляются пять строк, столбец AutoIncrement может содержать значения {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="6c439-143">For example, if five rows are inserted into a table, the autoincrement column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="6c439-144"><strong>Windows 2000:  </strong> Этот бит можно использовать только для столбцов типа <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c439-144"><strong>Windows 2000:  </strong>This bit can be used only on columns of type <strong>JET_coltypLong</strong>.</span></span></p>
<p><span data-ttu-id="6c439-145"><strong>Windows Server 2003 и более поздние версии:  </strong> Этот бит можно использовать только для столбцов типа <strong>JET_coltypLong</strong> или <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c439-145"><strong>Windows Server 2003 and later:  </strong>This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c439-146">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="6c439-146">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="6c439-147">Этот бит допустим только для вызовов <a href="gg269215(v=exchg.10).md">жетжетколумнинфо</a>.</span><span class="sxs-lookup"><span data-stu-id="6c439-147">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-148">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="6c439-148">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="6c439-149">Этот бит допустим только для вызовов <a href="gg269211(v=exchg.10).md">жетопентемптабле</a>.</span><span class="sxs-lookup"><span data-stu-id="6c439-149">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c439-150">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="6c439-150">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="6c439-151">Этот бит допустим только для вызовов <a href="gg269211(v=exchg.10).md">жетопентемптабле</a>.</span><span class="sxs-lookup"><span data-stu-id="6c439-151">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-152">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="6c439-152">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="6c439-153">Столбец может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="6c439-153">The column can be multi-valued.</span></span> <span data-ttu-id="6c439-154">Столбец с несколькими значениями может иметь ноль, одно или несколько связанных с ним значений.</span><span class="sxs-lookup"><span data-stu-id="6c439-154">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="6c439-155">Различные значения в столбце с несколькими значениями определяются элементом <strong>итагсекуенце</strong> в различных структурах, например <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="6c439-155">The various values in a multi-valued column are identified by the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="6c439-156">Столбцы с несколькими значениями должны быть помечены как столбцы. Это значит, что они не могут быть столбцами фиксированной длины или переменной длины.</span><span class="sxs-lookup"><span data-stu-id="6c439-156">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c439-157">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="6c439-157">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="6c439-158">Столбец является столбцом депонированного обновления.</span><span class="sxs-lookup"><span data-stu-id="6c439-158">The column is an escrow update column.</span></span> <span data-ttu-id="6c439-159">Столбец депонированного обновления может обновляться параллельно разными сеансами с <a href="gg294125(v=exchg.10).md">жетескровупдате</a> и поддерживать согласованность транзакций.</span><span class="sxs-lookup"><span data-stu-id="6c439-159">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and maintain transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="6c439-160">Столбец депонированного обновления может быть создан только в том случае, если таблица пуста.</span><span class="sxs-lookup"><span data-stu-id="6c439-160">An escrow update column can be created only when the table is empty.</span></span></p></li>
<li><p><span data-ttu-id="6c439-161">Столбец депонированного обновления должен иметь тип <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="6c439-161">An escrow update column must be of type <strong>JET_coltypLong.</strong></span></span></p></li>
<li><p><span data-ttu-id="6c439-162">Столбец депонированного обновления должен иметь значение по умолчанию ( <strong>кбдефаулт</strong> должно быть положительным).</span><span class="sxs-lookup"><span data-stu-id="6c439-162">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
<li><p><span data-ttu-id="6c439-163">JET_bitColumnEscrowUpdate нельзя использовать в сочетании со следующими константами:</span><span class="sxs-lookup"><span data-stu-id="6c439-163">JET_bitColumnEscrowUpdate cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="6c439-164">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="6c439-164">JET_bitColumnTagged</span></span></p></li>
<li><p><span data-ttu-id="6c439-165">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="6c439-165">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="6c439-166">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="6c439-166">JET_bitColumnAutoincrement</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-167">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="6c439-167">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="6c439-168">Столбец создается без версии.</span><span class="sxs-lookup"><span data-stu-id="6c439-168">The column is created without a version.</span></span> <span data-ttu-id="6c439-169">Другие транзакции, пытающиеся добавить столбец с тем же именем, завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6c439-169">Other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="6c439-170">Этот бит удобен только для <a href="gg294122(v=exchg.10).md">жетаддколумн</a>.</span><span class="sxs-lookup"><span data-stu-id="6c439-170">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="6c439-171">Его нельзя использовать в транзакции.</span><span class="sxs-lookup"><span data-stu-id="6c439-171">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c439-172">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="6c439-172">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="6c439-173">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="6c439-173">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-174">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="6c439-174">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="6c439-175">Вместо JET_bitColumnFinalize используйте JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="6c439-175">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="6c439-176">JET_bitColumnFinalize указывает, что столбец может быть завершен.</span><span class="sxs-lookup"><span data-stu-id="6c439-176">JET_bitColumnFinalize specifies that a column can be finalized.</span></span> <span data-ttu-id="6c439-177">Если столбец, который может быть завершен, имеет столбец депонированного обновления, который достигает нуля, строка будет удалена.</span><span class="sxs-lookup"><span data-stu-id="6c439-177">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="6c439-178">В будущих версиях вместо этого можно вызвать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c439-178">Future versions can invoke a callback function instead.</span></span> <span data-ttu-id="6c439-179">Дополнительные сведения см. в разделе <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="6c439-179">For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="6c439-180">Столбец, который может быть завершен, должен быть столбцом типа "условно Update".</span><span class="sxs-lookup"><span data-stu-id="6c439-180">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="6c439-181">JET_bitColumnFinalize нельзя использовать с JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="6c439-181">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c439-182">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="6c439-182">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="6c439-183">Значение по умолчанию для столбца предоставляется функцией обратного вызова <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="6c439-183">The default value for a column is provided by the callback function, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="6c439-184">Столбец, содержащий определяемое пользователем значение по умолчанию, должен быть столбцом с тегами.</span><span class="sxs-lookup"><span data-stu-id="6c439-184">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="6c439-185"><strong>пвдефаулт</strong> должен указывать на структуру <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , а для <strong>кбдефаулт</strong> должно быть задано значение sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="6c439-185"><strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p>
<p><span data-ttu-id="6c439-186">JET_bitColumnUserDefinedDefault нельзя использовать в сочетании со следующими константами:</span><span class="sxs-lookup"><span data-stu-id="6c439-186">JET_bitColumnUserDefinedDefault cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="6c439-187">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="6c439-187">JET_bitColumnFixed</span></span></p></li>
<li><p><span data-ttu-id="6c439-188">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="6c439-188">JET_bitColumnNotNULL</span></span></p></li>
<li><p><span data-ttu-id="6c439-189">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="6c439-189">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="6c439-190">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="6c439-190">JET_bitColumnAutoincrement</span></span></p></li>
<li><p><span data-ttu-id="6c439-191">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="6c439-191">JET_bitColumnUpdatable</span></span></p></li>
<li><p><span data-ttu-id="6c439-192">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="6c439-192">JET_bitColumnEscrowUpdate</span></span></p></li>
<li><p><span data-ttu-id="6c439-193">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="6c439-193">JET_bitColumnFinalize</span></span></p></li>
<li><p><span data-ttu-id="6c439-194">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="6c439-194">JET_bitColumnDeleteOnZero</span></span></p></li>
<li><p><span data-ttu-id="6c439-195">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="6c439-195">JET_bitColumnMaybeNull</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-196">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="6c439-196">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="6c439-197">Столбец является столбцом депонированного обновления, и когда он достигает нуля, запись будет удалена.</span><span class="sxs-lookup"><span data-stu-id="6c439-197">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="6c439-198">Обычно для столбца, который может быть завершен, можно использовать его как поле счетчика ссылок, а когда поле достигает нуля, запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="6c439-198">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="6c439-199">JET_bitColumnDeleteOnZero связана с JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="6c439-199">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="6c439-200">Столбец Deleted-on-Zero должен быть столбцом депонированного обновления.</span><span class="sxs-lookup"><span data-stu-id="6c439-200">A delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="6c439-201">JET_bitColumnDeleteOnZero нельзя использовать с JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="6c439-201">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="6c439-202">JET_bitColumnDeleteOnZero нельзя использовать с пользовательскими столбцами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c439-202">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c439-203">**пвдефаулт**</span><span class="sxs-lookup"><span data-stu-id="6c439-203">**pvDefault**</span></span>

<span data-ttu-id="6c439-204">Указывает на буфер, который будет значением по умолчанию для столбца.</span><span class="sxs-lookup"><span data-stu-id="6c439-204">Points to a buffer which will be the default value for a column.</span></span> <span data-ttu-id="6c439-205">Длина буфера равна **кбдефаулт**.</span><span class="sxs-lookup"><span data-stu-id="6c439-205">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="6c439-206">Если значение по умолчанию отсутствует, **пвдефаулт** должно иметь значение null, а **кбдефаулт** — нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6c439-206">If there is no default, **pvDefault** should be set to NULL and **cbDefault** should be set to zero.</span></span> <span data-ttu-id="6c439-207">Если *грбит* имеет JET_bitColumnUserDefinedDefault, **пвдефаулт** будет интерпретироваться как указатель на структуру JET_USERDEFINEDDEFAULT.</span><span class="sxs-lookup"><span data-stu-id="6c439-207">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a JET_USERDEFINEDDEFAULT structure.</span></span> <span data-ttu-id="6c439-208">Значения по умолчанию не могут быть больше 255 байт.</span><span class="sxs-lookup"><span data-stu-id="6c439-208">Default values cannot be larger than 255 bytes.</span></span> <span data-ttu-id="6c439-209">Если значение по умолчанию превышает 255 байт, оно будет обрезано без уведомления.</span><span class="sxs-lookup"><span data-stu-id="6c439-209">If a default value is larger than 255 bytes, it will be silently truncated.</span></span>

<span data-ttu-id="6c439-210">**кбдефаулт**</span><span class="sxs-lookup"><span data-stu-id="6c439-210">**cbDefault**</span></span>

<span data-ttu-id="6c439-211">Размер (в байтах) буфера, заданного параметром **пвдефаулт**.</span><span class="sxs-lookup"><span data-stu-id="6c439-211">The size, in bytes, of the buffer specified by **pvDefault**.</span></span>

<span data-ttu-id="6c439-212">**cp**</span><span class="sxs-lookup"><span data-stu-id="6c439-212">**cp**</span></span>

<span data-ttu-id="6c439-213">Кодовая страница для столбца.</span><span class="sxs-lookup"><span data-stu-id="6c439-213">The code page for the column.</span></span> <span data-ttu-id="6c439-214">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="6c439-214">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="6c439-215">Нулевое значение означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="6c439-215">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="6c439-216">Если столбец не является текстовым столбцом, кодовая страница автоматически получает значение 0.</span><span class="sxs-lookup"><span data-stu-id="6c439-216">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="6c439-217">**columnid**</span><span class="sxs-lookup"><span data-stu-id="6c439-217">**columnid**</span></span>

<span data-ttu-id="6c439-218">При успешном завершении идентификатор столбца вновь созданного столбца будет передан обратно в это поле.</span><span class="sxs-lookup"><span data-stu-id="6c439-218">On success, the column identifier of the newly-created column will be passed back in this field.</span></span> <span data-ttu-id="6c439-219">При сбое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="6c439-219">On failure, the value is undefined.</span></span>

<span data-ttu-id="6c439-220">**Err**</span><span class="sxs-lookup"><span data-stu-id="6c439-220">**err**</span></span>

<span data-ttu-id="6c439-221">Поле **Err** будет содержать состояние создания этого столбца.</span><span class="sxs-lookup"><span data-stu-id="6c439-221">The **err** field will contain the status of creating this column.</span></span> <span data-ttu-id="6c439-222">Список вероятных возвращаемых значений см. в разделе [жетаддколумн](./jetaddcolumn-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6c439-222">See [JetAddColumn](./jetaddcolumn-function.md) for a list of likely return values.</span></span>

### <a name="requirements"></a><span data-ttu-id="6c439-223">Требования</span><span class="sxs-lookup"><span data-stu-id="6c439-223">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c439-224"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="6c439-224"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6c439-225">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6c439-225">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-226"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6c439-226"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6c439-227">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6c439-227">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c439-228"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6c439-228"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6c439-229">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6c439-229">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c439-230"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="6c439-230"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6c439-231">Реализуется как <strong>JET_COLUMNCREATE_W</strong> (Юникод) и <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6c439-231">Implemented as <strong>JET_COLUMNCREATE_W</strong> (Unicode) and <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6c439-232">См. также:</span><span class="sxs-lookup"><span data-stu-id="6c439-232">See Also</span></span>

[<span data-ttu-id="6c439-233">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="6c439-233">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="6c439-234">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="6c439-234">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="6c439-235">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6c439-235">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6c439-236">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6c439-236">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6c439-237">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="6c439-237">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="6c439-238">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6c439-238">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="6c439-239">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="6c439-239">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="6c439-240">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6c439-240">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="6c439-241">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="6c439-241">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="6c439-242">жетаддколумн</span><span class="sxs-lookup"><span data-stu-id="6c439-242">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="6c439-243">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="6c439-243">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="6c439-244">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="6c439-244">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="6c439-245">жетескровупдате</span><span class="sxs-lookup"><span data-stu-id="6c439-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="6c439-246">жетренамеколумн</span><span class="sxs-lookup"><span data-stu-id="6c439-246">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)  
[<span data-ttu-id="6c439-247">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="6c439-247">JetSetColumns</span></span>](./jetsetcolumns-function.md)
