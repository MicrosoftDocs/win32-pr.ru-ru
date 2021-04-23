---
description: Таблица Таржетимажес содержит сведения о целевых образах продукта. Пакет обновления установщик Windows обновляет целевой образ в обновленном образе.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Таблица Таржетимажес (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913068"
---
# <a name="targetimages-table-patchwizdll"></a><span data-ttu-id="bb2d2-104">Таблица Таржетимажес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="bb2d2-104">TargetImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="bb2d2-105">Таблица Таржетимажес содержит сведения о целевых образах продукта.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-105">The TargetImages table contains information about the target images of the product.</span></span> <span data-ttu-id="bb2d2-106">Пакет обновления установщик Windows обновляет целевой образ в обновленном образе.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span>

<span data-ttu-id="bb2d2-107">Таблица Таржетимажес, содержащая по крайней мере одну запись, необходима в каждой базе данных создания исправлений (файл. PCP).</span><span class="sxs-lookup"><span data-stu-id="bb2d2-107">A TargetImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="bb2d2-108">Эта таблица используется функцией [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="bb2d2-108">This table is used by the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="bb2d2-109">Таблица Таржетимажес содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-109">The TargetImages table has the following columns.</span></span>



| <span data-ttu-id="bb2d2-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="bb2d2-110">Column</span></span>                | <span data-ttu-id="bb2d2-111">Type</span><span class="sxs-lookup"><span data-stu-id="bb2d2-111">Type</span></span>    | <span data-ttu-id="bb2d2-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="bb2d2-112">Key</span></span> | <span data-ttu-id="bb2d2-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="bb2d2-113">Nullable</span></span> |
|-----------------------|---------|-----|----------|
| <span data-ttu-id="bb2d2-114">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="bb2d2-114">Target</span></span>                | <span data-ttu-id="bb2d2-115">text</span><span class="sxs-lookup"><span data-stu-id="bb2d2-115">text</span></span>    | <span data-ttu-id="bb2d2-116">Да</span><span class="sxs-lookup"><span data-stu-id="bb2d2-116">Y</span></span>   | <span data-ttu-id="bb2d2-117">Нет</span><span class="sxs-lookup"><span data-stu-id="bb2d2-117">N</span></span>        |
| <span data-ttu-id="bb2d2-118">мсипас</span><span class="sxs-lookup"><span data-stu-id="bb2d2-118">MsiPath</span></span>               | <span data-ttu-id="bb2d2-119">text</span><span class="sxs-lookup"><span data-stu-id="bb2d2-119">text</span></span>    |     | <span data-ttu-id="bb2d2-120">Нет</span><span class="sxs-lookup"><span data-stu-id="bb2d2-120">N</span></span>        |
| <span data-ttu-id="bb2d2-121">симболпасс</span><span class="sxs-lookup"><span data-stu-id="bb2d2-121">SymbolPaths</span></span>           | <span data-ttu-id="bb2d2-122">text</span><span class="sxs-lookup"><span data-stu-id="bb2d2-122">text</span></span>    |     | <span data-ttu-id="bb2d2-123">Да</span><span class="sxs-lookup"><span data-stu-id="bb2d2-123">Y</span></span>        |
| <span data-ttu-id="bb2d2-124">Обновлено</span><span class="sxs-lookup"><span data-stu-id="bb2d2-124">Upgraded</span></span>              | <span data-ttu-id="bb2d2-125">text</span><span class="sxs-lookup"><span data-stu-id="bb2d2-125">text</span></span>    |     | <span data-ttu-id="bb2d2-126">Нет</span><span class="sxs-lookup"><span data-stu-id="bb2d2-126">N</span></span>        |
| <span data-ttu-id="bb2d2-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="bb2d2-127">Order</span></span>                 | <span data-ttu-id="bb2d2-128">Целое число</span><span class="sxs-lookup"><span data-stu-id="bb2d2-128">integer</span></span> |     | <span data-ttu-id="bb2d2-129">Нет</span><span class="sxs-lookup"><span data-stu-id="bb2d2-129">N</span></span>        |
| <span data-ttu-id="bb2d2-130">продуктвалидатефлагс</span><span class="sxs-lookup"><span data-stu-id="bb2d2-130">ProductValidateFlags</span></span>  | <span data-ttu-id="bb2d2-131">text</span><span class="sxs-lookup"><span data-stu-id="bb2d2-131">text</span></span>    |     | <span data-ttu-id="bb2d2-132">Да</span><span class="sxs-lookup"><span data-stu-id="bb2d2-132">Y</span></span>        |
| <span data-ttu-id="bb2d2-133">игноремиссингсркфилес</span><span class="sxs-lookup"><span data-stu-id="bb2d2-133">IgnoreMissingSrcFiles</span></span> | <span data-ttu-id="bb2d2-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="bb2d2-134">integer</span></span> |     | <span data-ttu-id="bb2d2-135">Нет</span><span class="sxs-lookup"><span data-stu-id="bb2d2-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bb2d2-136">Столбцы</span><span class="sxs-lookup"><span data-stu-id="bb2d2-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bb2d2-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Мишень</span><span class="sxs-lookup"><span data-stu-id="bb2d2-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="bb2d2-138">Идентификатор целевого образа.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-138">Identifier for a target image.</span></span> <span data-ttu-id="bb2d2-139">Пакет исправлений обновляет целевой образ, указанный в этом столбце, на обновленный образ, указанный в обновленном столбце.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-139">The patch package updates the target image specified in this column to the upgraded image specified in the Upgraded column.</span></span> <span data-ttu-id="bb2d2-140">Для каждого обновленного образа существует один или несколько целевых образов.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-140">There are one or more target images for each upgraded image.</span></span> <span data-ttu-id="bb2d2-141">Целевой образ должен представлять собой полностью несжатый образ установки продукта, например административный образ или образ установки без сжатия на компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-141">The target image must be a fully uncompressed setup image of the product, such as an administrative image or an uncompressed setup image on a CD-ROM.</span></span> <span data-ttu-id="bb2d2-142">Обратите внимание, что функция [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) не создает двоичные исправления для файлов в ящиках.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-142">Note that the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function does not generate binary patches for files in cabinets.</span></span> <span data-ttu-id="bb2d2-143">Значение в этом поле используется со значением в обновленном поле для создания имен преобразований, добавляемых установщиком в пакет исправлений.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-143">The value in this field is used with the value in the Upgraded field to generate the names of the transforms that the installer adds to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="bb2d2-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>мсипас</span><span class="sxs-lookup"><span data-stu-id="bb2d2-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="bb2d2-145">В этом поле указывается полный путь, включая имя файла, с расположением MSI файла для целевого образа.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-145">This field specifies the full path, including the file name, to the location of the .msi file for the target image.</span></span> <span data-ttu-id="bb2d2-146">Это расположение исходных файлов для целевого образа.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-146">This is the location of the source files for the target image.</span></span>

</dd> <dt>

<span data-ttu-id="bb2d2-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>симболпасс</span><span class="sxs-lookup"><span data-stu-id="bb2d2-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="bb2d2-148">Разделенный точками с запятой список папок для поиска файлов символов, которые могут использоваться для оптимизации создания двоичного исправления.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-148">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="bb2d2-149">Обратите внимание, что поиск в подкаталогах папок, указанных в этом поле, не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-149">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="bb2d2-150">Оптимизированное двоичное обновление может быть небольшим.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-150">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="bb2d2-151">Microsoft Visual C++ должны быть установлены на компьютере, создающем исправление, и использоваться для создания файлов символов.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-151">Microsoft Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="bb2d2-152">Это поле является необязательным, и установщик создает двоичное исправление, даже если файлы символов не указаны или если файлы символов становятся недоступными для Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-152">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="bb2d2-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Обновит</span><span class="sxs-lookup"><span data-stu-id="bb2d2-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="bb2d2-154">Внешний ключ к обновленному столбцу [таблицы упградедимажес](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="bb2d2-154">Foreign key to the Upgraded column of the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="bb2d2-155">Функция [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) игнорирует все обновленные образы, на которые не ссылается хотя бы одна запись таблицы таржетимажес.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-155">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function ignores any upgraded image that is not referenced by at least one record of the TargetImages table.</span></span>

</dd> <dt>

<span data-ttu-id="bb2d2-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Порядок</span><span class="sxs-lookup"><span data-stu-id="bb2d2-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="bb2d2-157">Относительный порядок целевого изображения.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-157">Relative order of the target image.</span></span> <span data-ttu-id="bb2d2-158">Так как к обновленному образу можно применить несколько целевых объектов, поле "порядок" предоставляет средства для упорядочения преобразований в списке "преобразования исправлений".</span><span class="sxs-lookup"><span data-stu-id="bb2d2-158">Because multiple targets can be patched to an upgraded image, the Order field provides a means to sequence the transforms in the patch transforms list.</span></span> <span data-ttu-id="bb2d2-159">Обычно порядок — от самого старого до нового изображения.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-159">Commonly, the order is from oldest to newest image.</span></span>

</dd> <dt>

<span data-ttu-id="bb2d2-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>продуктвалидатефлагс</span><span class="sxs-lookup"><span data-stu-id="bb2d2-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span></span>
</dt> <dd>

<span data-ttu-id="bb2d2-161">Поле Продуктвалидатефлагс используется для определения проверки продукта, чтобы избежать применения несущественных преобразований.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-161">The ProductValidateFlags field is used to specify product checking to avoid applying irrelevant transforms.</span></span> <span data-ttu-id="bb2d2-162">Значение, указанное в этом поле, должно представлять собой шестнадцатеричное целое число из 8 цифр и одно из допустимых значений параметра *ивалидатион* функции [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="bb2d2-162">The value entered in this field must be an 8-digit hex integer and one of the valid values for the *iValidation* parameter of the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function.</span></span> <span data-ttu-id="bb2d2-163">Значение по умолчанию — 0x00000922, которое равно **мситрансформ \_ Validate \_ упдатеверсион**  +  **мситрансформ \_ проверить \_ невекуалбасеверсион**  +  **мситрансформ \_ Validate \_ UPGRADECODE**  +  **мситрансформ \_ проверить \_ продукт**.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-163">The default value is 0x00000922 which equals **MSITRANSFORM\_VALIDATE\_UPDATEVERSION** + **MSITRANSFORM\_VALIDATE\_NEWEQUALBASEVERSION** + **MSITRANSFORM\_VALIDATE\_UPGRADECODE** + **MSITRANSFORM\_VALIDATE\_PRODUCT**.</span></span>

</dd> <dt>

<span data-ttu-id="bb2d2-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>игноремиссингсркфилес</span><span class="sxs-lookup"><span data-stu-id="bb2d2-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span></span>
</dt> <dd>

<span data-ttu-id="bb2d2-165">Если для этого поля задано ненулевое значение, файлы, отсутствующие в целевом образе, игнорируются установщиком и остаются без изменений во время установки исправлений.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-165">If this field is set to a nonzero value, files missing from the target image are ignored by the installer and left unchanged during patching.</span></span> <span data-ttu-id="bb2d2-166">Это позволяет устанавливать исправления без необходимости создания всего образа. требуются только измененные файлы продукта и MSI.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-166">This enables patches to be made without requiring the entire image; only the changed files of the product and the .msi file are required.</span></span> <span data-ttu-id="bb2d2-167">Это может сократить время, необходимое для создания исправления.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-167">This may reduce the time required to generate the patch.</span></span>

> [!Note]  
> <span data-ttu-id="bb2d2-168">Не используйте значение Игноремиссингсркфилес с параметром Трустмси, равным 1, в [таблице свойств](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="bb2d2-168">Do not use the IgnoreMissingSrcFiles value with TrustMsi set to 1 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb2d2-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb2d2-169">Remarks</span></span>

<span data-ttu-id="bb2d2-170">Эта таблица принимает переменные среды в виде путей, начинающихся с Patchwiz.dll версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="bb2d2-170">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 



