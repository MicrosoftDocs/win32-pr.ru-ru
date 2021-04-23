---
description: Текстовый файл архива для установщик Windows базы данных содержит расширение IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Формат файла архива
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909088"
---
# <a name="archive-file-format"></a><span data-ttu-id="eee67-103">Формат файла архива</span><span class="sxs-lookup"><span data-stu-id="eee67-103">Archive File Format</span></span>

<span data-ttu-id="eee67-104">[Текстовый файл архива](text-archive-files.md) для установщик Windows базы данных содержит расширение IDT.</span><span class="sxs-lookup"><span data-stu-id="eee67-104">A [text archive file](text-archive-files.md) for a Windows Installer database carries an .idt file name extension.</span></span> <span data-ttu-id="eee67-105">При экспорте всей базы данных в архивные файлы каждая таблица в базе данных имеет отдельный файл IDT.</span><span class="sxs-lookup"><span data-stu-id="eee67-105">When an entire database is exported to archive files, each table in the database has a separate .idt file.</span></span> <span data-ttu-id="eee67-106">Если таблица содержит столбец потока, каждый поток в таблице представляется файлом с расширением имени файла ИБД.</span><span class="sxs-lookup"><span data-stu-id="eee67-106">If a table contains a stream column, each stream in the table is represented by a file with an .ibd file name extension.</span></span> <span data-ttu-id="eee67-107">ИБД-файлы хранятся в папке с тем же именем, что и таблица.</span><span class="sxs-lookup"><span data-stu-id="eee67-107">The .ibd files are stored in a folder with the same name as the table.</span></span>

## <a name="idt-file-format"></a><span data-ttu-id="eee67-108">Формат файла IDT</span><span class="sxs-lookup"><span data-stu-id="eee67-108">.idt File Format</span></span>

<span data-ttu-id="eee67-109">Файл IDT экспортированной таблицы базы данных, содержащий только символы ASCII, имеет следующий базовый формат.</span><span class="sxs-lookup"><span data-stu-id="eee67-109">The .idt file of an exported database table that contains only ASCII characters has the following basic format.</span></span>

