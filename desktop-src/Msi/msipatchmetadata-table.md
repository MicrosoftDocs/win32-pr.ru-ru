---
description: Таблица Мсипатчметадата содержит сведения об исправлении установщик Windows, которое требуется для удаления исправления и используется для установки и удаления программ.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Таблица Мсипатчметадата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651170"
---
# <a name="msipatchmetadata-table"></a><span data-ttu-id="331b5-103">Таблица Мсипатчметадата</span><span class="sxs-lookup"><span data-stu-id="331b5-103">MsiPatchMetadata Table</span></span>

<span data-ttu-id="331b5-104">Таблица Мсипатчметадата содержит сведения об исправлении установщик Windows, которое требуется для удаления исправления и используется для **установки и удаления программ**.</span><span class="sxs-lookup"><span data-stu-id="331b5-104">The MsiPatchMetadata Table contains information about a Windows Installer patch that is required to remove the patch and that is used by **Add/Remove Programs**.</span></span>

<span data-ttu-id="331b5-105">Исправления, установленные без этой таблицы в базе данных исправлений (MSP-файл), не могут быть удалены и отсутствуют некоторые сведения из окна " **Установка и удаление программ**".</span><span class="sxs-lookup"><span data-stu-id="331b5-105">Patches installed without this table present in the patch database (.msp file) cannot be removed, and are missing some information from **Add/Remove Programs**.</span></span> <span data-ttu-id="331b5-106">Таблица должна находиться в базе данных файла исправления, а не в преобразовании исправления.</span><span class="sxs-lookup"><span data-stu-id="331b5-106">The table must be in the database of the patch file and not in a transform in the patch.</span></span>

