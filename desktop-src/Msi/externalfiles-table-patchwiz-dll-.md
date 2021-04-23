---
description: Таблица Екстерналфилес содержит сведения о конкретных файлах, которые не являются частью обычного целевого образа.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Таблица Екстерналфилес (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544287"
---
# <a name="externalfiles-table-patchwizdll"></a><span data-ttu-id="53cdb-103">Таблица Екстерналфилес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="53cdb-103">ExternalFiles Table (Patchwiz.dll)</span></span>

<span data-ttu-id="53cdb-104">Таблица Екстерналфилес содержит сведения о конкретных файлах, которые не являются частью обычного целевого образа.</span><span class="sxs-lookup"><span data-stu-id="53cdb-104">The ExternalFiles table contains information about specific files that are not part of a regular target image.</span></span> <span data-ttu-id="53cdb-105">Эти файлы могут существовать в продуктах, которые были обновлены другим продуктом, обновлением или исправлением.</span><span class="sxs-lookup"><span data-stu-id="53cdb-105">These files may exist in products that have been updated by another product, upgrade, or patch.</span></span> <span data-ttu-id="53cdb-106">Эта таблица является необязательной в базе данных создания исправлений (файл PCP) и используется функцией [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="53cdb-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="53cdb-107">Таблица Екстерналфилес содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="53cdb-107">The ExternalFiles table has the following columns.</span></span>



| <span data-ttu-id="53cdb-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="53cdb-108">Column</span></span>        | <span data-ttu-id="53cdb-109">Type</span><span class="sxs-lookup"><span data-stu-id="53cdb-109">Type</span></span>    | <span data-ttu-id="53cdb-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="53cdb-110">Key</span></span> | <span data-ttu-id="53cdb-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="53cdb-111">Nullable</span></span> |
|---------------|---------|-----|----------|
| <span data-ttu-id="53cdb-112">Семейство</span><span class="sxs-lookup"><span data-stu-id="53cdb-112">Family</span></span>        | <span data-ttu-id="53cdb-113">text</span><span class="sxs-lookup"><span data-stu-id="53cdb-113">text</span></span>    | <span data-ttu-id="53cdb-114">Да</span><span class="sxs-lookup"><span data-stu-id="53cdb-114">Y</span></span>   | <span data-ttu-id="53cdb-115">Нет</span><span class="sxs-lookup"><span data-stu-id="53cdb-115">N</span></span>        |
| <span data-ttu-id="53cdb-116">фтк</span><span class="sxs-lookup"><span data-stu-id="53cdb-116">FTK</span></span>           | <span data-ttu-id="53cdb-117">text</span><span class="sxs-lookup"><span data-stu-id="53cdb-117">text</span></span>    | <span data-ttu-id="53cdb-118">Да</span><span class="sxs-lookup"><span data-stu-id="53cdb-118">Y</span></span>   | <span data-ttu-id="53cdb-119">Нет</span><span class="sxs-lookup"><span data-stu-id="53cdb-119">N</span></span>        |
| <span data-ttu-id="53cdb-120">FilePath</span><span class="sxs-lookup"><span data-stu-id="53cdb-120">FilePath</span></span>      | <span data-ttu-id="53cdb-121">text</span><span class="sxs-lookup"><span data-stu-id="53cdb-121">text</span></span>    | <span data-ttu-id="53cdb-122">Да</span><span class="sxs-lookup"><span data-stu-id="53cdb-122">Y</span></span>   | <span data-ttu-id="53cdb-123">Нет</span><span class="sxs-lookup"><span data-stu-id="53cdb-123">N</span></span>        |
| <span data-ttu-id="53cdb-124">симболпасс</span><span class="sxs-lookup"><span data-stu-id="53cdb-124">SymbolPaths</span></span>   | <span data-ttu-id="53cdb-125">text</span><span class="sxs-lookup"><span data-stu-id="53cdb-125">text</span></span>    |     | <span data-ttu-id="53cdb-126">Да</span><span class="sxs-lookup"><span data-stu-id="53cdb-126">Y</span></span>        |
| <span data-ttu-id="53cdb-127">игнореоффсетс</span><span class="sxs-lookup"><span data-stu-id="53cdb-127">IgnoreOffsets</span></span> | <span data-ttu-id="53cdb-128">text</span><span class="sxs-lookup"><span data-stu-id="53cdb-128">text</span></span>    |     | <span data-ttu-id="53cdb-129">Да</span><span class="sxs-lookup"><span data-stu-id="53cdb-129">Y</span></span>        |
| <span data-ttu-id="53cdb-130">игнореленгсс</span><span class="sxs-lookup"><span data-stu-id="53cdb-130">IgnoreLengths</span></span> | <span data-ttu-id="53cdb-131">text</span><span class="sxs-lookup"><span data-stu-id="53cdb-131">text</span></span>    |     | <span data-ttu-id="53cdb-132">Да</span><span class="sxs-lookup"><span data-stu-id="53cdb-132">Y</span></span>        |
| <span data-ttu-id="53cdb-133">ретаиноффсетс</span><span class="sxs-lookup"><span data-stu-id="53cdb-133">RetainOffsets</span></span> | <span data-ttu-id="53cdb-134">text</span><span class="sxs-lookup"><span data-stu-id="53cdb-134">text</span></span>    |     | <span data-ttu-id="53cdb-135">Нет</span><span class="sxs-lookup"><span data-stu-id="53cdb-135">N</span></span>        |
| <span data-ttu-id="53cdb-136">Заказ</span><span class="sxs-lookup"><span data-stu-id="53cdb-136">Order</span></span>         | <span data-ttu-id="53cdb-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="53cdb-137">integer</span></span> |     | <span data-ttu-id="53cdb-138">Да</span><span class="sxs-lookup"><span data-stu-id="53cdb-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="53cdb-139">Столбцы</span><span class="sxs-lookup"><span data-stu-id="53cdb-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="53cdb-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Семьи</span><span class="sxs-lookup"><span data-stu-id="53cdb-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="53cdb-141">Внешний ключ к столбцу Family [таблицы имажефамилиес (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="53cdb-141">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="53cdb-142"><span id="FTK"></span><span id="ftk"></span>фтк</span><span class="sxs-lookup"><span data-stu-id="53cdb-142"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="53cdb-143">Внешний ключ в [таблицу File](file-table.md) файла MSI обновленного образа.</span><span class="sxs-lookup"><span data-stu-id="53cdb-143">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="53cdb-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>Равно</span><span class="sxs-lookup"><span data-stu-id="53cdb-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span></span>
</dt> <dd>

<span data-ttu-id="53cdb-145">Полный путь к внешнему файлу, включая имя файла.</span><span class="sxs-lookup"><span data-stu-id="53cdb-145">Full path of the external file including the file name.</span></span> <span data-ttu-id="53cdb-146">Поле FilePath используется для нахождение файла, указанного в столбце ФТК.</span><span class="sxs-lookup"><span data-stu-id="53cdb-146">FilePath field is used to locate the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="53cdb-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>симболпасс</span><span class="sxs-lookup"><span data-stu-id="53cdb-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="53cdb-148">Полный путь поиска файлов символов файла, указанного в столбце ФТК.</span><span class="sxs-lookup"><span data-stu-id="53cdb-148">Full path searched for symbol files of the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="53cdb-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>игнореоффсетс</span><span class="sxs-lookup"><span data-stu-id="53cdb-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="53cdb-150">Значение в этом поле представляет собой разделенный запятыми список номеров смещений диапазона для диапазонов, которые будут игнорироваться во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="53cdb-150">The value in this field is a comma-delimited list of range offset numbers for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="53cdb-151">Порядок и количество диапазонов в списке должны соответствовать элементам в столбце Игнореленгсс.</span><span class="sxs-lookup"><span data-stu-id="53cdb-151">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="53cdb-152">Этот столбец является необязательным.</span><span class="sxs-lookup"><span data-stu-id="53cdb-152">This column is optional.</span></span>

<span data-ttu-id="53cdb-153">Значения могут быть десятичными или шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="53cdb-153">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="53cdb-154">[Patchwiz.dll](patchwiz-dll.md) считает значение шестнадцатеричным, если оно имеет префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="53cdb-154">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="53cdb-155">Столбцы являются строковыми столбцами, а Patchwiz.dll преобразовывают значения в ULONG.</span><span class="sxs-lookup"><span data-stu-id="53cdb-155">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="53cdb-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>игнореленгсс</span><span class="sxs-lookup"><span data-stu-id="53cdb-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="53cdb-157">Значение в этом поле представляет собой разделенный запятыми список длин диапазонов в байтах, в течение которых диапазоны пропускаются во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="53cdb-157">The value in this field is a comma-delimited list of range lengths in bytes for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="53cdb-158">Порядок и количество диапазонов в списке должны соответствовать элементам в столбце Игнореоффсетс.</span><span class="sxs-lookup"><span data-stu-id="53cdb-158">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="53cdb-159">Этот столбец является необязательным.</span><span class="sxs-lookup"><span data-stu-id="53cdb-159">This column is optional.</span></span>

<span data-ttu-id="53cdb-160">Значения могут быть десятичными или шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="53cdb-160">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="53cdb-161">[Patchwiz.dll](patchwiz-dll.md) считает значение шестнадцатеричным, если оно имеет префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="53cdb-161">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="53cdb-162">Столбцы являются строковыми столбцами, а Patchwiz.dll преобразовывают значения в ULONG.</span><span class="sxs-lookup"><span data-stu-id="53cdb-162">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="53cdb-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>ретаиноффсетс</span><span class="sxs-lookup"><span data-stu-id="53cdb-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="53cdb-164">Значение в этом поле представляет собой разделенный запятыми список номеров смещений диапазона для диапазонов, которые должны храниться во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="53cdb-164">The value in this field is a comma-delimited list of range offset numbers for the ranges to be retained in the External file.</span></span> <span data-ttu-id="53cdb-165">Порядок и количество диапазонов в списке должны совпадать с элементами в столбце Ретаиноффсетс соответствующей записи в [таблице фамилифилеранжес (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="53cdb-165">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span></span>

<span data-ttu-id="53cdb-166">Значения могут быть десятичными или шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="53cdb-166">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="53cdb-167">[Patchwiz.dll](patchwiz-dll.md) считает значение шестнадцатеричным, если оно имеет префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="53cdb-167">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="53cdb-168">Столбцы являются строковыми столбцами, а Patchwiz.dll преобразовывают значения в ULONG.</span><span class="sxs-lookup"><span data-stu-id="53cdb-168">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="53cdb-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Порядок</span><span class="sxs-lookup"><span data-stu-id="53cdb-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="53cdb-170">Если для одного и того же внешнего файла указаны две или более версии, таблица может содержать несколько записей с совпадающими значениями в полях ФТК и Family.</span><span class="sxs-lookup"><span data-stu-id="53cdb-170">If two or more versions are specified for the same external file, the table may contain multiple records with matching values in the FTK and Family fields.</span></span> <span data-ttu-id="53cdb-171">В этом случае в поле порядок можно указать порядок внешних файлов, которые будут использоваться при создании исправления.</span><span class="sxs-lookup"><span data-stu-id="53cdb-171">In this case, the Order field may specify the order of external files to use when creating the patch.</span></span> <span data-ttu-id="53cdb-172">Порядок от самой старой до самой последней версии.</span><span class="sxs-lookup"><span data-stu-id="53cdb-172">The order is from the oldest to the most recent version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53cdb-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53cdb-173">Remarks</span></span>

<span data-ttu-id="53cdb-174">Эта таблица принимает переменные среды в виде путей, начинающихся с Patchwiz.dll версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="53cdb-174">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53cdb-175">См. также</span><span class="sxs-lookup"><span data-stu-id="53cdb-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53cdb-176">Исправление выбранных регионов файла</span><span class="sxs-lookup"><span data-stu-id="53cdb-176">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



