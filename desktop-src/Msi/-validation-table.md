---
description: '\_Таблица проверки — это системная таблица, содержащая имена столбцов и значения столбцов для всех таблиц в базе данных.'
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: Таблица _Validation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909160"
---
# <a name="_validation-table"></a><span data-ttu-id="27e5f-103">\_Таблица проверки</span><span class="sxs-lookup"><span data-stu-id="27e5f-103">\_Validation Table</span></span>

<span data-ttu-id="27e5f-104">\_Таблица проверки — это системная таблица, содержащая имена столбцов и значения столбцов для всех таблиц в базе данных.</span><span class="sxs-lookup"><span data-stu-id="27e5f-104">The \_Validation table is a system table that contains the column names and the column values for all of the tables in the database.</span></span> <span data-ttu-id="27e5f-105">Он используется в процессе проверки базы данных, чтобы убедиться в том, что для всех столбцов учитывается правильность значений.</span><span class="sxs-lookup"><span data-stu-id="27e5f-105">It is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="27e5f-106">Эта таблица не поставляется с базой данных установщика.</span><span class="sxs-lookup"><span data-stu-id="27e5f-106">This table is not shipped with the installer database.</span></span>

<span data-ttu-id="27e5f-107">\_Таблица проверки содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="27e5f-107">The \_Validation table has the following columns.</span></span>