<span data-ttu-id="331b5-107">Таблица Мсипатчметадата содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="331b5-107">The MsiPatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="331b5-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="331b5-108">Column</span></span>   | <span data-ttu-id="331b5-109">Type</span><span class="sxs-lookup"><span data-stu-id="331b5-109">Type</span></span>                         | <span data-ttu-id="331b5-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="331b5-110">Key</span></span> | <span data-ttu-id="331b5-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="331b5-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="331b5-112">Company</span><span class="sxs-lookup"><span data-stu-id="331b5-112">Company</span></span>  | [<span data-ttu-id="331b5-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="331b5-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="331b5-114">Да</span><span class="sxs-lookup"><span data-stu-id="331b5-114">Y</span></span>   | <span data-ttu-id="331b5-115">Да</span><span class="sxs-lookup"><span data-stu-id="331b5-115">Y</span></span>        |
| <span data-ttu-id="331b5-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="331b5-116">Property</span></span> | [<span data-ttu-id="331b5-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="331b5-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="331b5-118">Да</span><span class="sxs-lookup"><span data-stu-id="331b5-118">Y</span></span>   | <span data-ttu-id="331b5-119">Нет</span><span class="sxs-lookup"><span data-stu-id="331b5-119">N</span></span>        |
| <span data-ttu-id="331b5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="331b5-120">Value</span></span>    | [<span data-ttu-id="331b5-121">Text</span><span class="sxs-lookup"><span data-stu-id="331b5-121">Text</span></span>](text.md)             | <span data-ttu-id="331b5-122">Нет</span><span class="sxs-lookup"><span data-stu-id="331b5-122">N</span></span>   | <span data-ttu-id="331b5-123">Нет</span><span class="sxs-lookup"><span data-stu-id="331b5-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="331b5-124">Столбцы</span><span class="sxs-lookup"><span data-stu-id="331b5-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="331b5-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Во</span><span class="sxs-lookup"><span data-stu-id="331b5-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="331b5-126">Название компании.</span><span class="sxs-lookup"><span data-stu-id="331b5-126">The name of the company.</span></span> <span data-ttu-id="331b5-127">Пустое поле (значение null) указывает, что строка содержит одно из стандартных свойств метаданных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="331b5-127">An empty field (a Null value) indicates that the row contains one of the standard metadata properties of the Windows Installer.</span></span> <span data-ttu-id="331b5-128">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="331b5-128">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="331b5-129">Добавив строку в таблицу и введя название компании в этом поле, можно добавить любую компанию, чтобы расширить набор свойств.</span><span class="sxs-lookup"><span data-stu-id="331b5-129">By adding a row to the table and entering a company name in this field, you can add any company to extend the property set.</span></span>

</dd> <dt>

<span data-ttu-id="331b5-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Свойства</span><span class="sxs-lookup"><span data-stu-id="331b5-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="331b5-131">Имя свойства метаданных.</span><span class="sxs-lookup"><span data-stu-id="331b5-131">The name of a metadata property.</span></span>

</dd> <dt>

<span data-ttu-id="331b5-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="331b5-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="331b5-133">Значение свойства метаданных.</span><span class="sxs-lookup"><span data-stu-id="331b5-133">The value of the metadata property.</span></span> <span data-ttu-id="331b5-134">Значение не может быть равно null или пустой строке.</span><span class="sxs-lookup"><span data-stu-id="331b5-134">This can never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="331b5-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="331b5-135">Remarks</span></span>

<span data-ttu-id="331b5-136">Доступно в установщик Windows 3,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="331b5-136">Available in Windows Installer 3.0 and later.</span></span>

<span data-ttu-id="331b5-137">Строки в таблице Мсипатчметадата, содержащие значение NULL в поле CompanyName, относятся к одному из следующих стандартных свойств метаданных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="331b5-137">Rows in the MsiPatchMetadata Table that contain a Null value in the CompanyName field refer to one of the following standard Windows Installer metadata properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="331b5-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="331b5-138">Property</span></span></th>
<th><span data-ttu-id="331b5-139">Описание</span><span class="sxs-lookup"><span data-stu-id="331b5-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="331b5-140">алловремовал</span><span class="sxs-lookup"><span data-stu-id="331b5-140">AllowRemoval</span></span></td>
<td><span data-ttu-id="331b5-141">Указывает, является ли исправление <a href="uninstallable-patches.md">неудаляемым</a>.</span><span class="sxs-lookup"><span data-stu-id="331b5-141">Indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="331b5-142">Если поле значения содержит значение 0 (ноль), исправление не может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="331b5-142">If the value field contains 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="331b5-143">Если поле значения содержит одно (1), исправление является неудаляемым. это свойство зарегистрировано, и его значение можно получить с помощью функции <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>мсижетпатчинфоекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="331b5-143">If the value field contains one (1), the patch is an Uninstallable Patch.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="331b5-144">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="331b5-144">ManufacturerName</span></span></td>
<td><span data-ttu-id="331b5-145">Имя производителя приложения.</span><span class="sxs-lookup"><span data-stu-id="331b5-145">Name of the manufacturer of the application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="331b5-146">минорупдатетаржетртм</span><span class="sxs-lookup"><span data-stu-id="331b5-146">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="331b5-147">Указывает, что исправление предназначено для ОКОНЧАТЕЛЬНОй версии продукта или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="331b5-147">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="331b5-148">Создайте это дополнительное свойство в незначительных исправлениях обновления, содержащих сведения о последовательности, чтобы указать, что исправление Удаляет все исправления до RTM версии продукта или до последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="331b5-148">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="331b5-149">Это свойство доступно в установщик Windows 3,1 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="331b5-149">This property is available in Windows Installer 3.1 and later.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="331b5-150">таржетпродуктнаме</span><span class="sxs-lookup"><span data-stu-id="331b5-150">TargetProductName</span></span></td>
<td><span data-ttu-id="331b5-151">Имя приложения или целевого набора приложений.</span><span class="sxs-lookup"><span data-stu-id="331b5-151">Name of the application or target application suite.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="331b5-152">мореинфаурл</span><span class="sxs-lookup"><span data-stu-id="331b5-152">MoreInfoURL</span></span></td>
<td><span data-ttu-id="331b5-153">URL-адрес, предоставляющий сведения, относящиеся к данному исправлению.</span><span class="sxs-lookup"><span data-stu-id="331b5-153">A URL that provides information specific to this patch.</span></span> <span data-ttu-id="331b5-154">Это свойство зарегистрировано, и его значение можно получить с помощью функции <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>мсижетпатчинфоекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="331b5-154">This property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="331b5-155">Начиная с Windows XP с пакетом обновления 2 (SP2), это значение может быть ссылкой на службу поддержки для исправления, которое отображается в окне <strong>Установка и удаление программ</strong>.</span><span class="sxs-lookup"><span data-stu-id="331b5-155">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="331b5-156">креатионтимеутк</span><span class="sxs-lookup"><span data-stu-id="331b5-156">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="331b5-157">Время создания файла MSP в формате мм-дд-гг чч: мм (месяц-день-год, час: минута).</span><span class="sxs-lookup"><span data-stu-id="331b5-157">Creation time of the .msp file in the form of mm-dd-yy HH:MM (month-day-year hour:minute).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="331b5-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="331b5-158">DisplayName</span></span></td>
<td><span data-ttu-id="331b5-159">Название исправления, которое подходит для общедоступного экрана.</span><span class="sxs-lookup"><span data-stu-id="331b5-159">A title for the patch that is okay for public display.</span></span> <span data-ttu-id="331b5-160">Это свойство зарегистрировано, и его значение можно получить с помощью функции <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>мсижетпатчинфоекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="331b5-160">This property is registered, and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="331b5-161">Начиная с Windows XP с пакетом обновления 2 (SP2), это значение представляет собой имя исправления, которое отображается в окне <strong>Установка и удаление программ</strong>.</span><span class="sxs-lookup"><span data-stu-id="331b5-161">Beginning with Windows XP with SP2, this value is the name of the patch that is displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="331b5-162">Описание</span><span class="sxs-lookup"><span data-stu-id="331b5-162">Description</span></span></td>
<td><span data-ttu-id="331b5-163">Краткое описание исправления.</span><span class="sxs-lookup"><span data-stu-id="331b5-163">Brief description of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="331b5-164">Классификация</span><span class="sxs-lookup"><span data-stu-id="331b5-164">Classification</span></span></td>
<td><span data-ttu-id="331b5-165">Строковое значение, содержащее произвольную категорию обновлений, определенную автором исправления.</span><span class="sxs-lookup"><span data-stu-id="331b5-165">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="331b5-166">Например, авторы исправлений могут указать, что каждое исправление будет классифицироваться как исправление, сводный показатель безопасности, критическое обновление, обновление, пакет обновления или накопительное обновление.</span><span class="sxs-lookup"><span data-stu-id="331b5-166">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="331b5-167">Это свойство обязательно.</span><span class="sxs-lookup"><span data-stu-id="331b5-167">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="331b5-168">оптимизека</span><span class="sxs-lookup"><span data-stu-id="331b5-168">OptimizeCA</span></span></td>
<td><span data-ttu-id="331b5-169">Указывает, должны ли установщик Windows пропускать пользовательские действия при применении исправления.</span><span class="sxs-lookup"><span data-stu-id="331b5-169">Indicates whether the Windows Installer should skip custom actions when applying the patch.</span></span> <span data-ttu-id="331b5-170">Это может сократить время, необходимое для применения исправления.</span><span class="sxs-lookup"><span data-stu-id="331b5-170">This can reduce the time required to apply the patch.</span></span> <span data-ttu-id="331b5-171">Свойство Оптимизека может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="331b5-171">The OptimizeCA property can have one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="331b5-172">0 — не пропускать никаких настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="331b5-172">0 - Do not skip any custom actions.</span></span></li>
<li><span data-ttu-id="331b5-173">1 — пропускать настраиваемые действия при назначении свойств и каталогов.</span><span class="sxs-lookup"><span data-stu-id="331b5-173">1 - Skip property and directory assignment custom actions.</span></span> <span data-ttu-id="331b5-174"><a href="custom-action-type-35.md">Тип настраиваемого действия 35</a> и <a href="custom-action-type-51.md">тип настраиваемого действия 51</a> могут быть пользовательскими действиями назначения свойств и каталогов.</span><span class="sxs-lookup"><span data-stu-id="331b5-174"><a href="custom-action-type-35.md">Custom Action Type 35</a> and <a href="custom-action-type-51.md">Custom Action Type 51</a> can be property and directory assignment custom actions.</span></span></li>
<li><span data-ttu-id="331b5-175">2 — пропускать немедленные пользовательские действия, которые не относятся к назначениям свойств или каталогов.</span><span class="sxs-lookup"><span data-stu-id="331b5-175">2 - Skip immediate custom actions that do not fall into the property or directory assignments.</span></span> <span data-ttu-id="331b5-176">Непосредственные пользовательские действия не включают параметр Мсидбкустомактионтипеинскрипт в столбец Type <a href="customaction-table.md">таблицы CustomAction</a>.</span><span class="sxs-lookup"><span data-stu-id="331b5-176">The immediate custom actions do not include msidbCustomActionTypeInScript option in the Type column of the <a href="customaction-table.md">CustomAction Table</a>.</span></span></li>
<li><span data-ttu-id="331b5-177">4. пропускать пользовательские действия, выполняемые в скрипте.</span><span class="sxs-lookup"><span data-stu-id="331b5-177">4 - Skip custom actions that run within the script.</span></span></li>
</ul>
<span data-ttu-id="331b5-178">Значение параметра Оптимизека должно быть одинаковым для всех устанавливаемых исправлений или никакие пользовательские действия не пропускаются.</span><span class="sxs-lookup"><span data-stu-id="331b5-178">The value of OptimizeCA must be the same for all patches that are being installed or no custom actions are skipped.</span></span> <span data-ttu-id="331b5-179">Например, если устанавливаются два исправления, а для Оптимизека заданы значения 1 и 2 соответственно, никакие пользовательские действия не пропускаются.</span><span class="sxs-lookup"><span data-stu-id="331b5-179">For example, if two patches are being installed, and OptimizeCA is set to the values 1 and 2 respectively, no custom actions are skipped.</span></span> <br/> <span data-ttu-id="331b5-180">Значения Оптимизека можно комбинировать при обработке нескольких новых исправлений.</span><span class="sxs-lookup"><span data-stu-id="331b5-180">The values of OptimizeCA can be combined when processing multiple new patches.</span></span> <span data-ttu-id="331b5-181">Если все исправления содержат значение 1 (одно), которое включается в значения, то все пользовательские действия назначения свойств и каталогов пропускаются.</span><span class="sxs-lookup"><span data-stu-id="331b5-181">If all patches have a 1 (one) included in the values, then all property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="331b5-182">Если одно исправление имеет значение 3 (три) для свойства, а одно исправление имеет значение 1 (одно) для свойства, то пользовательские действия для назначения свойств и каталогов пропускаются.</span><span class="sxs-lookup"><span data-stu-id="331b5-182">If one patch has the value 3 (three)for the property, and one patch has the value 1 (one) for the property, the property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="331b5-183">Однако другие немедленные пользовательские действия выполняются, поскольку не все запрошенные исправления пропускаются.</span><span class="sxs-lookup"><span data-stu-id="331b5-183">However, the other immediate custom actions run, because not all of the patches requested are skipped.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="331b5-184">оптимизединсталлмоде</span><span class="sxs-lookup"><span data-stu-id="331b5-184">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="331b5-185">Если это свойство имеет значение 1 (одно) во всех исправлениях, которые должны быть применены в транзакции, по возможности будет оптимизировано применение исправления.</span><span class="sxs-lookup"><span data-stu-id="331b5-185">If this property is set to 1 (one) in all the patches to be applied in a transaction, an application of the patch is optimized if possible.</span></span> <span data-ttu-id="331b5-186">Дополнительные сведения см. в разделе <a href="patch-optimization.md">Оптимизация исправлений</a>.</span><span class="sxs-lookup"><span data-stu-id="331b5-186">For more information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="331b5-187">Доступно, начиная с установщик Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="331b5-187">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a><span data-ttu-id="331b5-188">Проверка</span><span class="sxs-lookup"><span data-stu-id="331b5-188">Validation</span></span>

<dl>

[<span data-ttu-id="331b5-189">ICE03</span><span class="sxs-lookup"><span data-stu-id="331b5-189">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="331b5-190">ICE06</span><span class="sxs-lookup"><span data-stu-id="331b5-190">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="331b5-191">См. также</span><span class="sxs-lookup"><span data-stu-id="331b5-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="331b5-192">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="331b5-192">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




