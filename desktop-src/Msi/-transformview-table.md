---
description: Это временная таблица только для чтения, используемая для просмотра преобразований в режиме представления преобразования. Эта таблица никогда не сохраняется в установщике.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: Таблица _TransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545202"
---
# <a name="_transformview-table"></a><span data-ttu-id="6f16a-104">\_Таблица переformview</span><span class="sxs-lookup"><span data-stu-id="6f16a-104">\_TransformView Table</span></span>

<span data-ttu-id="6f16a-105">Это временная таблица только для чтения, используемая для просмотра преобразований в режиме представления преобразования.</span><span class="sxs-lookup"><span data-stu-id="6f16a-105">This is a read-only temporary table used to view transforms with the transform view mode.</span></span> <span data-ttu-id="6f16a-106">Эта таблица никогда не сохраняется в установщике.</span><span class="sxs-lookup"><span data-stu-id="6f16a-106">This table is never persisted by the installer.</span></span>

<span data-ttu-id="6f16a-107">Чтобы вызвать режим представления преобразования, получите маркер и откройте эталонную базу данных.</span><span class="sxs-lookup"><span data-stu-id="6f16a-107">To invoke the transform view mode, obtain a handle and open the reference database.</span></span> <span data-ttu-id="6f16a-108">См. раздел [Получение маркера базы данных](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="6f16a-108">See [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span> <span data-ttu-id="6f16a-109">Вызовите [**мсидатабасеапплитрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) с мситрансформ \_ Error \_ виевтрансформ.</span><span class="sxs-lookup"><span data-stu-id="6f16a-109">Call [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) with MSITRANSFORM\_ERROR\_VIEWTRANSFORM.</span></span> <span data-ttu-id="6f16a-110">Это приостанавливает преобразование к базе данных и выводит содержимое преобразования в \_ таблицу reformview.</span><span class="sxs-lookup"><span data-stu-id="6f16a-110">This stops the transform from being applied to the database and dumps the transform contents into the \_TransformView table.</span></span> <span data-ttu-id="6f16a-111">Доступ к данным в таблице можно получить с помощью SQL запросов.</span><span class="sxs-lookup"><span data-stu-id="6f16a-111">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="6f16a-112">См. раздел [Работа с запросами](working-with-queries.md).</span><span class="sxs-lookup"><span data-stu-id="6f16a-112">See [Working with Queries](working-with-queries.md).</span></span>

<span data-ttu-id="6f16a-113">\_Таблица преобразования не удаляется, когда применяется другое преобразование.</span><span class="sxs-lookup"><span data-stu-id="6f16a-113">The \_TransformView table is not cleared when another transform is applied.</span></span> <span data-ttu-id="6f16a-114">Таблица отражает совокупный результат последовательных приложений.</span><span class="sxs-lookup"><span data-stu-id="6f16a-114">The table reflects the cumulative effect of successive applications.</span></span> <span data-ttu-id="6f16a-115">Для просмотра преобразований по отдельности необходимо освободить таблицу.</span><span class="sxs-lookup"><span data-stu-id="6f16a-115">To view the transforms separately you must release the table.</span></span>

<span data-ttu-id="6f16a-116">\_Таблица переformview содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="6f16a-116">The \_TransformView Table has the following columns.</span></span>



| <span data-ttu-id="6f16a-117">Столбец</span><span class="sxs-lookup"><span data-stu-id="6f16a-117">Column</span></span>  | <span data-ttu-id="6f16a-118">Type</span><span class="sxs-lookup"><span data-stu-id="6f16a-118">Type</span></span>                         | <span data-ttu-id="6f16a-119">Ключ</span><span class="sxs-lookup"><span data-stu-id="6f16a-119">Key</span></span> | <span data-ttu-id="6f16a-120">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="6f16a-120">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="6f16a-121">Таблица</span><span class="sxs-lookup"><span data-stu-id="6f16a-121">Table</span></span>   | [<span data-ttu-id="6f16a-122">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6f16a-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="6f16a-123">Да</span><span class="sxs-lookup"><span data-stu-id="6f16a-123">Y</span></span>   | <span data-ttu-id="6f16a-124">Нет</span><span class="sxs-lookup"><span data-stu-id="6f16a-124">N</span></span>        |
| <span data-ttu-id="6f16a-125">Столбец</span><span class="sxs-lookup"><span data-stu-id="6f16a-125">Column</span></span>  | [<span data-ttu-id="6f16a-126">Text</span><span class="sxs-lookup"><span data-stu-id="6f16a-126">Text</span></span>](text.md)             | <span data-ttu-id="6f16a-127">Да</span><span class="sxs-lookup"><span data-stu-id="6f16a-127">Y</span></span>   | <span data-ttu-id="6f16a-128">Нет</span><span class="sxs-lookup"><span data-stu-id="6f16a-128">N</span></span>        |
| <span data-ttu-id="6f16a-129">Строка</span><span class="sxs-lookup"><span data-stu-id="6f16a-129">Row</span></span>     | [<span data-ttu-id="6f16a-130">Text</span><span class="sxs-lookup"><span data-stu-id="6f16a-130">Text</span></span>](text.md)             | <span data-ttu-id="6f16a-131">Да</span><span class="sxs-lookup"><span data-stu-id="6f16a-131">Y</span></span>   | <span data-ttu-id="6f16a-132">Да</span><span class="sxs-lookup"><span data-stu-id="6f16a-132">Y</span></span>        |
| <span data-ttu-id="6f16a-133">Данные</span><span class="sxs-lookup"><span data-stu-id="6f16a-133">Data</span></span>    | [<span data-ttu-id="6f16a-134">Text</span><span class="sxs-lookup"><span data-stu-id="6f16a-134">Text</span></span>](text.md)             | <span data-ttu-id="6f16a-135">Нет</span><span class="sxs-lookup"><span data-stu-id="6f16a-135">N</span></span>   | <span data-ttu-id="6f16a-136">Да</span><span class="sxs-lookup"><span data-stu-id="6f16a-136">Y</span></span>        |
| <span data-ttu-id="6f16a-137">Текущий</span><span class="sxs-lookup"><span data-stu-id="6f16a-137">Current</span></span> | [<span data-ttu-id="6f16a-138">Text</span><span class="sxs-lookup"><span data-stu-id="6f16a-138">Text</span></span>](text.md)             | <span data-ttu-id="6f16a-139">Нет</span><span class="sxs-lookup"><span data-stu-id="6f16a-139">N</span></span>   | <span data-ttu-id="6f16a-140">Да</span><span class="sxs-lookup"><span data-stu-id="6f16a-140">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="6f16a-141">Столбец</span><span class="sxs-lookup"><span data-stu-id="6f16a-141">Column</span></span>

<dl> <dt>

<span data-ttu-id="6f16a-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица</span><span class="sxs-lookup"><span data-stu-id="6f16a-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="6f16a-143">Имя измененной таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="6f16a-143">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="6f16a-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Рубрик</span><span class="sxs-lookup"><span data-stu-id="6f16a-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="6f16a-145">Имя измененного столбца таблицы или вставка, удаление, создание или удаление.</span><span class="sxs-lookup"><span data-stu-id="6f16a-145">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="6f16a-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Строки</span><span class="sxs-lookup"><span data-stu-id="6f16a-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="6f16a-147">Список значений первичного ключа, разделенных символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="6f16a-147">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="6f16a-148">Значения NULL первичного ключа представлены одним символом пробела.</span><span class="sxs-lookup"><span data-stu-id="6f16a-148">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="6f16a-149">Значение NULL в этом столбце указывает на изменение схемы.</span><span class="sxs-lookup"><span data-stu-id="6f16a-149">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="6f16a-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="6f16a-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="6f16a-151">Data, Name потока данных или определения столбца.</span><span class="sxs-lookup"><span data-stu-id="6f16a-151">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="6f16a-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Данном</span><span class="sxs-lookup"><span data-stu-id="6f16a-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="6f16a-153">Текущее значение из базы данных-образца или столбец с номером.</span><span class="sxs-lookup"><span data-stu-id="6f16a-153">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f16a-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f16a-154">Remarks</span></span>

<span data-ttu-id="6f16a-155">Объект \_ FormView удерживается в памяти с помощью счетчика блокировок, который можно освободить с помощью следующей команды SQL.</span><span class="sxs-lookup"><span data-stu-id="6f16a-155">The \_TransformView is held in memory by a lock count, that can be released with the following SQL command.</span></span>

<span data-ttu-id="6f16a-156">«ALTER TABLE reon \_ Free».</span><span class="sxs-lookup"><span data-stu-id="6f16a-156">"ALTER TABLE \_TransformView FREE".</span></span>

<span data-ttu-id="6f16a-157">Доступ к данным в таблице можно получить с помощью SQL запросов.</span><span class="sxs-lookup"><span data-stu-id="6f16a-157">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="6f16a-158">В языке SQL есть два основных подразделения: язык описания данных DDL, который используется для определения всех объектов в базе данных SQL, и языка обработки данных DML, который используется для выбора, вставки, обновления и удаления данных в объектах, определенных с помощью DDL.</span><span class="sxs-lookup"><span data-stu-id="6f16a-158">The SQL language has two main divisions: Data Definition Language (DDL) that is used to define all the objects in an SQL database, and Data Manipulation Language (DML) that is used to select, insert, update, and delete data in the objects defined using DDL.</span></span>

<span data-ttu-id="6f16a-159">Операции преобразования языка обработки данных (DML) обозначаются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6f16a-159">The Data Manipulation Language (DML) transform operations are indicated as follows.</span></span> <span data-ttu-id="6f16a-160">Язык обработки данных DML — это инструкции в SQL, которые управляют, а не определяют данные.</span><span class="sxs-lookup"><span data-stu-id="6f16a-160">Data Manipulation Language (DML) are those statements in SQL that manipulate, as opposed to define, data.</span></span>



| <span data-ttu-id="6f16a-161">Операция преобразования</span><span class="sxs-lookup"><span data-stu-id="6f16a-161">Transform operation</span></span> | <span data-ttu-id="6f16a-162">Результат SQL</span><span class="sxs-lookup"><span data-stu-id="6f16a-162">SQL result</span></span>                                    |
|---------------------|-----------------------------------------------|
| <span data-ttu-id="6f16a-163">Изменение данных</span><span class="sxs-lookup"><span data-stu-id="6f16a-163">Modify data</span></span>         | <span data-ttu-id="6f16a-164">Таблица рубрик строки Data {Текущее значение}</span><span class="sxs-lookup"><span data-stu-id="6f16a-164">{table} {column} {row} {data} {current value}</span></span> |
| <span data-ttu-id="6f16a-165">Вставка строки</span><span class="sxs-lookup"><span data-stu-id="6f16a-165">Insert row</span></span>          | <span data-ttu-id="6f16a-166">Таблица «INSERT» {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="6f16a-166">{table} "INSERT" {row} NULL NULL</span></span>              |
| <span data-ttu-id="6f16a-167">Удаление строки</span><span class="sxs-lookup"><span data-stu-id="6f16a-167">Delete row</span></span>          | <span data-ttu-id="6f16a-168">Таблица «DELETE» {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="6f16a-168">{table} "DELETE" {row} NULL NULL</span></span>              |



 

<span data-ttu-id="6f16a-169">Операции преобразования языка описания данных DDL указываются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6f16a-169">The Data Definition Language (DDL) transform operations are indicated as follows.</span></span> <span data-ttu-id="6f16a-170">Язык описания данных (DDL) — это инструкции в SQL, которые определяют, а не управляют данными.</span><span class="sxs-lookup"><span data-stu-id="6f16a-170">Data Definition Language (DDL) are those statements in SQL that define, as opposed to manipulate, data.</span></span>



| <span data-ttu-id="6f16a-171">Операция преобразования</span><span class="sxs-lookup"><span data-stu-id="6f16a-171">Transform operation</span></span> | <span data-ttu-id="6f16a-172">Результат SQL</span><span class="sxs-lookup"><span data-stu-id="6f16a-172">SQL result</span></span>                                   |
|---------------------|----------------------------------------------|
| <span data-ttu-id="6f16a-173">Добавление столбца</span><span class="sxs-lookup"><span data-stu-id="6f16a-173">Add column</span></span>          | <span data-ttu-id="6f16a-174">Таблица рубрик NULL {дефн} {номер столбца}</span><span class="sxs-lookup"><span data-stu-id="6f16a-174">{table} {column} NULL {defn} {column number}</span></span> |
| <span data-ttu-id="6f16a-175">Добавить таблицу</span><span class="sxs-lookup"><span data-stu-id="6f16a-175">Add table</span></span>           | <span data-ttu-id="6f16a-176">Таблица "CREATE" NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="6f16a-176">{table} "CREATE" NULL NULL NULL</span></span>              |
| <span data-ttu-id="6f16a-177">Удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="6f16a-177">Drop table</span></span>          | <span data-ttu-id="6f16a-178">Таблица "DROP" NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="6f16a-178">{table} "DROP" NULL NULL NULL</span></span>                |



 

<span data-ttu-id="6f16a-179">Когда приложение преобразования добавляет эту таблицу, поле данных получает текст, который может интерпретироваться как 16-разрядное целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="6f16a-179">When the application of a transform adds this table, the Data field receives text that can be interpreted as a 16-bit integer value.</span></span> <span data-ttu-id="6f16a-180">Значение описывает столбец с именем в поле Column.</span><span class="sxs-lookup"><span data-stu-id="6f16a-180">The value describes the column named in the Column field.</span></span> <span data-ttu-id="6f16a-181">Можно сравнить целочисленное значение с константами в следующей таблице, чтобы определить определение изменяемого столбца.</span><span class="sxs-lookup"><span data-stu-id="6f16a-181">You can compare the integer value to the constants in the following table to determine the definition of the altered column.</span></span>



| <span data-ttu-id="6f16a-182">bit</span><span class="sxs-lookup"><span data-stu-id="6f16a-182">Bit</span></span>                                                                                                       | <span data-ttu-id="6f16a-183">Описание</span><span class="sxs-lookup"><span data-stu-id="6f16a-183">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f16a-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>BITS 0 7</span><span class="sxs-lookup"><span data-stu-id="6f16a-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span></span><br/>         | <span data-ttu-id="6f16a-185">Шестнадцатеричное: Символ 0x0000 0x0100</span><span class="sxs-lookup"><span data-stu-id="6f16a-185">Hexadecimal: 0x0000 0x0100</span></span><br/> <span data-ttu-id="6f16a-186">Десятичное число: 0 255</span><span class="sxs-lookup"><span data-stu-id="6f16a-186">Decimal: 0 255</span></span><br/> <span data-ttu-id="6f16a-187">Ширина столбца</span><span class="sxs-lookup"><span data-stu-id="6f16a-187">Column width</span></span><br/>                                                                                                                                                                                                                                  |
| <span data-ttu-id="6f16a-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Бит 8</span><span class="sxs-lookup"><span data-stu-id="6f16a-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span></span><br/>                  | <span data-ttu-id="6f16a-189">Шестнадцатеричное: 0x0100</span><span class="sxs-lookup"><span data-stu-id="6f16a-189">Hexadecimal: 0x0100</span></span><br/> <span data-ttu-id="6f16a-190">Десятичное число: 256</span><span class="sxs-lookup"><span data-stu-id="6f16a-190">Decimal: 256</span></span><br/> <span data-ttu-id="6f16a-191">Постоянный столбец.</span><span class="sxs-lookup"><span data-stu-id="6f16a-191">A persistent column.</span></span> <span data-ttu-id="6f16a-192">Ноль означает временный столбец.</span><span class="sxs-lookup"><span data-stu-id="6f16a-192">Zero means a temporary column.</span></span> <br/>                                                                                                                                                                                                   |
| <span data-ttu-id="6f16a-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Бит 9</span><span class="sxs-lookup"><span data-stu-id="6f16a-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span></span><br/>                  | <span data-ttu-id="6f16a-194">Шестнадцатеричное: 0x0200</span><span class="sxs-lookup"><span data-stu-id="6f16a-194">Hexadecimal: 0x0200</span></span><br/> <span data-ttu-id="6f16a-195">Десятичное число: 1023</span><span class="sxs-lookup"><span data-stu-id="6f16a-195">Decimal: 1023</span></span><br/> <span data-ttu-id="6f16a-196">Локализуемый столбец.</span><span class="sxs-lookup"><span data-stu-id="6f16a-196">A localizable column.</span></span> <span data-ttu-id="6f16a-197">Ноль означает, что столбец не может быть локализован.</span><span class="sxs-lookup"><span data-stu-id="6f16a-197">Zero means the column cannot be localized.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="6f16a-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>BITS 10 11</span><span class="sxs-lookup"><span data-stu-id="6f16a-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span></span><br/> | <span data-ttu-id="6f16a-199">Шестнадцатеричное: Символ 0x0000</span><span class="sxs-lookup"><span data-stu-id="6f16a-199">Hexadecimal: 0x0000</span></span><br/> <span data-ttu-id="6f16a-200">Десятичное число: 0</span><span class="sxs-lookup"><span data-stu-id="6f16a-200">Decimal: 0</span></span><br/> <span data-ttu-id="6f16a-201">Long integer</span><span class="sxs-lookup"><span data-stu-id="6f16a-201">Long integer</span></span><br/> <span data-ttu-id="6f16a-202">Шестнадцатеричное: 0x0400</span><span class="sxs-lookup"><span data-stu-id="6f16a-202">Hexadecimal: 0x0400</span></span><br/> <span data-ttu-id="6f16a-203">Десятичное число: 1024</span><span class="sxs-lookup"><span data-stu-id="6f16a-203">Decimal: 1024</span></span><br/> <span data-ttu-id="6f16a-204">Короткое целое</span><span class="sxs-lookup"><span data-stu-id="6f16a-204">Short integer</span></span><br/> <span data-ttu-id="6f16a-205">Шестнадцатеричное: 0x0800</span><span class="sxs-lookup"><span data-stu-id="6f16a-205">Hexadecimal: 0x0800</span></span><br/> <span data-ttu-id="6f16a-206">Десятичное число: 2048</span><span class="sxs-lookup"><span data-stu-id="6f16a-206">Decimal: 2048</span></span><br/> <span data-ttu-id="6f16a-207">Двоичный объект</span><span class="sxs-lookup"><span data-stu-id="6f16a-207">Binary object</span></span><br/> <span data-ttu-id="6f16a-208">Шестнадцатеричное: 0x0C00</span><span class="sxs-lookup"><span data-stu-id="6f16a-208">Hexadecimal: 0x0C00</span></span><br/> <span data-ttu-id="6f16a-209">Десятичное число: 3072</span><span class="sxs-lookup"><span data-stu-id="6f16a-209">Decimal: 3072</span></span><br/> <span data-ttu-id="6f16a-210">Строка</span><span class="sxs-lookup"><span data-stu-id="6f16a-210">String</span></span><br/> |
| <span data-ttu-id="6f16a-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Бит 12</span><span class="sxs-lookup"><span data-stu-id="6f16a-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span></span><br/>              | <span data-ttu-id="6f16a-212">Шестнадцатеричное: 0x1000</span><span class="sxs-lookup"><span data-stu-id="6f16a-212">Hexadecimal: 0x1000</span></span><br/> <span data-ttu-id="6f16a-213">Десятичное число: 4096</span><span class="sxs-lookup"><span data-stu-id="6f16a-213">Decimal: 4096</span></span><br/> <span data-ttu-id="6f16a-214">Столбец, допускающий значение null.</span><span class="sxs-lookup"><span data-stu-id="6f16a-214">Nullable column.</span></span> <span data-ttu-id="6f16a-215">Ноль означает, что столбец не допускает значения NULL.</span><span class="sxs-lookup"><span data-stu-id="6f16a-215">Zero means the column is non-nullable.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="6f16a-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Бит 13</span><span class="sxs-lookup"><span data-stu-id="6f16a-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span></span><br/>              | <span data-ttu-id="6f16a-217">Шестнадцатеричное: 0x2000</span><span class="sxs-lookup"><span data-stu-id="6f16a-217">Hexadecimal: 0x2000</span></span><br/> <span data-ttu-id="6f16a-218">Десятичное число: 8192</span><span class="sxs-lookup"><span data-stu-id="6f16a-218">Decimal: 8192</span></span><br/> <span data-ttu-id="6f16a-219">Первичный ключевой столбец.</span><span class="sxs-lookup"><span data-stu-id="6f16a-219">Primary key column.</span></span> <span data-ttu-id="6f16a-220">Ноль означает, что этот столбец не является первичным ключом.</span><span class="sxs-lookup"><span data-stu-id="6f16a-220">Zero means this column is not a primary key.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="6f16a-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>BITS 14 15</span><span class="sxs-lookup"><span data-stu-id="6f16a-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span></span><br/> | <span data-ttu-id="6f16a-222">Шестнадцатеричное: 0x4000 0x8000</span><span class="sxs-lookup"><span data-stu-id="6f16a-222">Hexadecimal: 0x4000 0x8000</span></span><br/> <span data-ttu-id="6f16a-223">Десятичное число: 16384 32768</span><span class="sxs-lookup"><span data-stu-id="6f16a-223">Decimal: 16384 32768</span></span><br/> <span data-ttu-id="6f16a-224">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="6f16a-224">Reserved</span></span><br/>                                                                                                                                                                                                                                |



 

<span data-ttu-id="6f16a-225">Пример сценария, демонстрирующий \_ таблицу преобразований, см. в разделе [Просмотр преобразования](view-a-transform.md).</span><span class="sxs-lookup"><span data-stu-id="6f16a-225">For a script sample that demonstrates the \_TransformView table, see [View a Transform](view-a-transform.md).</span></span>

 

 




