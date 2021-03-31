---
description: Мсивиевжетколумнинфо и свойство ColumnInfo объекта View используют следующий формат для описания определений столбцов базы данных.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Формат определения столбца
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264860"
---
# <a name="column-definition-format"></a><span data-ttu-id="5772b-103">Формат определения столбца</span><span class="sxs-lookup"><span data-stu-id="5772b-103">Column Definition Format</span></span>

<span data-ttu-id="5772b-104">[**Мсивиевжетколумнинфо**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) и [**свойство ColumnInfo**](view-columninfo.md) объекта [**View**](view-object.md) используют следующий формат для описания определений столбцов базы данных.</span><span class="sxs-lookup"><span data-stu-id="5772b-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) and the [**ColumnInfo Property**](view-columninfo.md) of the [**View**](view-object.md) object use the following format to describe database column definitions.</span></span> <span data-ttu-id="5772b-105">Каждый столбец описывается строкой в соответствующем поле записи, возвращаемом функцией или свойством.</span><span class="sxs-lookup"><span data-stu-id="5772b-105">Each column is described by a string in the corresponding record field returned by the function or property.</span></span> <span data-ttu-id="5772b-106">Строка определения состоит из одной буквы, представляющей тип данных, за которой следует ширина столбца (в символах, если применимо, байтов в противном случае).</span><span class="sxs-lookup"><span data-stu-id="5772b-106">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise).</span></span> <span data-ttu-id="5772b-107">Нулевая ширина означает неограниченную ширину (например, длинные текстовые поля и потоки).</span><span class="sxs-lookup"><span data-stu-id="5772b-107">A width of zero designates an unbounded width (for example, long text fields and streams).</span></span> <span data-ttu-id="5772b-108">Прописная буква означает, что в столбце разрешены значения NULL.</span><span class="sxs-lookup"><span data-stu-id="5772b-108">An uppercase letter indicates that null values are allowed in the column.</span></span>



| <span data-ttu-id="5772b-109">Дескриптор столбца</span><span class="sxs-lookup"><span data-stu-id="5772b-109">Column descriptor</span></span> | <span data-ttu-id="5772b-110">Строка определения</span><span class="sxs-lookup"><span data-stu-id="5772b-110">Definition string</span></span>                 |
|-------------------|-----------------------------------|
| <span data-ttu-id="5772b-111">#d0?</span><span class="sxs-lookup"><span data-stu-id="5772b-111">s?</span></span>                | <span data-ttu-id="5772b-112">Строка, переменная длина (? = 1-255)</span><span class="sxs-lookup"><span data-stu-id="5772b-112">String, variable length (?=1-255)</span></span> |
| <span data-ttu-id="5772b-113">сна</span><span class="sxs-lookup"><span data-stu-id="5772b-113">s0</span></span>                | <span data-ttu-id="5772b-114">Строка, переменная длина</span><span class="sxs-lookup"><span data-stu-id="5772b-114">String, variable length</span></span>           |
| <span data-ttu-id="5772b-115">i2</span><span class="sxs-lookup"><span data-stu-id="5772b-115">i2</span></span>                | <span data-ttu-id="5772b-116">Короткое целое</span><span class="sxs-lookup"><span data-stu-id="5772b-116">Short integer</span></span>                     |
| <span data-ttu-id="5772b-117">i4</span><span class="sxs-lookup"><span data-stu-id="5772b-117">i4</span></span>                | <span data-ttu-id="5772b-118">Long integer</span><span class="sxs-lookup"><span data-stu-id="5772b-118">Long integer</span></span>                      |
| <span data-ttu-id="5772b-119">v0</span><span class="sxs-lookup"><span data-stu-id="5772b-119">v0</span></span>                | <span data-ttu-id="5772b-120">Двоичный поток</span><span class="sxs-lookup"><span data-stu-id="5772b-120">Binary Stream</span></span>                     |
| <span data-ttu-id="5772b-121">модуле?</span><span class="sxs-lookup"><span data-stu-id="5772b-121">g?</span></span>                | <span data-ttu-id="5772b-122">Временная строка (? = 0-255)</span><span class="sxs-lookup"><span data-stu-id="5772b-122">Temporary string (?=0-255)</span></span>        |
| <span data-ttu-id="5772b-123">б?</span><span class="sxs-lookup"><span data-stu-id="5772b-123">j?</span></span>                | <span data-ttu-id="5772b-124">Временное целое число (? = 0, 1, 2, 4)</span><span class="sxs-lookup"><span data-stu-id="5772b-124">Temporary integer (?=0,1,2,4)</span></span>     |
| <span data-ttu-id="5772b-125">O0</span><span class="sxs-lookup"><span data-stu-id="5772b-125">O0</span></span>                | <span data-ttu-id="5772b-126">Временный объект</span><span class="sxs-lookup"><span data-stu-id="5772b-126">Temporary object</span></span>                  |



 

