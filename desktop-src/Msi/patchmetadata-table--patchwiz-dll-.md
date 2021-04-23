---
description: Таблица Патчметадата содержит сведения об исправлении установщик Windows, которое требуется для удаления исправления и используется для установки и удаления программ.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Таблица Патчметадата (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651166"
---
# <a name="patchmetadata-table-patchwizdll"></a><span data-ttu-id="80a35-103">Таблица Патчметадата (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="80a35-103">PatchMetadata Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="80a35-104">Таблица Патчметадата содержит сведения об исправлении установщик Windows, которое требуется для удаления исправления и используется для установки и удаления программ.</span><span class="sxs-lookup"><span data-stu-id="80a35-104">The PatchMetadata Table contains information about a Windows Installer patch that is required to remove a patch and that is used by Add/Remove Programs.</span></span> <span data-ttu-id="80a35-105">Все свойства в таблице Патчметадата добавляются в [таблицу мсипатчметадата](msipatchmetadata-table.md) MSP-файла для исправления.</span><span class="sxs-lookup"><span data-stu-id="80a35-105">All the properties in the PatchMetadata Table are added to the [MsiPatchMetadata Table](msipatchmetadata-table.md) of the .msp file for a patch.</span></span>

<span data-ttu-id="80a35-106">Таблица Патчметадата требуется в файлах свойств для создания исправления (PCP-файлы), имеющих Минимумрекуиредмсиверсион, равный 300 в [таблице свойств](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="80a35-106">The PatchMetadata Table is required in patch creation properties files (.pcp files) that have a MinimumRequiredMsiVersion equal to 300 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="80a35-107">Таблица является необязательной, если Минимумрекуиредмсиверсион не равно 300.</span><span class="sxs-lookup"><span data-stu-id="80a35-107">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

<span data-ttu-id="80a35-108">Таблица Патчметадата содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="80a35-108">The PatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="80a35-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="80a35-109">Column</span></span>   | <span data-ttu-id="80a35-110">Type</span><span class="sxs-lookup"><span data-stu-id="80a35-110">Type</span></span> | <span data-ttu-id="80a35-111">Ключ</span><span class="sxs-lookup"><span data-stu-id="80a35-111">Key</span></span> | <span data-ttu-id="80a35-112">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="80a35-112">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="80a35-113">Company</span><span class="sxs-lookup"><span data-stu-id="80a35-113">Company</span></span>  | <span data-ttu-id="80a35-114">text</span><span class="sxs-lookup"><span data-stu-id="80a35-114">text</span></span> | <span data-ttu-id="80a35-115">Да</span><span class="sxs-lookup"><span data-stu-id="80a35-115">Y</span></span>   | <span data-ttu-id="80a35-116">Да</span><span class="sxs-lookup"><span data-stu-id="80a35-116">Y</span></span>        |
| <span data-ttu-id="80a35-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="80a35-117">Property</span></span> | <span data-ttu-id="80a35-118">text</span><span class="sxs-lookup"><span data-stu-id="80a35-118">text</span></span> | <span data-ttu-id="80a35-119">Да</span><span class="sxs-lookup"><span data-stu-id="80a35-119">Y</span></span>   | <span data-ttu-id="80a35-120">Нет</span><span class="sxs-lookup"><span data-stu-id="80a35-120">N</span></span>        |
| <span data-ttu-id="80a35-121">Значение</span><span class="sxs-lookup"><span data-stu-id="80a35-121">Value</span></span>    | <span data-ttu-id="80a35-122">text</span><span class="sxs-lookup"><span data-stu-id="80a35-122">text</span></span> |     | <span data-ttu-id="80a35-123">Да</span><span class="sxs-lookup"><span data-stu-id="80a35-123">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="80a35-124">Столбцы</span><span class="sxs-lookup"><span data-stu-id="80a35-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="80a35-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Во</span><span class="sxs-lookup"><span data-stu-id="80a35-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="80a35-126">Название компании.</span><span class="sxs-lookup"><span data-stu-id="80a35-126">The name of the company.</span></span> <span data-ttu-id="80a35-127">Пустое поле (значение null) указывает, что эта строка содержит одно из стандартных свойств метаданных.</span><span class="sxs-lookup"><span data-stu-id="80a35-127">An empty field (a Null value) indicates that this row contains one of the standard metadata properties.</span></span> <span data-ttu-id="80a35-128">Компания может расширить набор свойств, добавив строку в таблицу и введя название компании в этом поле.</span><span class="sxs-lookup"><span data-stu-id="80a35-128">A company can extend the property set by adding a row to the table, and entering a company name in this field.</span></span>

</dd> <dt>

<span data-ttu-id="80a35-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Свойства</span><span class="sxs-lookup"><span data-stu-id="80a35-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="80a35-130">Имя свойства метаданных.</span><span class="sxs-lookup"><span data-stu-id="80a35-130">The name of a metadata property.</span></span> <span data-ttu-id="80a35-131">Свойства Алловремовал, ManufacturerName, Таржетпродуктнаме, Мореинфаурл, DisplayName, Description и Classification необходимы в таблице Патчметадата.</span><span class="sxs-lookup"><span data-stu-id="80a35-131">The AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description, and Classification properties are required in the PatchMetadata Table .</span></span> <span data-ttu-id="80a35-132">Это поле должно содержать одно из следующих стандартных свойств метаданных, если поле Company пустое (значение null).</span><span class="sxs-lookup"><span data-stu-id="80a35-132">This field must contain one of the following standard metadata properties if the Company field is empty (a Null value).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80a35-133">Свойство</span><span class="sxs-lookup"><span data-stu-id="80a35-133">Property</span></span></th>
<th><span data-ttu-id="80a35-134">Описание</span><span class="sxs-lookup"><span data-stu-id="80a35-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80a35-135">алловремовал</span><span class="sxs-lookup"><span data-stu-id="80a35-135">AllowRemoval</span></span></td>
<td><span data-ttu-id="80a35-136">Целочисленное значение, указывающее, является ли исправление <a href="uninstallable-patches.md">неудаляемым</a>.</span><span class="sxs-lookup"><span data-stu-id="80a35-136">An integer value that indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="80a35-137">Если поле значения содержит значение 0 (ноль), исправление не может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="80a35-137">If the Value field contains a 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="80a35-138">Если поле значения содержит значение 1 (одно), это исправление является удаляемым.</span><span class="sxs-lookup"><span data-stu-id="80a35-138">If the Value field contains 1 (one), the patch is an Uninstallable Patch.</span></span> <span data-ttu-id="80a35-139">Это свойство является обязательным. Это свойство зарегистрировано, и его значение можно получить с помощью функции <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>мсижетпатчинфоекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="80a35-139">This property is required.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80a35-140">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="80a35-140">ManufacturerName</span></span></td>
<td><span data-ttu-id="80a35-141">Строковое значение, содержащее имя производителя приложения.</span><span class="sxs-lookup"><span data-stu-id="80a35-141">A string value that contains the name of the manufacturer of the application.</span></span> <span data-ttu-id="80a35-142">Это свойство обязательно.</span><span class="sxs-lookup"><span data-stu-id="80a35-142">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80a35-143">минорупдатетаржетртм</span><span class="sxs-lookup"><span data-stu-id="80a35-143">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="80a35-144">Указывает, что исправление предназначено для ОКОНЧАТЕЛЬНОй версии продукта или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="80a35-144">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="80a35-145">Создайте это дополнительное свойство в незначительных исправлениях обновления, содержащих сведения о последовательности, чтобы указать, что исправление Удаляет все исправления до RTM версии продукта или до последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="80a35-145">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="80a35-146">Это свойство доступно, начиная с установщик Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="80a35-146">This property is available beginning with Windows Installer 3.1.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="80a35-147">Чтобы для установки исправления требовалось установить установщик Windows 3,1, установите свойство Минимумрекуиредмсиверсион в значение 310 в <a href="properties-table-patchwiz-dll-.md">таблице Properties</a> файла. PCP.</span><span class="sxs-lookup"><span data-stu-id="80a35-147">To require that Windows Installer 3.1 be installed to apply the patch, set the MinimumRequiredMsiVersion property to 310 in the <a href="properties-table-patchwiz-dll-.md">Properties Table</a> of the .pcp file.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80a35-148">таржетпродуктнаме</span><span class="sxs-lookup"><span data-stu-id="80a35-148">TargetProductName</span></span></td>
<td><span data-ttu-id="80a35-149">Строковое значение, содержащее имя приложения или целевого набора приложений.</span><span class="sxs-lookup"><span data-stu-id="80a35-149">A string value that contains the name of the application or target application suite.</span></span> <span data-ttu-id="80a35-150">Это свойство обязательно.</span><span class="sxs-lookup"><span data-stu-id="80a35-150">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80a35-151">мореинфаурл</span><span class="sxs-lookup"><span data-stu-id="80a35-151">MoreInfoURL</span></span></td>
<td><span data-ttu-id="80a35-152">Строковое значение, содержащее URL-адрес, указывающий на сведения об этом исправлении.</span><span class="sxs-lookup"><span data-stu-id="80a35-152">A string value that contains a URL pointing to information for this patch.</span></span> <span data-ttu-id="80a35-153">Это обязательное свойство зарегистрировано, и его значение можно получить с помощью функции <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>мсижетпатчинфоекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="80a35-153">This required property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="80a35-154">Начиная с Windows XP с пакетом обновления 2 (SP2), это значение может быть ссылкой на службу поддержки для исправления, которое отображается в окне Установка и удаление программ.</span><span class="sxs-lookup"><span data-stu-id="80a35-154">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in Add/Remove Programs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80a35-155">креатионтимеутк</span><span class="sxs-lookup"><span data-stu-id="80a35-155">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="80a35-156">Строковое значение, содержащее время создания файла MSP в формате mm-дд-гг чч: мм (месяц-день-год, час: минута).</span><span class="sxs-lookup"><span data-stu-id="80a35-156">A string value that contains the creation time of the .msp file in the form mm-dd-yy HH:MM (month-day-year hour:minute).</span></span> <span data-ttu-id="80a35-157">Это необязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="80a35-157">This property is optional.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80a35-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="80a35-158">DisplayName</span></span></td>
<td><span data-ttu-id="80a35-159">Строковое значение, содержащее название обновления, которое подходит для общедоступного экрана.</span><span class="sxs-lookup"><span data-stu-id="80a35-159">A string value that contains the title for the patch that is suitable for public display.</span></span> <span data-ttu-id="80a35-160">Это свойство обязательно.</span><span class="sxs-lookup"><span data-stu-id="80a35-160">This property is required.</span></span> <span data-ttu-id="80a35-161">Это свойство зарегистрировано, и его значение можно получить с помощью функции <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>мсижетпатчинфоекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="80a35-161">This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="80a35-162">Начиная с Windows XP с пакетом обновления 2 (SP2) это значение представляет собой имя исправления, которое отображается в окне Установка и удаление программ, начиная с Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="80a35-162">Beginning with Windows XP with SP2, this value is the name of the patch displayed in Add/Remove Programs beginning with Windows XP with SP2.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80a35-163">Описание</span><span class="sxs-lookup"><span data-stu-id="80a35-163">Description</span></span></td>
<td><span data-ttu-id="80a35-164">Строковое значение, содержащее краткое описание исправления.</span><span class="sxs-lookup"><span data-stu-id="80a35-164">A string value that contains a brief description of the patch.</span></span> <span data-ttu-id="80a35-165">Это свойство обязательно.</span><span class="sxs-lookup"><span data-stu-id="80a35-165">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80a35-166">Классификация</span><span class="sxs-lookup"><span data-stu-id="80a35-166">Classification</span></span></td>
<td><span data-ttu-id="80a35-167">Строковое значение, содержащее произвольную категорию обновлений, определенную автором исправления.</span><span class="sxs-lookup"><span data-stu-id="80a35-167">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="80a35-168">Например, авторы исправлений могут указать, что каждое исправление будет классифицироваться как исправление, сводный показатель безопасности, критическое обновление, обновление, пакет обновления или накопительное обновление.</span><span class="sxs-lookup"><span data-stu-id="80a35-168">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="80a35-169">Это свойство обязательно.</span><span class="sxs-lookup"><span data-stu-id="80a35-169">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80a35-170">оптимизединсталлмоде</span><span class="sxs-lookup"><span data-stu-id="80a35-170">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="80a35-171">Если для этого свойства задано значение 1 (одно) во всех исправлениях, которые будут применены в транзакции, то применение исправления будет оптимизировано по возможности.</span><span class="sxs-lookup"><span data-stu-id="80a35-171">If this property is set to 1 (one) in all the patches to be applied in a transaction, the application of the patch is optimized if possible.</span></span> <span data-ttu-id="80a35-172">Дополнительные сведения см. в разделе <a href="patch-optimization.md">Оптимизация исправлений</a>.</span><span class="sxs-lookup"><span data-stu-id="80a35-172">For information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="80a35-173">Доступно, начиная с установщик Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="80a35-173">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="80a35-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="80a35-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="80a35-175">Значение свойства метаданных.</span><span class="sxs-lookup"><span data-stu-id="80a35-175">Value of the metadata property.</span></span> <span data-ttu-id="80a35-176">Значение не может быть равно null или пустой строке.</span><span class="sxs-lookup"><span data-stu-id="80a35-176">This can never be Null or an empty string.</span></span> <span data-ttu-id="80a35-177">Это значение может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="80a35-177">This value can be localized.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="80a35-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80a35-178">Remarks</span></span>

<span data-ttu-id="80a35-179">Доступно начиная с установщик Windows 3,0.</span><span class="sxs-lookup"><span data-stu-id="80a35-179">Available beginning in Windows Installer 3.0.</span></span>

<span data-ttu-id="80a35-180">Все свойства, созданные в таблице Патчметадата, добавляются в таблицу Мсипатчметадата файла MSP.</span><span class="sxs-lookup"><span data-stu-id="80a35-180">All properties authored into the PatchMetadata Table are added to the MsiPatchMetadata table of the msp file.</span></span> <span data-ttu-id="80a35-181">Свойства Алловремовал, Мореинфаурл и DisplayName зарегистрированы и доступны через [**мсижетпатчинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="80a35-181">AllowRemoval, MoreInfoURL and DisplayName properties are registered and are accessible through the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

 

 