| <span data-ttu-id="27e5f-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="27e5f-108">Column</span></span>      | <span data-ttu-id="27e5f-109">Type</span><span class="sxs-lookup"><span data-stu-id="27e5f-109">Type</span></span>                               | <span data-ttu-id="27e5f-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="27e5f-110">Key</span></span> | <span data-ttu-id="27e5f-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="27e5f-111">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="27e5f-112">Таблица</span><span class="sxs-lookup"><span data-stu-id="27e5f-112">Table</span></span>       | [<span data-ttu-id="27e5f-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="27e5f-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="27e5f-114">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-114">Y</span></span>   | <span data-ttu-id="27e5f-115">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-115">N</span></span>        |
| <span data-ttu-id="27e5f-116">Столбец</span><span class="sxs-lookup"><span data-stu-id="27e5f-116">Column</span></span>      | [<span data-ttu-id="27e5f-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="27e5f-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="27e5f-118">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-118">Y</span></span>   | <span data-ttu-id="27e5f-119">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-119">N</span></span>        |
| <span data-ttu-id="27e5f-120">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="27e5f-120">Nullable</span></span>    | [<span data-ttu-id="27e5f-121">Text</span><span class="sxs-lookup"><span data-stu-id="27e5f-121">Text</span></span>](text.md)                   | <span data-ttu-id="27e5f-122">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-122">N</span></span>   | <span data-ttu-id="27e5f-123">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-123">N</span></span>        |
| <span data-ttu-id="27e5f-124">MinValue</span><span class="sxs-lookup"><span data-stu-id="27e5f-124">MinValue</span></span>    | [<span data-ttu-id="27e5f-125">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="27e5f-125">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="27e5f-126">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-126">N</span></span>   | <span data-ttu-id="27e5f-127">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-127">Y</span></span>        |
| <span data-ttu-id="27e5f-128">MaxValue</span><span class="sxs-lookup"><span data-stu-id="27e5f-128">MaxValue</span></span>    | [<span data-ttu-id="27e5f-129">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="27e5f-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="27e5f-130">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-130">N</span></span>   | <span data-ttu-id="27e5f-131">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-131">Y</span></span>        |
| <span data-ttu-id="27e5f-132">кэйтабле</span><span class="sxs-lookup"><span data-stu-id="27e5f-132">KeyTable</span></span>    | [<span data-ttu-id="27e5f-133">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="27e5f-133">Identifier</span></span>](identifier.md)       | <span data-ttu-id="27e5f-134">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-134">N</span></span>   | <span data-ttu-id="27e5f-135">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-135">Y</span></span>        |
| <span data-ttu-id="27e5f-136">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="27e5f-136">KeyColumn</span></span>   | [<span data-ttu-id="27e5f-137">Integer</span><span class="sxs-lookup"><span data-stu-id="27e5f-137">Integer</span></span>](integer.md)             | <span data-ttu-id="27e5f-138">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-138">N</span></span>   | <span data-ttu-id="27e5f-139">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-139">Y</span></span>        |
| <span data-ttu-id="27e5f-140">Категория</span><span class="sxs-lookup"><span data-stu-id="27e5f-140">Category</span></span>    | [<span data-ttu-id="27e5f-141">Text</span><span class="sxs-lookup"><span data-stu-id="27e5f-141">Text</span></span>](text.md)                   | <span data-ttu-id="27e5f-142">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-142">N</span></span>   | <span data-ttu-id="27e5f-143">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-143">Y</span></span>        |
| <span data-ttu-id="27e5f-144">Присвойте параметру</span><span class="sxs-lookup"><span data-stu-id="27e5f-144">Set</span></span>         | [<span data-ttu-id="27e5f-145">Text</span><span class="sxs-lookup"><span data-stu-id="27e5f-145">Text</span></span>](text.md)                   | <span data-ttu-id="27e5f-146">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-146">N</span></span>   | <span data-ttu-id="27e5f-147">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-147">Y</span></span>        |
| <span data-ttu-id="27e5f-148">Описание</span><span class="sxs-lookup"><span data-stu-id="27e5f-148">Description</span></span> | [<span data-ttu-id="27e5f-149">Text</span><span class="sxs-lookup"><span data-stu-id="27e5f-149">Text</span></span>](text.md)                   | <span data-ttu-id="27e5f-150">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-150">N</span></span>   | <span data-ttu-id="27e5f-151">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="27e5f-152">Столбцы</span><span class="sxs-lookup"><span data-stu-id="27e5f-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="27e5f-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица</span><span class="sxs-lookup"><span data-stu-id="27e5f-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-154">Используется для задания конкретной таблицы.</span><span class="sxs-lookup"><span data-stu-id="27e5f-154">Used to identify a particular table.</span></span> <span data-ttu-id="27e5f-155">Этот ключ и ключ столбца образуют первичный ключ \_ таблицы проверки.</span><span class="sxs-lookup"><span data-stu-id="27e5f-155">This key and the Column key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="27e5f-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Рубрик</span><span class="sxs-lookup"><span data-stu-id="27e5f-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-157">Используется для обнаружения определенного столбца таблицы.</span><span class="sxs-lookup"><span data-stu-id="27e5f-157">Used to identify a particular column of the table.</span></span> <span data-ttu-id="27e5f-158">Этот ключ и ключ таблицы образуют первичный ключ \_ таблицы проверки.</span><span class="sxs-lookup"><span data-stu-id="27e5f-158">This key and the Table key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="27e5f-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Обнуляемого</span><span class="sxs-lookup"><span data-stu-id="27e5f-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-160">Определяет, может ли столбец содержать значение null.</span><span class="sxs-lookup"><span data-stu-id="27e5f-160">Identifies whether the column may contain a Null value.</span></span>

<span data-ttu-id="27e5f-161">Этот столбец может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="27e5f-161">This column may have one of the following values.</span></span>



| <span data-ttu-id="27e5f-162">Строка</span><span class="sxs-lookup"><span data-stu-id="27e5f-162">String</span></span> | <span data-ttu-id="27e5f-163">Значение</span><span class="sxs-lookup"><span data-stu-id="27e5f-163">Meaning</span></span>                                   |
|--------|-------------------------------------------|
| <span data-ttu-id="27e5f-164">Да</span><span class="sxs-lookup"><span data-stu-id="27e5f-164">Y</span></span>      | <span data-ttu-id="27e5f-165">Да, столбец может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="27e5f-165">Yes, the column may have a Null value.</span></span>    |
| <span data-ttu-id="27e5f-166">Нет</span><span class="sxs-lookup"><span data-stu-id="27e5f-166">N</span></span>      | <span data-ttu-id="27e5f-167">Нет, столбец не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="27e5f-167">No, the column may not have a Null value.</span></span> |



 

</dd> <dt>

<span data-ttu-id="27e5f-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span><span class="sxs-lookup"><span data-stu-id="27e5f-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-169">Это поле применяется к столбцам, имеющим числовое значение.</span><span class="sxs-lookup"><span data-stu-id="27e5f-169">This field applies to columns having numeric value.</span></span> <span data-ttu-id="27e5f-170">Поле содержит минимальное допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="27e5f-170">The field contains the minimum permissible value.</span></span> <span data-ttu-id="27e5f-171">Это может быть минимальное значение для целого числа или минимальное значение для даты или строки версии.</span><span class="sxs-lookup"><span data-stu-id="27e5f-171">This can be the minimum value for an integer or the minimum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="27e5f-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span><span class="sxs-lookup"><span data-stu-id="27e5f-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-173">Это поле применяется к столбцам, имеющим числовое значение.</span><span class="sxs-lookup"><span data-stu-id="27e5f-173">This field applies to columns having numeric value.</span></span> <span data-ttu-id="27e5f-174">Поле является максимальным допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="27e5f-174">The field is the maximum permissible value.</span></span> <span data-ttu-id="27e5f-175">Это может быть максимальное значение для целого числа или максимальное значение для даты или строки версии.</span><span class="sxs-lookup"><span data-stu-id="27e5f-175">This may be the maximum value for an integer or the maximum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="27e5f-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>кэйтабле</span><span class="sxs-lookup"><span data-stu-id="27e5f-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-177">Это поле применяется к столбцам, которые являются внешними ключами.</span><span class="sxs-lookup"><span data-stu-id="27e5f-177">This field applies to columns that are external keys.</span></span> <span data-ttu-id="27e5f-178">Поле, указанное в столбце, должно ссылаться на номер столбца, заданный столбцом KeyColumn в таблице с именем в Кэйтабле.</span><span class="sxs-lookup"><span data-stu-id="27e5f-178">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="27e5f-179">Это может быть список таблиц, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="27e5f-179">This can be a list of tables separated by semicolons.</span></span>

</dd> <dt>

<span data-ttu-id="27e5f-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span><span class="sxs-lookup"><span data-stu-id="27e5f-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-181">Это поле применяется к столбцам таблицы, которые являются внешними ключами.</span><span class="sxs-lookup"><span data-stu-id="27e5f-181">This field applies to table columns that are external keys.</span></span> <span data-ttu-id="27e5f-182">Поле, указанное в столбце, должно ссылаться на номер столбца, заданный столбцом KeyColumn в таблице с именем в Кэйтабле.</span><span class="sxs-lookup"><span data-stu-id="27e5f-182">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="27e5f-183">Допустимый диапазон значений поля KeyColumn — 1-32.</span><span class="sxs-lookup"><span data-stu-id="27e5f-183">The permissible range of the KeyColumn field is 1-32.</span></span>

</dd> <dt>

<span data-ttu-id="27e5f-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Категори</span><span class="sxs-lookup"><span data-stu-id="27e5f-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-185">Это тип данных, содержащихся в поле базы данных, заданном столбцами таблицы и столбца \_ проверки.</span><span class="sxs-lookup"><span data-stu-id="27e5f-185">This is the type of data contained by the database field specified by the Table and Column columns of the \_Validation table.</span></span> <span data-ttu-id="27e5f-186">Если это тип с числовым значением, например [Integer](integer.md), [даублеинтежер](doubleinteger.md) или [Time/Date](time-date.md), введите NULL в это поле и укажите диапазон значений с помощью столбцов MinValue и MaxValue.</span><span class="sxs-lookup"><span data-stu-id="27e5f-186">If this is a type having a numeric value, such as [Integer](integer.md), [DoubleInteger](doubleinteger.md) or [Time/Date](time-date.md), then enter null into this field and specify the value's range using the MinValue and MaxValue columns.</span></span> <span data-ttu-id="27e5f-187">Используйте столбец Категория, чтобы указать нечисловые типы данных, описанные в разделе [типы данных столбцов](column-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="27e5f-187">Use the Category column to specify the non-numeric data types described in [Column Data Types](column-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5f-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Параметр</span><span class="sxs-lookup"><span data-stu-id="27e5f-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-189">Это список допустимых значений для этого поля, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="27e5f-189">This is a list of permissible values for this field separated by semicolons.</span></span> <span data-ttu-id="27e5f-190">Это поле обычно используется для перечислений.</span><span class="sxs-lookup"><span data-stu-id="27e5f-190">This field is usually used for enumerations.</span></span>

</dd> <dt>

<span data-ttu-id="27e5f-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="27e5f-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="27e5f-192">Описание данных, хранящихся в столбце.</span><span class="sxs-lookup"><span data-stu-id="27e5f-192">A description of the data that is stored in the column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="27e5f-193">Проверка</span><span class="sxs-lookup"><span data-stu-id="27e5f-193">Validation</span></span>

<dl>

[<span data-ttu-id="27e5f-194">ICE03</span><span class="sxs-lookup"><span data-stu-id="27e5f-194">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="27e5f-195">ICE06</span><span class="sxs-lookup"><span data-stu-id="27e5f-195">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="27e5f-196">ICE32</span><span class="sxs-lookup"><span data-stu-id="27e5f-196">ICE32</span></span>](ice32.md)  
</dl>

## <a name="remarks"></a><span data-ttu-id="27e5f-197">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27e5f-197">Remarks</span></span>

<span data-ttu-id="27e5f-198">Поле категории этой таблицы применяется только к строковым данным.</span><span class="sxs-lookup"><span data-stu-id="27e5f-198">The Category field of this table only applies to string data.</span></span> <span data-ttu-id="27e5f-199">Если поле столбца ссылается на столбец с двоичными данными, то в поле Category должен быть указан двоичный тип данных.</span><span class="sxs-lookup"><span data-stu-id="27e5f-199">If the Column field refers to a column with binary data, the binary data type must be specified in the Category field.</span></span> <span data-ttu-id="27e5f-200">Типы столбцов целочисленных данных игнорируют поле Category во время проверки.</span><span class="sxs-lookup"><span data-stu-id="27e5f-200">Integer data Column types ignore the Category field during validation.</span></span>

 

 