-   <span data-ttu-id="eee67-110">Первая строка содержит имена столбцов таблицы, разделенные символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="eee67-110">The first row contains the table column names separated by tabs.</span></span>
-   <span data-ttu-id="eee67-111">Вторая строка содержит определения столбцов, разделенные символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="eee67-111">The second row contains the column definitions separated by tabs.</span></span>
-   <span data-ttu-id="eee67-112">Если файл содержит только ASCII-данные, третья строка имеет имя таблицы и имена первичных ключевых столбцов, разделенные символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="eee67-112">If the file contain only ASCII data, the third row is table name and primary key column names separated by tabs.</span></span>
-   <span data-ttu-id="eee67-113">Остальные строки в файле представляют собой строки в таблице со столбцами, разделенными символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="eee67-113">The remaining rows in the file represent rows in the table, with columns separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="eee67-114">Если файл содержит данные, отличные от ASCII, третья строка представляет собой числовую кодовую страницу, за которой следуют имя таблицы и имена первичных ключевых столбцов, разделенные символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="eee67-114">If the file contains non-ASCII data, the third row is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span> <span data-ttu-id="eee67-115">Файл IDT, содержащий сведения, не относящиеся к ASCII, должен сохраняться в формате ASCII.</span><span class="sxs-lookup"><span data-stu-id="eee67-115">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="eee67-116">Например, текстовый файл архива может содержать имена столбцов и таблиц в кодировке UTF-8, но сам файл архива должен быть ASCII.</span><span class="sxs-lookup"><span data-stu-id="eee67-116">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span> <span data-ttu-id="eee67-117">См. раздел [данные ASCII в текстовых файлах архива](ascii-data-in-text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="eee67-117">See the section [ASCII Data in Text Archive Files](ascii-data-in-text-archive-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="eee67-118">В специальных файлах [ \_ форцекодепаже](-forcecodepage.md) и [ \_ SummaryInformation](-summaryinformation.md) . IDT используются расширенные форматы.</span><span class="sxs-lookup"><span data-stu-id="eee67-118">The special [\_ForceCodepage](-forcecodepage.md) and [\_SummaryInformation](-summaryinformation.md) .idt files use extended formats.</span></span> <span data-ttu-id="eee67-119">\_ \_ Описание их форматов см. в разделах форцекодепаже и SummaryInformation.</span><span class="sxs-lookup"><span data-stu-id="eee67-119">See the \_ForceCodepage and \_SummaryInformation sections for descriptions of their formats.</span></span>

 

## <a name="column-definitions"></a><span data-ttu-id="eee67-120">Определения столбцов</span><span class="sxs-lookup"><span data-stu-id="eee67-120">Column Definitions</span></span>

<span data-ttu-id="eee67-121">Определения столбцов обозначаются символами.</span><span class="sxs-lookup"><span data-stu-id="eee67-121">Column definitions are indicated by characters.</span></span>

-   <span data-ttu-id="eee67-122">Первый символ обозначает тип столбца.</span><span class="sxs-lookup"><span data-stu-id="eee67-122">The first character indicates the column type.</span></span> <span data-ttu-id="eee67-123">Строчная буква указывает на столбец, не допускающий значения NULL, а буква в верхнем регистре указывает, что столбец может содержать значения NULL.</span><span class="sxs-lookup"><span data-stu-id="eee67-123">A lowercase letter indicates a non-nullable column and an uppercase letter indicates that the column can contain null values.</span></span>

    | <span data-ttu-id="eee67-124">Знак</span><span class="sxs-lookup"><span data-stu-id="eee67-124">Character</span></span> | <span data-ttu-id="eee67-125">Значение</span><span class="sxs-lookup"><span data-stu-id="eee67-125">Meaning</span></span>                   |
    |-----------|---------------------------|
    | <span data-ttu-id="eee67-126">s, S</span><span class="sxs-lookup"><span data-stu-id="eee67-126">s, S</span></span>      | <span data-ttu-id="eee67-127">Строковый столбец</span><span class="sxs-lookup"><span data-stu-id="eee67-127">String Column</span></span>             |
    | <span data-ttu-id="eee67-128">l, L</span><span class="sxs-lookup"><span data-stu-id="eee67-128">l, L</span></span>      | <span data-ttu-id="eee67-129">Локализуемый строковый столбец</span><span class="sxs-lookup"><span data-stu-id="eee67-129">Localizable String Column</span></span> |
    | <span data-ttu-id="eee67-130">v, V</span><span class="sxs-lookup"><span data-stu-id="eee67-130">v, V</span></span>      | <span data-ttu-id="eee67-131">Двоичный столбец</span><span class="sxs-lookup"><span data-stu-id="eee67-131">Binary Column</span></span>             |
    | <span data-ttu-id="eee67-132">я, я</span><span class="sxs-lookup"><span data-stu-id="eee67-132">i, I</span></span>      | <span data-ttu-id="eee67-133">Целочисленный столбец</span><span class="sxs-lookup"><span data-stu-id="eee67-133">Integer Column</span></span>            |

    

     

-   <span data-ttu-id="eee67-134">Второй символ указывает размер данных столбца.</span><span class="sxs-lookup"><span data-stu-id="eee67-134">The second character indicates the column data size.</span></span>

    > [!Note]  
    > <span data-ttu-id="eee67-135">Установщик Windows на самом деле не использует указанный размер столбца, чтобы ограничить размер строки, которую можно указать в поле строкового столбца.</span><span class="sxs-lookup"><span data-stu-id="eee67-135">The Windows Installer does not actually use the specified column size to limit the size of the string that can be entered into a string column field.</span></span> <span data-ttu-id="eee67-136">Однако некоторые средства разработки используют указанный размер столбца, чтобы ограничить размер допустимой строки.</span><span class="sxs-lookup"><span data-stu-id="eee67-136">However, some authoring tools do use the specified column size to limit the size of a valid string.</span></span> <span data-ttu-id="eee67-137">Рекомендуется, чтобы строки, введенные в любой столбец, соответствовали указанному требованию к размеру.</span><span class="sxs-lookup"><span data-stu-id="eee67-137">It is recommended that strings entered into any column meet the specified size requirement.</span></span>

     

    

    | <span data-ttu-id="eee67-138">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="eee67-138">Column Definition</span></span> | <span data-ttu-id="eee67-139">Значение</span><span class="sxs-lookup"><span data-stu-id="eee67-139">Meaning</span></span>                                    |
    |-------------------|--------------------------------------------|
    | <span data-ttu-id="eee67-140">s255</span><span class="sxs-lookup"><span data-stu-id="eee67-140">s255</span></span>              | <span data-ttu-id="eee67-141">Столбец строк 255, не допускающий значения NULL</span><span class="sxs-lookup"><span data-stu-id="eee67-141">Non-Nullable String Column 255 long</span></span>        |
    | <span data-ttu-id="eee67-142">L50</span><span class="sxs-lookup"><span data-stu-id="eee67-142">L50</span></span>               | <span data-ttu-id="eee67-143">Столбец локализуемых строк, допускающий значения NULL, длинный 50</span><span class="sxs-lookup"><span data-stu-id="eee67-143">Nullable Localizable String Column 50 long</span></span> |
    | <span data-ttu-id="eee67-144">I2, I2</span><span class="sxs-lookup"><span data-stu-id="eee67-144">i2, I2</span></span>            | <span data-ttu-id="eee67-145">Столбец коротких целых чисел</span><span class="sxs-lookup"><span data-stu-id="eee67-145">Short Integer Column</span></span>                       |
    | <span data-ttu-id="eee67-146">I4, I4</span><span class="sxs-lookup"><span data-stu-id="eee67-146">i4, I4</span></span>            | <span data-ttu-id="eee67-147">Столбец длинных целых чисел</span><span class="sxs-lookup"><span data-stu-id="eee67-147">Long Integer Column</span></span>                        |

    

     

## <a name="control-character-translation"></a><span data-ttu-id="eee67-148">Управление преобразованием символов</span><span class="sxs-lookup"><span data-stu-id="eee67-148">Control Character Translation</span></span>

<span data-ttu-id="eee67-149">При экспорте таблицы в текстовый файл архива преобразуются управляющие символы, чтобы избежать конфликтов с разделителями файлов.</span><span class="sxs-lookup"><span data-stu-id="eee67-149">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span> <span data-ttu-id="eee67-150">При записи в файл. IDT управляющие символы преобразуются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="eee67-150">While writing into the .idt file, the control characters are translated as follows.</span></span>



| <span data-ttu-id="eee67-151">Управляющий символ</span><span class="sxs-lookup"><span data-stu-id="eee67-151">Control Character</span></span> | <span data-ttu-id="eee67-152">Преобразование в. IDT</span><span class="sxs-lookup"><span data-stu-id="eee67-152">Translation in .idt</span></span> | <span data-ttu-id="eee67-153">Значение</span><span class="sxs-lookup"><span data-stu-id="eee67-153">Meaning</span></span>         |
|-------------------|---------------------|-----------------|
| <span data-ttu-id="eee67-154">NULL</span><span class="sxs-lookup"><span data-stu-id="eee67-154">NULL</span></span>              | <span data-ttu-id="eee67-155">21</span><span class="sxs-lookup"><span data-stu-id="eee67-155">21</span></span>                  | <span data-ttu-id="eee67-156">NULL</span><span class="sxs-lookup"><span data-stu-id="eee67-156">Null</span></span>            |
| <span data-ttu-id="eee67-157">BS</span><span class="sxs-lookup"><span data-stu-id="eee67-157">BS</span></span>                | <span data-ttu-id="eee67-158">27</span><span class="sxs-lookup"><span data-stu-id="eee67-158">27</span></span>                  | <span data-ttu-id="eee67-159">Резервное пространство</span><span class="sxs-lookup"><span data-stu-id="eee67-159">Back Space</span></span>      |
| <span data-ttu-id="eee67-160">HT</span><span class="sxs-lookup"><span data-stu-id="eee67-160">HT</span></span>                | <span data-ttu-id="eee67-161">16</span><span class="sxs-lookup"><span data-stu-id="eee67-161">16</span></span>                  | <span data-ttu-id="eee67-162">Вкладка</span><span class="sxs-lookup"><span data-stu-id="eee67-162">Tab</span></span>             |
| <span data-ttu-id="eee67-163">ВОЗВРАТА</span><span class="sxs-lookup"><span data-stu-id="eee67-163">LF</span></span>                | <span data-ttu-id="eee67-164">25</span><span class="sxs-lookup"><span data-stu-id="eee67-164">25</span></span>                  | <span data-ttu-id="eee67-165">Перевод строки</span><span class="sxs-lookup"><span data-stu-id="eee67-165">Line Feed</span></span>       |
| <span data-ttu-id="eee67-166">FF</span><span class="sxs-lookup"><span data-stu-id="eee67-166">FF</span></span>                | <span data-ttu-id="eee67-167">24</span><span class="sxs-lookup"><span data-stu-id="eee67-167">24</span></span>                  | <span data-ttu-id="eee67-168">Веб-канал формы</span><span class="sxs-lookup"><span data-stu-id="eee67-168">Form Feed</span></span>       |
| <span data-ttu-id="eee67-169">CR</span><span class="sxs-lookup"><span data-stu-id="eee67-169">CR</span></span>                | <span data-ttu-id="eee67-170">17</span><span class="sxs-lookup"><span data-stu-id="eee67-170">17</span></span>                  | <span data-ttu-id="eee67-171">Возврат каретки</span><span class="sxs-lookup"><span data-stu-id="eee67-171">Carriage Return</span></span> |



 

 

 



