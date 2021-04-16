---
description: В таблице Мсипатчсекуенце содержатся все сведения, необходимые установщику для определения последовательности применения небольшого исправления обновления относительно всех остальных исправлений.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Таблица Мсипатчсекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664544"
---
# <a name="msipatchsequence-table"></a><span data-ttu-id="a2979-103">Таблица Мсипатчсекуенце</span><span class="sxs-lookup"><span data-stu-id="a2979-103">MsiPatchSequence Table</span></span>

<span data-ttu-id="a2979-104">В таблице Мсипатчсекуенце содержатся все сведения, необходимые установщику для определения последовательности применения [небольшого исправления обновления](small-updates.md) относительно всех остальных исправлений.</span><span class="sxs-lookup"><span data-stu-id="a2979-104">The MsiPatchSequence table contains all the information the installer requires to determine the sequence of application of a [small update](small-updates.md) patch relative to all other patches.</span></span> <span data-ttu-id="a2979-105">Таблица должна находиться в базе данных файла исправления, а не в преобразовании исправления.</span><span class="sxs-lookup"><span data-stu-id="a2979-105">The table must be in the database of the patch file and not in a transform in the patch.</span></span> <span data-ttu-id="a2979-106">Установщик пропускает эту таблицу при установке [основного](major-upgrades.md) обновления.</span><span class="sxs-lookup"><span data-stu-id="a2979-106">The installer ignores this table when applying a [major upgrade](major-upgrades.md) patch.</span></span> <span data-ttu-id="a2979-107">При применении [незначительного исправления обновления](minor-upgrades.md) установщик использует эту таблицу только для обнаружения заменяемых исправлений, которые не должны быть последовательными.</span><span class="sxs-lookup"><span data-stu-id="a2979-107">When applying a [minor upgrade](minor-upgrades.md) patch, the installer only uses this table to identify superseded patches that must not be sequenced.</span></span>

<span data-ttu-id="a2979-108">**Таблица мсипатчсекуенце** содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="a2979-108">The **MsiPatchSequence table** has the following columns.</span></span>



| <span data-ttu-id="a2979-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="a2979-109">Column</span></span>      | <span data-ttu-id="a2979-110">Type</span><span class="sxs-lookup"><span data-stu-id="a2979-110">Type</span></span>                         | <span data-ttu-id="a2979-111">Ключ</span><span class="sxs-lookup"><span data-stu-id="a2979-111">Key</span></span> | <span data-ttu-id="a2979-112">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="a2979-112">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="a2979-113">патчфамили</span><span class="sxs-lookup"><span data-stu-id="a2979-113">PatchFamily</span></span> | [<span data-ttu-id="a2979-114">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="a2979-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="a2979-115">Да</span><span class="sxs-lookup"><span data-stu-id="a2979-115">Y</span></span>   | <span data-ttu-id="a2979-116">Нет</span><span class="sxs-lookup"><span data-stu-id="a2979-116">N</span></span>        |
| <span data-ttu-id="a2979-117">ProductCode</span><span class="sxs-lookup"><span data-stu-id="a2979-117">ProductCode</span></span> | [<span data-ttu-id="a2979-118">GUID</span><span class="sxs-lookup"><span data-stu-id="a2979-118">GUID</span></span>](guid.md)             | <span data-ttu-id="a2979-119">Да</span><span class="sxs-lookup"><span data-stu-id="a2979-119">Y</span></span>   | <span data-ttu-id="a2979-120">Да</span><span class="sxs-lookup"><span data-stu-id="a2979-120">Y</span></span>        |
| <span data-ttu-id="a2979-121">Последовательность</span><span class="sxs-lookup"><span data-stu-id="a2979-121">Sequence</span></span>    | [<span data-ttu-id="a2979-122">Version</span><span class="sxs-lookup"><span data-stu-id="a2979-122">Version</span></span>](version.md)       | <span data-ttu-id="a2979-123">Нет</span><span class="sxs-lookup"><span data-stu-id="a2979-123">N</span></span>   | <span data-ttu-id="a2979-124">Нет</span><span class="sxs-lookup"><span data-stu-id="a2979-124">N</span></span>        |
| <span data-ttu-id="a2979-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a2979-125">Attributes</span></span>  | [<span data-ttu-id="a2979-126">Integer</span><span class="sxs-lookup"><span data-stu-id="a2979-126">Integer</span></span>](integer.md)       | <span data-ttu-id="a2979-127">Нет</span><span class="sxs-lookup"><span data-stu-id="a2979-127">N</span></span>   | <span data-ttu-id="a2979-128">Да</span><span class="sxs-lookup"><span data-stu-id="a2979-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a2979-129">Столбцы</span><span class="sxs-lookup"><span data-stu-id="a2979-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a2979-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>патчфамили</span><span class="sxs-lookup"><span data-stu-id="a2979-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="a2979-131">Указывает, что исправление является членом семейства исправлений, указанного в этом поле.</span><span class="sxs-lookup"><span data-stu-id="a2979-131">Specifies that the patch is a member of the patch family named in this field.</span></span> <span data-ttu-id="a2979-132">Исправления в одном семействе исправлений, предназначенных для той же версии продукта, сортируются по значениям в столбце последовательности.</span><span class="sxs-lookup"><span data-stu-id="a2979-132">Patches in the same patch family that target the same product version are sorted by the values in the Sequence column.</span></span> <span data-ttu-id="a2979-133">Исправления в семействе исправлений применяются к целевому продукту в порядке возрастания последовательности.</span><span class="sxs-lookup"><span data-stu-id="a2979-133">The patches within the patch family are applied to the target product in the order of increasing sequence.</span></span> <span data-ttu-id="a2979-134">Патчфамили также используется для определения того, какие исправления следует заменить.</span><span class="sxs-lookup"><span data-stu-id="a2979-134">The PatchFamily is also used to determine which patches are to be superseded.</span></span> <span data-ttu-id="a2979-135">Исправление может быть указано в нескольких строках и принадлежать к нескольким семействам исправлений, если оно применяется к нескольким продуктам или включает несколько исправлений.</span><span class="sxs-lookup"><span data-stu-id="a2979-135">A patch may be listed in multiple rows and belong to multiple patch families if it applies to more than one product or includes multiple fixes.</span></span>

