---
description: Таблица Таржетфилес \_ оптионалдата содержит сведения о конкретных файлах в целевом образе. Эта таблица является необязательной в базе данных создания исправлений (файл PCP) и используется функцией Уикреатепатчпаккажеекс.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: Таблица TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998908"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="a0f40-104">\_Таблица Оптионалдата таржетфилес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a0f40-104">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="a0f40-105">Таблица Таржетфилес \_ оптионалдата содержит сведения о конкретных файлах в целевом образе.</span><span class="sxs-lookup"><span data-stu-id="a0f40-105">The TargetFiles\_OptionalData table contains information about specific files in a target image.</span></span> <span data-ttu-id="a0f40-106">Эта таблица является необязательной в базе данных создания исправлений (файл PCP) и используется функцией [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f40-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="a0f40-107">Таблица Таржетфилес \_ оптионалдата содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="a0f40-107">The TargetFiles\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="a0f40-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="a0f40-108">Column</span></span>        | <span data-ttu-id="a0f40-109">Type</span><span class="sxs-lookup"><span data-stu-id="a0f40-109">Type</span></span> | <span data-ttu-id="a0f40-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="a0f40-110">Key</span></span> | <span data-ttu-id="a0f40-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="a0f40-111">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="a0f40-112">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="a0f40-112">Target</span></span>        | <span data-ttu-id="a0f40-113">text</span><span class="sxs-lookup"><span data-stu-id="a0f40-113">text</span></span> | <span data-ttu-id="a0f40-114">Да</span><span class="sxs-lookup"><span data-stu-id="a0f40-114">Y</span></span>   | <span data-ttu-id="a0f40-115">Нет</span><span class="sxs-lookup"><span data-stu-id="a0f40-115">N</span></span>        |
| <span data-ttu-id="a0f40-116">фтк</span><span class="sxs-lookup"><span data-stu-id="a0f40-116">FTK</span></span>           | <span data-ttu-id="a0f40-117">text</span><span class="sxs-lookup"><span data-stu-id="a0f40-117">text</span></span> | <span data-ttu-id="a0f40-118">Да</span><span class="sxs-lookup"><span data-stu-id="a0f40-118">Y</span></span>   | <span data-ttu-id="a0f40-119">Нет</span><span class="sxs-lookup"><span data-stu-id="a0f40-119">N</span></span>        |
| <span data-ttu-id="a0f40-120">симболпасс</span><span class="sxs-lookup"><span data-stu-id="a0f40-120">SymbolPaths</span></span>   | <span data-ttu-id="a0f40-121">text</span><span class="sxs-lookup"><span data-stu-id="a0f40-121">text</span></span> |     | <span data-ttu-id="a0f40-122">Да</span><span class="sxs-lookup"><span data-stu-id="a0f40-122">Y</span></span>        |
| <span data-ttu-id="a0f40-123">игнореоффсетс</span><span class="sxs-lookup"><span data-stu-id="a0f40-123">IgnoreOffsets</span></span> | <span data-ttu-id="a0f40-124">text</span><span class="sxs-lookup"><span data-stu-id="a0f40-124">text</span></span> |     | <span data-ttu-id="a0f40-125">Да</span><span class="sxs-lookup"><span data-stu-id="a0f40-125">Y</span></span>        |
| <span data-ttu-id="a0f40-126">игнореленгсс</span><span class="sxs-lookup"><span data-stu-id="a0f40-126">IgnoreLengths</span></span> | <span data-ttu-id="a0f40-127">text</span><span class="sxs-lookup"><span data-stu-id="a0f40-127">text</span></span> |     | <span data-ttu-id="a0f40-128">Да</span><span class="sxs-lookup"><span data-stu-id="a0f40-128">Y</span></span>        |
| <span data-ttu-id="a0f40-129">ретаиноффсетс</span><span class="sxs-lookup"><span data-stu-id="a0f40-129">RetainOffsets</span></span> | <span data-ttu-id="a0f40-130">text</span><span class="sxs-lookup"><span data-stu-id="a0f40-130">text</span></span> |     | <span data-ttu-id="a0f40-131">Да</span><span class="sxs-lookup"><span data-stu-id="a0f40-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a0f40-132">Столбцы</span><span class="sxs-lookup"><span data-stu-id="a0f40-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a0f40-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Мишень</span><span class="sxs-lookup"><span data-stu-id="a0f40-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="a0f40-134">Внешний ключ к целевому столбцу [таблицы таржетимажес (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="a0f40-134">Foreign key to the Target column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0f40-135"><span id="FTK"></span><span id="ftk"></span>фтк</span><span class="sxs-lookup"><span data-stu-id="a0f40-135"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="a0f40-136">Внешний ключ в [таблице файлов](file-table.md) целевого образа.</span><span class="sxs-lookup"><span data-stu-id="a0f40-136">Foreign key into the [File table](file-table.md) of target image.</span></span>

</dd> <dt>

<span data-ttu-id="a0f40-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>симболпасс</span><span class="sxs-lookup"><span data-stu-id="a0f40-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="a0f40-138">Значение в этом поле добавляется в список папок, разделенных точкой с запятой, в столбце Симболпасс [таблицы таржетимажес (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) при создании исправления и может использоваться для добавления файлов символов для определенного файла.</span><span class="sxs-lookup"><span data-stu-id="a0f40-138">The value in this field is added to the semicolon delimited list of folders in the SymbolPaths column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="a0f40-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>игнореоффсетс</span><span class="sxs-lookup"><span data-stu-id="a0f40-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="a0f40-140">Значение в этом поле представляет собой разделенный запятыми список номеров смещений диапазона для диапазонов, которые будут игнорироваться в целевом файле.</span><span class="sxs-lookup"><span data-stu-id="a0f40-140">The value in this field is a comma delimited list of range offset numbers for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="a0f40-141">Порядок и количество диапазонов в списке должны соответствовать элементам в столбце Игнореленгсс.</span><span class="sxs-lookup"><span data-stu-id="a0f40-141">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="a0f40-142">Этот столбец является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a0f40-142">This column is optional.</span></span>

<span data-ttu-id="a0f40-143">Значения могут быть десятичными или шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="a0f40-143">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="a0f40-144">[Patchwiz.dll](patchwiz-dll.md) считает значение шестнадцатеричным, если оно имеет префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="a0f40-144">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="a0f40-145">Столбцы являются строковыми столбцами, а Patchwiz.dll преобразовывают значения в ULONG.</span><span class="sxs-lookup"><span data-stu-id="a0f40-145">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="a0f40-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>игнореленгсс</span><span class="sxs-lookup"><span data-stu-id="a0f40-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="a0f40-147">Значение в этом поле представляет собой разделенный запятыми список длин диапазонов в байтах, в течение которых диапазоны пропускаются в целевом файле.</span><span class="sxs-lookup"><span data-stu-id="a0f40-147">The value in this field is a comma delimited list of range lengths in bytes for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="a0f40-148">Порядок и количество диапазонов в списке должны соответствовать элементам в столбце Игнореоффсетс.</span><span class="sxs-lookup"><span data-stu-id="a0f40-148">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="a0f40-149">Этот столбец является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a0f40-149">This column is optional.</span></span>

<span data-ttu-id="a0f40-150">Значения могут быть десятичными или шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="a0f40-150">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="a0f40-151">[Patchwiz.dll](patchwiz-dll.md) считает значение шестнадцатеричным, если оно имеет префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="a0f40-151">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="a0f40-152">Столбцы являются строковыми столбцами, а Patchwiz.dll преобразовывают значения в ULONG.</span><span class="sxs-lookup"><span data-stu-id="a0f40-152">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="a0f40-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>ретаиноффсетс</span><span class="sxs-lookup"><span data-stu-id="a0f40-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="a0f40-154">Значение в этом поле представляет собой разделенный запятыми список номеров смещений диапазона для диапазонов, которые должны храниться в целевом файле.</span><span class="sxs-lookup"><span data-stu-id="a0f40-154">The value in this field is a comma delimited list of range offset numbers for the ranges to be retained in the Target file.</span></span> <span data-ttu-id="a0f40-155">Порядок и количество диапазонов в списке должны совпадать с элементами в столбце Ретаиноффсетс соответствующей записи в [таблице фамилифилеранжес (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span><span class="sxs-lookup"><span data-stu-id="a0f40-155">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span></span>

<span data-ttu-id="a0f40-156">Значения могут быть десятичными или шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="a0f40-156">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="a0f40-157">[Patchwiz.dll](patchwiz-dll.md) считает значение шестнадцатеричным, если оно имеет префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="a0f40-157">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="a0f40-158">Столбцы являются строковыми столбцами, а Patchwiz.dll преобразовывают значения в ULONG.</span><span class="sxs-lookup"><span data-stu-id="a0f40-158">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a0f40-159">См. также</span><span class="sxs-lookup"><span data-stu-id="a0f40-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f40-160">Исправление выбранных регионов файла</span><span class="sxs-lookup"><span data-stu-id="a0f40-160">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