<span data-ttu-id="5772b-127">Строки, используемые для описания столбцов, имеют следующую связь со строками запросов SQL, используемыми CREATE и ALTER.</span><span class="sxs-lookup"><span data-stu-id="5772b-127">The strings used to describe columns have the following relationship to the SQL query strings used by CREATE and ALTER.</span></span> <span data-ttu-id="5772b-128">Дополнительные сведения см. в разделе [синтаксис SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="5772b-128">For more information, see [SQL Syntax](sql-syntax.md).</span></span>



| <span data-ttu-id="5772b-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5772b-129">Returned value</span></span> | <span data-ttu-id="5772b-130">Синтаксис SQL</span><span class="sxs-lookup"><span data-stu-id="5772b-130">SQL syntax</span></span>                |
|----------------|---------------------------|
| <span data-ttu-id="5772b-131">сна</span><span class="sxs-lookup"><span data-stu-id="5772b-131">s0</span></span>             | <span data-ttu-id="5772b-132">лонгчар</span><span class="sxs-lookup"><span data-stu-id="5772b-132">LONGCHAR</span></span>                  |
| <span data-ttu-id="5772b-133">объединения</span><span class="sxs-lookup"><span data-stu-id="5772b-133">l0</span></span>             | <span data-ttu-id="5772b-134">ЛОНГЧАР ДЛЯ ЛОКАЛИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="5772b-134">LONGCHAR LOCALIZABLE</span></span>      |
| <span data-ttu-id="5772b-135">#d0 \#</span><span class="sxs-lookup"><span data-stu-id="5772b-135">s \#</span></span>           | <span data-ttu-id="5772b-136">CHAR ( \# )</span><span class="sxs-lookup"><span data-stu-id="5772b-136">CHAR(\#)</span></span>                  |
| <span data-ttu-id="5772b-137">#d0 \#</span><span class="sxs-lookup"><span data-stu-id="5772b-137">s \#</span></span>           | <span data-ttu-id="5772b-138">CHARACTER ( \# )</span><span class="sxs-lookup"><span data-stu-id="5772b-138">CHARACTER(\#)</span></span>             |
| <span data-ttu-id="5772b-139">н \#</span><span class="sxs-lookup"><span data-stu-id="5772b-139">l \#</span></span>           | <span data-ttu-id="5772b-140">ТИП CHAR ( \# ) — локализуемый</span><span class="sxs-lookup"><span data-stu-id="5772b-140">CHAR(\#) LOCALIZABLE</span></span>      |
| <span data-ttu-id="5772b-141">н \#</span><span class="sxs-lookup"><span data-stu-id="5772b-141">l \#</span></span>           | <span data-ttu-id="5772b-142">подлежит \# локализации символ ()</span><span class="sxs-lookup"><span data-stu-id="5772b-142">CHARACTER(\#) LOCALIZABLE</span></span> |
| <span data-ttu-id="5772b-143">i2</span><span class="sxs-lookup"><span data-stu-id="5772b-143">i2</span></span>             | <span data-ttu-id="5772b-144">SHORT</span><span class="sxs-lookup"><span data-stu-id="5772b-144">SHORT</span></span>                     |
| <span data-ttu-id="5772b-145">i2</span><span class="sxs-lookup"><span data-stu-id="5772b-145">i2</span></span>             | <span data-ttu-id="5772b-146">INT</span><span class="sxs-lookup"><span data-stu-id="5772b-146">INT</span></span>                       |
| <span data-ttu-id="5772b-147">i2</span><span class="sxs-lookup"><span data-stu-id="5772b-147">i2</span></span>             | <span data-ttu-id="5772b-148">INTEGER</span><span class="sxs-lookup"><span data-stu-id="5772b-148">INTEGER</span></span>                   |
| <span data-ttu-id="5772b-149">i4</span><span class="sxs-lookup"><span data-stu-id="5772b-149">i4</span></span>             | <span data-ttu-id="5772b-150">LONG</span><span class="sxs-lookup"><span data-stu-id="5772b-150">LONG</span></span>                      |
| <span data-ttu-id="5772b-151">v0</span><span class="sxs-lookup"><span data-stu-id="5772b-151">v0</span></span>             | <span data-ttu-id="5772b-152">OBJECT</span><span class="sxs-lookup"><span data-stu-id="5772b-152">OBJECT</span></span>                    |



 

<span data-ttu-id="5772b-153">Если буква не прописная, то инструкция SQL должна быть добавлена со значением NOT NULL.</span><span class="sxs-lookup"><span data-stu-id="5772b-153">If the letter is not capitalized, the SQL statement should be appended with NOT NULL.</span></span>



| <span data-ttu-id="5772b-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5772b-154">Returned value</span></span> | <span data-ttu-id="5772b-155">Синтаксис SQL</span><span class="sxs-lookup"><span data-stu-id="5772b-155">SQL syntax</span></span>        |
|----------------|-------------------|
| <span data-ttu-id="5772b-156">сна</span><span class="sxs-lookup"><span data-stu-id="5772b-156">s0</span></span>             | <span data-ttu-id="5772b-157">ЛОНГЧАР NOT NULL</span><span class="sxs-lookup"><span data-stu-id="5772b-157">LONGCHAR NOT NULL</span></span> |



 

<span data-ttu-id="5772b-158">Установщик не ограничивает длину столбцов на значение, заданное в формате определения столбца.</span><span class="sxs-lookup"><span data-stu-id="5772b-158">The installer does not internally limit the length of columns to the value specified by the column definition format.</span></span> <span data-ttu-id="5772b-159">Если данные, введенные в поле, превышают указанную длину столбца, пакет не проходит [проверку пакета](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="5772b-159">If the data entered into a field exceeds the specified column length, the package fails to pass [package validation](package-validation.md).</span></span> <span data-ttu-id="5772b-160">Чтобы пройти проверку в этом случае, необходимо изменить либо данные, либо схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="5772b-160">To pass validation in this case, either the data or the database schema must be changed.</span></span> <span data-ttu-id="5772b-161">Единственный способ изменить длину столбца стандартной таблицы — это экспортировать таблицу с помощью [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), отредактировать экспортированный файл IDT, а затем импортировать таблицу с помощью [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="5772b-161">The only means to change the column length of a standard table is by exporting the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editing the exported .idt file, and then importing the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="5772b-162">Авторы не могут изменять типы данных столбцов, допустимость значений NULL или атрибуты локализации любых столбцов в стандартных таблицах.</span><span class="sxs-lookup"><span data-stu-id="5772b-162">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="5772b-163">Авторы могут создавать пользовательские таблицы со столбцами, имеющими атрибуты столбцов.</span><span class="sxs-lookup"><span data-stu-id="5772b-163">Authors can create custom tables with columns having any column attributes.</span></span>

<span data-ttu-id="5772b-164">При использовании [**мсидатабасемерже**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) для слияния эталонной базы данных в целевую базу данных имена столбцов, число первичных ключей и типы данных столбцов должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="5772b-164">When using [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to merge a reference database into a target database, the column names, number of primary keys, and column data types must match.</span></span> <span data-ttu-id="5772b-165">**Мсидатабасемерже** игнорирует атрибуты локализации и длины столбцов.</span><span class="sxs-lookup"><span data-stu-id="5772b-165">**MsiDatabaseMerge** ignores the localization and column length attributes.</span></span> <span data-ttu-id="5772b-166">Если столбец в базе данных-образце имеет длину 0 или больше, чем длина этого столбца в целевой базе данных, **мсидатабасемерже** увеличивает длину столбца в целевой базе данных до длины в базе данных-образце.</span><span class="sxs-lookup"><span data-stu-id="5772b-166">If a column in the reference database has a length that is 0 or greater than the that column's length in the target database, **MsiDatabaseMerge** increases the column length in the target database to the length in the reference database.</span></span>

<span data-ttu-id="5772b-167">При использовании Mergmod.dll версии 2,0 приложение модуля слияния в MSI-файл никогда не изменяет длину столбцов или типы столбцов существующей таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="5772b-167">When using Mergmod.dll version 2.0, the application of a merge module to a .msi file never changes the length of columns or the column types of an existing database table.</span></span> <span data-ttu-id="5772b-168">Однако приложение модуля слияния может изменить схему существующей таблицы базы данных, если модуль добавляет новые столбцы в таблицу, для которой допускается добавление столбцов.</span><span class="sxs-lookup"><span data-stu-id="5772b-168">The application of a merge module can however change the schema of an existing database table if the module adds new columns to a table for which it is valid to add columns.</span></span> <span data-ttu-id="5772b-169">При использовании Mergemod.dll версии, меньшей версии 2,0, приложение модуля слияния никогда не изменяет длину столбцов и никогда не изменяет схему целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="5772b-169">When using a Mergemod.dll version less than version 2.0, the application of a merge module never changes the length of columns and never changes the schema of the target database.</span></span>

 

 