<span data-ttu-id="a2979-136">Установщик Windows не интерпретирует значение Патчфамили любым способом, отличным от сравнения для равенства с другими значениями Патчфамили.</span><span class="sxs-lookup"><span data-stu-id="a2979-136">The Windows Installer does not interpret the PatchFamily value in any way other than comparisons for equality against other PatchFamily values.</span></span> <span data-ttu-id="a2979-137">Значение Патчфамили должно быть уникальным в пределах ProductCode, предназначенного для набора исправлений.</span><span class="sxs-lookup"><span data-stu-id="a2979-137">A PatchFamily value must be unique within the ProductCode targeted by the set of patches.</span></span> <span data-ttu-id="a2979-138">В сценариях комплексного исправления идентификатор Патчфамили может требоваться глобально уникальным.</span><span class="sxs-lookup"><span data-stu-id="a2979-138">In the complex patching scenarios the PatchFamily identifier may need to be globally unique.</span></span>

</dd> <dt>

<span data-ttu-id="a2979-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span><span class="sxs-lookup"><span data-stu-id="a2979-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span></span>
</dt> <dd>

<span data-ttu-id="a2979-140">Значение в этом поле является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a2979-140">A value in this field is optional.</span></span> <span data-ttu-id="a2979-141">Если в этом поле введен идентификатор GUID [кода продукта](product-codes.md) , а исправление применяется к указанному продукту, то исправление сортируется и применяется как член указанного патчфамили.</span><span class="sxs-lookup"><span data-stu-id="a2979-141">If a [product code](product-codes.md) GUID is entered in this field and the patch is being applied to the specified product, the patch is sorted and applied as a member of the specified PatchFamily.</span></span> <span data-ttu-id="a2979-142">Если в этом поле введен идентификатор GUID кода продукта, а исправление не применяется к продукту, указанному в ProductCode, эта строка игнорируется.</span><span class="sxs-lookup"><span data-stu-id="a2979-142">If a product code GUID is entered in this field and the patch is not being applied to the product specified by ProductCode, this row is ignored.</span></span> <span data-ttu-id="a2979-143">Если значение ProductCode равно NULL, то исправление сортируется и применяется как член Патчфамили для всех целевых объектов исправления независимо от кода продукта.</span><span class="sxs-lookup"><span data-stu-id="a2979-143">If the value in ProductCode is NULL, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

<span data-ttu-id="a2979-144">Исправление может содержать несколько строк в одном Патчфамили и разные ProductCode для каждого продукта, для которого предназначено исправление.</span><span class="sxs-lookup"><span data-stu-id="a2979-144">A patch can have multiple rows in the same PatchFamily and a different ProductCode for each product targeted by the patch.</span></span> <span data-ttu-id="a2979-145">Одна строка для Патчфамили может указывать значение NULL для ProductCode.</span><span class="sxs-lookup"><span data-stu-id="a2979-145">One row for the PatchFamily can specify NULL for ProductCode.</span></span> <span data-ttu-id="a2979-146">Если целевой продукт соответствует строке со значением ProductCode, отличным от NULL, то установщик использует соответствующую строку и игнорирует строку с нулевым значением ProductCode.</span><span class="sxs-lookup"><span data-stu-id="a2979-146">If the target product matches a row with a non-NULL ProductCode, the installer uses the matching row and ignores the row with the NULL ProductCode.</span></span> <span data-ttu-id="a2979-147">Если ни один из указанных кодов продуктов не соответствует целевому объекту, то исправление сортируется и применяется как член Патчфамили для всех целей исправления независимо от кода продукта.</span><span class="sxs-lookup"><span data-stu-id="a2979-147">If none of the specified product codes match the target, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

</dd> <dt>

