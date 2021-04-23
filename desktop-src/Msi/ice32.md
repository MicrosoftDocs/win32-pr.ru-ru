---
description: ICE32 проверяет, что ключи и внешние ключи в файле MSI имеют одинаковые типы определения размера и столбца.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663662"
---
# <a name="ice32"></a><span data-ttu-id="8ba35-103">ICE32</span><span class="sxs-lookup"><span data-stu-id="8ba35-103">ICE32</span></span>

<span data-ttu-id="8ba35-104">ICE32 проверяет, что ключи и внешние ключи в файле MSI имеют одинаковые типы определения размера и столбца.</span><span class="sxs-lookup"><span data-stu-id="8ba35-104">ICE32 validates that keys and foreign keys in the .msi file are of the same size and column definition types.</span></span> <span data-ttu-id="8ba35-105">Это настраиваемое действие ICE выполняет сравнение с помощью [ \_ таблицы проверки](-validation-table.md) и использует типы определений, возвращаемые функцией [**мсивиевжетколумнинфо**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span><span class="sxs-lookup"><span data-stu-id="8ba35-105">This ICE custom action makes the comparison using the [\_Validation table](-validation-table.md) and using the definition types that are returned by [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span></span> <span data-ttu-id="8ba35-106">Дополнительные сведения см. в разделе [Формат определения столбца](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="8ba35-106">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

## <a name="result"></a><span data-ttu-id="8ba35-107">Результат</span><span class="sxs-lookup"><span data-stu-id="8ba35-107">Result</span></span>

<span data-ttu-id="8ba35-108">ICE32 отправляет ошибки, если MSI-файл содержит внешние ключи для ключей другой длины столбца или типа данных столбца.</span><span class="sxs-lookup"><span data-stu-id="8ba35-108">ICE32 posts errors if the .msi file contains any foreign keys to keys of a different column length or column data type.</span></span>

## <a name="example"></a><span data-ttu-id="8ba35-109">Пример</span><span class="sxs-lookup"><span data-stu-id="8ba35-109">Example</span></span>

<span data-ttu-id="8ba35-110">ICE32 размещает две ошибки в приведенном примере:</span><span class="sxs-lookup"><span data-stu-id="8ba35-110">ICE32 posts two errors for the example shown:</span></span>

-   <span data-ttu-id="8ba35-111">Определен внешний ключ и ключ, которые имеют разный размер.</span><span class="sxs-lookup"><span data-stu-id="8ba35-111">There is a foreign key and key defined that differ in size.</span></span>
-   <span data-ttu-id="8ba35-112">Определен внешний ключ и ключ, которые различаются по типу их определения.</span><span class="sxs-lookup"><span data-stu-id="8ba35-112">There is a foreign key and key defined that differ in their definition type.</span></span>

<span data-ttu-id="8ba35-113">[ \_ Таблица проверки](-validation-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="8ba35-113">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="8ba35-114">Таблица</span><span class="sxs-lookup"><span data-stu-id="8ba35-114">Table</span></span> | <span data-ttu-id="8ba35-115">Столбец</span><span class="sxs-lookup"><span data-stu-id="8ba35-115">Column</span></span>  | <span data-ttu-id="8ba35-116">кэйтабле</span><span class="sxs-lookup"><span data-stu-id="8ba35-116">KeyTable</span></span> | <span data-ttu-id="8ba35-117">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="8ba35-117">KeyColumn</span></span> |
|-------|---------|----------|-----------|
| <span data-ttu-id="8ba35-118">Файл</span><span class="sxs-lookup"><span data-stu-id="8ba35-118">File</span></span>  | <span data-ttu-id="8ba35-119">Версия</span><span class="sxs-lookup"><span data-stu-id="8ba35-119">Version</span></span> | <span data-ttu-id="8ba35-120">Файл</span><span class="sxs-lookup"><span data-stu-id="8ba35-120">File</span></span>     | <span data-ttu-id="8ba35-121">1</span><span class="sxs-lookup"><span data-stu-id="8ba35-121">1</span></span>         |
| <span data-ttu-id="8ba35-122">Колыханий</span><span class="sxs-lookup"><span data-stu-id="8ba35-122">Flap</span></span>  | <span data-ttu-id="8ba35-123">Column8</span><span class="sxs-lookup"><span data-stu-id="8ba35-123">Column8</span></span> | <span data-ttu-id="8ba35-124">Колыханий</span><span class="sxs-lookup"><span data-stu-id="8ba35-124">Flap</span></span>     | <span data-ttu-id="8ba35-125">1</span><span class="sxs-lookup"><span data-stu-id="8ba35-125">1</span></span>         |



 

<span data-ttu-id="8ba35-126">Определения столбцов (частично)</span><span class="sxs-lookup"><span data-stu-id="8ba35-126">Column Definitions (partial)</span></span>



| <span data-ttu-id="8ba35-127">Таблица</span><span class="sxs-lookup"><span data-stu-id="8ba35-127">Table</span></span> | <span data-ttu-id="8ba35-128">Столбец</span><span class="sxs-lookup"><span data-stu-id="8ba35-128">Column</span></span>  | <span data-ttu-id="8ba35-129">Тип</span><span class="sxs-lookup"><span data-stu-id="8ba35-129">Type</span></span> | <span data-ttu-id="8ba35-130">Размер</span><span class="sxs-lookup"><span data-stu-id="8ba35-130">Size</span></span> |
|-------|---------|------|------|
| <span data-ttu-id="8ba35-131">Файл</span><span class="sxs-lookup"><span data-stu-id="8ba35-131">File</span></span>  | <span data-ttu-id="8ba35-132">Файл</span><span class="sxs-lookup"><span data-stu-id="8ba35-132">File</span></span>    | <span data-ttu-id="8ba35-133">s</span><span class="sxs-lookup"><span data-stu-id="8ba35-133">s</span></span>    | <span data-ttu-id="8ba35-134">72</span><span class="sxs-lookup"><span data-stu-id="8ba35-134">72</span></span>   |
| <span data-ttu-id="8ba35-135">Файл</span><span class="sxs-lookup"><span data-stu-id="8ba35-135">File</span></span>  | <span data-ttu-id="8ba35-136">Версия</span><span class="sxs-lookup"><span data-stu-id="8ba35-136">Version</span></span> | <span data-ttu-id="8ba35-137">S</span><span class="sxs-lookup"><span data-stu-id="8ba35-137">S</span></span>    | <span data-ttu-id="8ba35-138">32</span><span class="sxs-lookup"><span data-stu-id="8ba35-138">32</span></span>   |
| <span data-ttu-id="8ba35-139">Колыханий</span><span class="sxs-lookup"><span data-stu-id="8ba35-139">Flap</span></span>  | <span data-ttu-id="8ba35-140">Column1</span><span class="sxs-lookup"><span data-stu-id="8ba35-140">Column1</span></span> | <span data-ttu-id="8ba35-141">i</span><span class="sxs-lookup"><span data-stu-id="8ba35-141">i</span></span>    | <span data-ttu-id="8ba35-142">2</span><span class="sxs-lookup"><span data-stu-id="8ba35-142">2</span></span>    |
| <span data-ttu-id="8ba35-143">Колыханий</span><span class="sxs-lookup"><span data-stu-id="8ba35-143">Flap</span></span>  | <span data-ttu-id="8ba35-144">Column8</span><span class="sxs-lookup"><span data-stu-id="8ba35-144">Column8</span></span> | <span data-ttu-id="8ba35-145">S</span><span class="sxs-lookup"><span data-stu-id="8ba35-145">S</span></span>    | <span data-ttu-id="8ba35-146">32</span><span class="sxs-lookup"><span data-stu-id="8ba35-146">32</span></span>   |



 

<span data-ttu-id="8ba35-147">Столбец Version таблицы File может быть внешним ключом к другому файлу в таблице File.</span><span class="sxs-lookup"><span data-stu-id="8ba35-147">The Version column of the File table can be a foreign key to another file in the File table.</span></span> <span data-ttu-id="8ba35-148">Это происходит с сопутствующими файлами.</span><span class="sxs-lookup"><span data-stu-id="8ba35-148">This occurs with companion files.</span></span> <span data-ttu-id="8ba35-149">Однако столбец Version допускает только строку 32, тогда как столбец File допускает строку длиной 72.</span><span class="sxs-lookup"><span data-stu-id="8ba35-149">However, the Version column only allows a string length 32, whereas the File column allows a string length 72.</span></span> <span data-ttu-id="8ba35-150">Чтобы устранить эту ошибку, измените значения длины строки на Match.</span><span class="sxs-lookup"><span data-stu-id="8ba35-150">To fix this error change the string lengths to match.</span></span>

<span data-ttu-id="8ba35-151">Определен внешний ключ и ключ, которые отличаются их типами определений.</span><span class="sxs-lookup"><span data-stu-id="8ba35-151">There is a foreign key and key defined that differ in their definition types.</span></span> <span data-ttu-id="8ba35-152">Column8 таблицы Колыханий указывается как внешний ключ для Столбец1.</span><span class="sxs-lookup"><span data-stu-id="8ba35-152">Column8 of the Flap Table is listed as a foreign key to Column1.</span></span> <span data-ttu-id="8ba35-153">Column8 — это строковый столбец, а Столбец1 — целочисленный столбец.</span><span class="sxs-lookup"><span data-stu-id="8ba35-153">Column8 is a string column and Column1 is an integer column.</span></span> <span data-ttu-id="8ba35-154">Необходимо определить внешний ключ и пары ключей, чтобы их типы данных совпадали.</span><span class="sxs-lookup"><span data-stu-id="8ba35-154">The foreign key and key pairs must be defined so that their data types match.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ba35-155">См. также</span><span class="sxs-lookup"><span data-stu-id="8ba35-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ba35-156">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="8ba35-156">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



