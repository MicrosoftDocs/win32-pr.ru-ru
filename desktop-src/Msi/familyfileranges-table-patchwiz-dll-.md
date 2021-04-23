---
description: Таблица Фамилифилеранжес содержит сведения о конкретных файлах обновленного образа с диапазонами, которые никогда не должны перезаписываться.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Таблица Фамилифилеранжес (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155523"
---
# <a name="familyfileranges-table-patchwizdll"></a><span data-ttu-id="72604-103">Таблица Фамилифилеранжес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="72604-103">FamilyFileRanges Table (Patchwiz.dll)</span></span>

<span data-ttu-id="72604-104">Таблица Фамилифилеранжес содержит сведения о конкретных файлах обновленного образа с диапазонами, которые никогда не должны перезаписываться.</span><span class="sxs-lookup"><span data-stu-id="72604-104">The FamilyFileRanges table contains information about particular files of an upgraded image with ranges that should never be overwritten.</span></span> <span data-ttu-id="72604-105">Эта таблица является необязательной в базе данных создания исправлений (файл PCP) и используется функцией [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="72604-105">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="72604-106">Таблица Фамилифилеранжес содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="72604-106">The FamilyFileRanges table has the following columns.</span></span>



| <span data-ttu-id="72604-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="72604-107">Column</span></span>        | <span data-ttu-id="72604-108">Type</span><span class="sxs-lookup"><span data-stu-id="72604-108">Type</span></span> | <span data-ttu-id="72604-109">Ключ</span><span class="sxs-lookup"><span data-stu-id="72604-109">Key</span></span> | <span data-ttu-id="72604-110">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="72604-110">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="72604-111">Семейство</span><span class="sxs-lookup"><span data-stu-id="72604-111">Family</span></span>        | <span data-ttu-id="72604-112">text</span><span class="sxs-lookup"><span data-stu-id="72604-112">text</span></span> | <span data-ttu-id="72604-113">Да</span><span class="sxs-lookup"><span data-stu-id="72604-113">Y</span></span>   | <span data-ttu-id="72604-114">Нет</span><span class="sxs-lookup"><span data-stu-id="72604-114">N</span></span>        |
| <span data-ttu-id="72604-115">фтк</span><span class="sxs-lookup"><span data-stu-id="72604-115">FTK</span></span>           | <span data-ttu-id="72604-116">text</span><span class="sxs-lookup"><span data-stu-id="72604-116">text</span></span> | <span data-ttu-id="72604-117">Да</span><span class="sxs-lookup"><span data-stu-id="72604-117">Y</span></span>   | <span data-ttu-id="72604-118">Нет</span><span class="sxs-lookup"><span data-stu-id="72604-118">N</span></span>        |
| <span data-ttu-id="72604-119">ретаиноффсетс</span><span class="sxs-lookup"><span data-stu-id="72604-119">RetainOffsets</span></span> | <span data-ttu-id="72604-120">text</span><span class="sxs-lookup"><span data-stu-id="72604-120">text</span></span> |     | <span data-ttu-id="72604-121">Нет</span><span class="sxs-lookup"><span data-stu-id="72604-121">N</span></span>        |
| <span data-ttu-id="72604-122">ретаинленгсс</span><span class="sxs-lookup"><span data-stu-id="72604-122">RetainLengths</span></span> | <span data-ttu-id="72604-123">text</span><span class="sxs-lookup"><span data-stu-id="72604-123">text</span></span> |     | <span data-ttu-id="72604-124">Нет</span><span class="sxs-lookup"><span data-stu-id="72604-124">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="72604-125">Столбцы</span><span class="sxs-lookup"><span data-stu-id="72604-125">Columns</span></span>

<dl> <dt>

<span data-ttu-id="72604-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Семьи</span><span class="sxs-lookup"><span data-stu-id="72604-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="72604-127">Внешний ключ к столбцу Family [таблицы имажефамилиес (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="72604-127">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="72604-128"><span id="FTK"></span><span id="ftk"></span>фтк</span><span class="sxs-lookup"><span data-stu-id="72604-128"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="72604-129">Внешний ключ в [файловые таблицы](file-table.md) всех обновленных образов в семействе образов.</span><span class="sxs-lookup"><span data-stu-id="72604-129">Foreign key into the [File tables](file-table.md) of all the upgraded images in the image family.</span></span>

</dd> <dt>

<span data-ttu-id="72604-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>ретаиноффсетс</span><span class="sxs-lookup"><span data-stu-id="72604-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="72604-131">Смещение диапазонов, которые не могут быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="72604-131">The offset of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="72604-132">Значение в этом поле представляет собой список номеров смещений диапазонов для диапазонов, которые не должны перезаписываться в целевых файлах.</span><span class="sxs-lookup"><span data-stu-id="72604-132">The value in this field is a list of the range offset numbers for ranges that are not to be overwritten in the target files.</span></span> <span data-ttu-id="72604-133">Порядок и количество диапазонов в списке должны соответствовать элементам в столбце Ретаинленгсс.</span><span class="sxs-lookup"><span data-stu-id="72604-133">The order and number of the ranges in the list must match the items in the RetainLengths column.</span></span>

<span data-ttu-id="72604-134">Значения могут быть десятичными или шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="72604-134">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="72604-135">[Patchwiz.dll](patchwiz-dll.md) считает значение шестнадцатеричным, если оно имеет префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="72604-135">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="72604-136">Столбцы являются строковыми столбцами, а Patchwiz.dll преобразовывают значения в ULONG.</span><span class="sxs-lookup"><span data-stu-id="72604-136">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="72604-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>ретаинленгсс</span><span class="sxs-lookup"><span data-stu-id="72604-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span></span>
</dt> <dd>

<span data-ttu-id="72604-138">Длина в байтах диапазонов, которые не могут быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="72604-138">The length in bytes of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="72604-139">Значение в этом поле представляет собой список значений длины диапазона для диапазонов, которые должны храниться в целевых файлах.</span><span class="sxs-lookup"><span data-stu-id="72604-139">The value in this field is a list of range length numbers for ranges to retain in target files.</span></span> <span data-ttu-id="72604-140">Порядок и количество диапазонов в списке должны соответствовать элементам в столбце Ретаиноффсетс.</span><span class="sxs-lookup"><span data-stu-id="72604-140">The order and number of the ranges in the list must match the items in the RetainOffsets column.</span></span>

<span data-ttu-id="72604-141">Значения могут быть десятичными или шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="72604-141">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="72604-142">[Patchwiz.dll](patchwiz-dll.md) считает значение шестнадцатеричным, если оно имеет префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="72604-142">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="72604-143">Столбцы являются строковыми столбцами, а Patchwiz.dll преобразовывают значения в ULONG.</span><span class="sxs-lookup"><span data-stu-id="72604-143">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72604-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72604-144">Remarks</span></span>

<span data-ttu-id="72604-145">Смещение и длина, указанные в Ретаиноффсетс и Ретаинленгсс, не должны указывать перекрывающиеся диапазоны.</span><span class="sxs-lookup"><span data-stu-id="72604-145">The offsets and lengths entered in RetainOffsets and RetainLengths must not specify overlapping ranges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72604-146">См. также</span><span class="sxs-lookup"><span data-stu-id="72604-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72604-147">Исправление выбранных регионов файла</span><span class="sxs-lookup"><span data-stu-id="72604-147">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