<span data-ttu-id="a2979-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="a2979-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="a2979-149">Значение в столбце Sequence указывает последовательность этого исправления в указанном Патчфамили.</span><span class="sxs-lookup"><span data-stu-id="a2979-149">The value in the Sequence column specifies the sequence of this patch within the specified PatchFamily.</span></span> <span data-ttu-id="a2979-150">Значение в последовательности выражается в формате данных [версии](version.md) .</span><span class="sxs-lookup"><span data-stu-id="a2979-150">The value in Sequence is expressed in the format of [Version](version.md) data.</span></span> <span data-ttu-id="a2979-151">Значение содержит от 1 до 4 полей, а каждое поле имеет диапазон от 0 до 65535.</span><span class="sxs-lookup"><span data-stu-id="a2979-151">The value contains between 1 and 4 fields and each field has a range of 0 to 65535.</span></span> <span data-ttu-id="a2979-152">Элементы Патчфамили сортируются и применяются к целевому продукту в порядке возрастания значений последовательности.</span><span class="sxs-lookup"><span data-stu-id="a2979-152">Members of PatchFamily are sorted and applied to the target product in the order of increasing Sequence values.</span></span> <span data-ttu-id="a2979-153">Например, следующие шесть значений увеличиваются: 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.</span><span class="sxs-lookup"><span data-stu-id="a2979-153">For example, the following six values are increasing: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.</span></span>

</dd> <dt>

<span data-ttu-id="a2979-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибута</span><span class="sxs-lookup"><span data-stu-id="a2979-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="a2979-155">Наличие атрибута **мсидбпатчсекуенцесуперседиарлиер** в строке указывает на то, что [небольшое обновление](small-updates.md) заменяет обновления, предоставляемые всеми исправлениями, с меньшими значениями последовательности в одном патчфамили.</span><span class="sxs-lookup"><span data-stu-id="a2979-155">The presence of the **msidbPatchSequenceSupersedeEarlier** attribute in a row indicates that the [small update](small-updates.md) patch supersedes the updates provided by all patches with lesser Sequence values in the same PatchFamily.</span></span> <span data-ttu-id="a2979-156">Это исправление содержит все исправления, описанные в предыдущих исправлениях в указанном Патчфамили.</span><span class="sxs-lookup"><span data-stu-id="a2979-156">This patch contains all fixes provided by earlier patches in the specified PatchFamily.</span></span> <span data-ttu-id="a2979-157">Этот атрибут не означает, что это исправление заменяет предыдущие исправления во всех случаях, так как предыдущие исправления могут принадлежать к нескольким семействам исправлений.</span><span class="sxs-lookup"><span data-stu-id="a2979-157">This attribute does not mean that this patch supersedes the earlier patches in all cases because the earlier patches can belong to multiple patch families.</span></span>

<span data-ttu-id="a2979-158">[Небольшое обновление](small-updates.md) не может заменять [незначительное](minor-upgrades.md) обновление или [существенное](major-upgrades.md) обновление при любых обстоятельствах, даже если задан параметр **мсидбпатчсекуенцесуперседиарлиер** .</span><span class="sxs-lookup"><span data-stu-id="a2979-158">A [small update](small-updates.md) patch cannot supersede a [minor upgrade](minor-upgrades.md) or [major upgrade](major-upgrades.md) patch under any circumstances, even if the **msidbPatchSequenceSupersedeEarlier** is set.</span></span> 

| <span data-ttu-id="a2979-159">Имя</span><span class="sxs-lookup"><span data-stu-id="a2979-159">Name</span></span>                                   | <span data-ttu-id="a2979-160">Значение</span><span class="sxs-lookup"><span data-stu-id="a2979-160">Value</span></span> | <span data-ttu-id="a2979-161">Значение</span><span class="sxs-lookup"><span data-stu-id="a2979-161">Meaning</span></span>                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | <span data-ttu-id="a2979-162">0x00</span><span class="sxs-lookup"><span data-stu-id="a2979-162">0x00</span></span>  | <span data-ttu-id="a2979-163">Указывает простое значение последовательности.</span><span class="sxs-lookup"><span data-stu-id="a2979-163">Indicates a simple sequencing value.</span></span>                              |
| <span data-ttu-id="a2979-164">**мсидбпатчсекуенцесуперседиарлиер**</span><span class="sxs-lookup"><span data-stu-id="a2979-164">**msidbPatchSequenceSupersedeEarlier**</span></span> | <span data-ttu-id="a2979-165">0x01</span><span class="sxs-lookup"><span data-stu-id="a2979-165">0x01</span></span>  | <span data-ttu-id="a2979-166">Указывает исправление, заменяющее предыдущие исправления в этом семействе.</span><span class="sxs-lookup"><span data-stu-id="a2979-166">Indicates a patch that supersedes earlier patches in this family.</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="a2979-167">Проверка</span><span class="sxs-lookup"><span data-stu-id="a2979-167">Validation</span></span>

<dl>

[<span data-ttu-id="a2979-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="a2979-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a2979-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="a2979-169">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="a2979-170">См. также</span><span class="sxs-lookup"><span data-stu-id="a2979-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2979-171">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="a2979-171">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



