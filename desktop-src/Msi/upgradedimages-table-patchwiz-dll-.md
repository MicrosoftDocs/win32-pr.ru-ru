---
description: Таблица Упградедимажес содержит сведения об обновленных образах продукта.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Таблица Упградедимажес (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348955"
---
# <a name="upgradedimages-table-patchwizdll"></a><span data-ttu-id="49853-103">Таблица Упградедимажес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="49853-103">UpgradedImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="49853-104">Таблица Упградедимажес содержит сведения об обновленных образах продукта.</span><span class="sxs-lookup"><span data-stu-id="49853-104">The UpgradedImages table contains information about the upgraded images of the product.</span></span> <span data-ttu-id="49853-105">Обновленный образ должен представлять собой полностью несжатый образ установки последней версии продукта, например административный образ или образ установки без сжатия с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="49853-105">The upgraded image should be a fully uncompressed setup image of the latest version of the product, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="49853-106">Пакет обновления установщик Windows обновляет целевой образ в обновленном образе.</span><span class="sxs-lookup"><span data-stu-id="49853-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span> <span data-ttu-id="49853-107">Таблица Упградедимажес является обязательной в базе данных создания исправлений (файл. PCP) и используется [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="49853-107">The UpgradedImages table is required in the patch creation database (.pcp file) and is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="49853-108">Таблица Упградедимажес, содержащая хотя бы одну запись, необходима в каждой базе данных создания исправлений (файл. PCP).</span><span class="sxs-lookup"><span data-stu-id="49853-108">An UpgradedImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="49853-109">Эта таблица используется [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="49853-109">This table is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="49853-110">Таблица Упградедимажес содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="49853-110">The UpgradedImages table has the following columns.</span></span>



| <span data-ttu-id="49853-111">Столбец</span><span class="sxs-lookup"><span data-stu-id="49853-111">Column</span></span>       | <span data-ttu-id="49853-112">Type</span><span class="sxs-lookup"><span data-stu-id="49853-112">Type</span></span> | <span data-ttu-id="49853-113">Ключ</span><span class="sxs-lookup"><span data-stu-id="49853-113">Key</span></span> | <span data-ttu-id="49853-114">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="49853-114">Nullable</span></span> |
|--------------|------|-----|----------|
| <span data-ttu-id="49853-115">Обновлено</span><span class="sxs-lookup"><span data-stu-id="49853-115">Upgraded</span></span>     | <span data-ttu-id="49853-116">text</span><span class="sxs-lookup"><span data-stu-id="49853-116">text</span></span> | <span data-ttu-id="49853-117">Да</span><span class="sxs-lookup"><span data-stu-id="49853-117">Y</span></span>   | <span data-ttu-id="49853-118">Нет</span><span class="sxs-lookup"><span data-stu-id="49853-118">N</span></span>        |
| <span data-ttu-id="49853-119">мсипас</span><span class="sxs-lookup"><span data-stu-id="49853-119">MsiPath</span></span>      | <span data-ttu-id="49853-120">text</span><span class="sxs-lookup"><span data-stu-id="49853-120">text</span></span> |     | <span data-ttu-id="49853-121">Нет</span><span class="sxs-lookup"><span data-stu-id="49853-121">N</span></span>        |
| <span data-ttu-id="49853-122">патчмсипас</span><span class="sxs-lookup"><span data-stu-id="49853-122">PatchMsiPath</span></span> | <span data-ttu-id="49853-123">text</span><span class="sxs-lookup"><span data-stu-id="49853-123">text</span></span> |     | <span data-ttu-id="49853-124">Да</span><span class="sxs-lookup"><span data-stu-id="49853-124">Y</span></span>        |
| <span data-ttu-id="49853-125">симболпасс</span><span class="sxs-lookup"><span data-stu-id="49853-125">SymbolPaths</span></span>  | <span data-ttu-id="49853-126">text</span><span class="sxs-lookup"><span data-stu-id="49853-126">text</span></span> |     | <span data-ttu-id="49853-127">Да</span><span class="sxs-lookup"><span data-stu-id="49853-127">Y</span></span>        |
| <span data-ttu-id="49853-128">Семейство</span><span class="sxs-lookup"><span data-stu-id="49853-128">Family</span></span>       | <span data-ttu-id="49853-129">text</span><span class="sxs-lookup"><span data-stu-id="49853-129">text</span></span> |     | <span data-ttu-id="49853-130">Нет</span><span class="sxs-lookup"><span data-stu-id="49853-130">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="49853-131">Столбцы</span><span class="sxs-lookup"><span data-stu-id="49853-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="49853-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Обновит</span><span class="sxs-lookup"><span data-stu-id="49853-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="49853-133">Обновленное поле — это произвольный идентификатор для подключения целевых образов к обновленному образу продукта.</span><span class="sxs-lookup"><span data-stu-id="49853-133">The Upgraded field is an arbitrary identifier to connect the target images with an upgraded image of the product.</span></span>

</dd> <dt>

<span data-ttu-id="49853-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>мсипас</span><span class="sxs-lookup"><span data-stu-id="49853-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="49853-135">В этом поле указывается полный путь, включая имя файла, с расположением MSI файла для обновленного образа.</span><span class="sxs-lookup"><span data-stu-id="49853-135">This field specifies the full path, including the file name, to the location of the .msi file for the upgraded image.</span></span> <span data-ttu-id="49853-136">Это расположение исходных файлов для обновленного образа.</span><span class="sxs-lookup"><span data-stu-id="49853-136">This is the location of the source files for the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="49853-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>патчмсипас</span><span class="sxs-lookup"><span data-stu-id="49853-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span></span>
</dt> <dd>

<span data-ttu-id="49853-138">Необязательный Патчмсипас указывает на измененную копию обновленной базы данных установки, которая содержит дополнительную разработку, относящуюся к процессу установки исправления.</span><span class="sxs-lookup"><span data-stu-id="49853-138">The optional patchMsiPath points to a modified copy of the upgraded installation database that contains additional authoring specific to the patch installation process.</span></span> <span data-ttu-id="49853-139">Например, в свойстве [**Patch**](patch.md) были внесены дополнительные диалоговые окна или настраиваемые действия.</span><span class="sxs-lookup"><span data-stu-id="49853-139">For example, additional dialogs or custom actions conditioned on the [**PATCH**](patch.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="49853-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>симболпасс</span><span class="sxs-lookup"><span data-stu-id="49853-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="49853-141">Разделенный точками с запятой список папок для поиска файлов символов, которые могут использоваться для оптимизации создания двоичного исправления.</span><span class="sxs-lookup"><span data-stu-id="49853-141">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="49853-142">Обратите внимание, что поиск в подкаталогах папок, указанных в этом поле, не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49853-142">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="49853-143">Оптимизированное двоичное обновление может быть небольшим.</span><span class="sxs-lookup"><span data-stu-id="49853-143">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="49853-144">Visual C++ должны быть установлены на компьютере, создающем исправление, и использоваться для создания файлов символов.</span><span class="sxs-lookup"><span data-stu-id="49853-144">Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="49853-145">Это поле является необязательным, и установщик создает двоичное исправление, даже если файлы символов не указаны или если файлы символов становятся недоступными для Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="49853-145">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="49853-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Семьи</span><span class="sxs-lookup"><span data-stu-id="49853-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="49853-147">Внешний ключ в [таблицу имажефамилиес](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="49853-147">Foreign key into the [ImageFamilies table](imagefamilies-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="49853-148">Каждый обновленный образ должен принадлежать только одному семейству.</span><span class="sxs-lookup"><span data-stu-id="49853-148">Each upgraded image must belong to only one family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49853-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49853-149">Remarks</span></span>

<span data-ttu-id="49853-150">Хотя каждый обновленный образ можно сгруппировать в отдельное семейство образов, группирование обновленных образов, совместно использующих файлы, может сделать. MSP меньше.</span><span class="sxs-lookup"><span data-stu-id="49853-150">Although each upgraded image can be grouped into a separate image family, grouping upgraded images that share files together may make the .msp smaller.</span></span>

<span data-ttu-id="49853-151">Эта таблица принимает переменные среды в виде путей, начинающихся с Patchwiz.dll версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="49853-151">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 



