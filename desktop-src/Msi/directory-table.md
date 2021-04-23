---
description: В таблице Directory указана структура каталога для продукта. Каждая строка таблицы указывает каталог как в исходном, так и на целевом.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Таблица каталога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998818"
---
# <a name="directory-table"></a><span data-ttu-id="fb4da-104">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="fb4da-104">Directory Table</span></span>

<span data-ttu-id="fb4da-105">В таблице Directory указана структура каталога для продукта.</span><span class="sxs-lookup"><span data-stu-id="fb4da-105">The Directory table specifies the directory layout for the product.</span></span> <span data-ttu-id="fb4da-106">Каждая строка таблицы указывает каталог как в исходном, так и на целевом.</span><span class="sxs-lookup"><span data-stu-id="fb4da-106">Each row of the table indicates a directory both at the source and the target.</span></span>

<span data-ttu-id="fb4da-107">Таблица Directory содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="fb4da-107">The Directory table has the following columns.</span></span>



| <span data-ttu-id="fb4da-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="fb4da-108">Column</span></span>            | <span data-ttu-id="fb4da-109">Type</span><span class="sxs-lookup"><span data-stu-id="fb4da-109">Type</span></span>                         | <span data-ttu-id="fb4da-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="fb4da-110">Key</span></span> | <span data-ttu-id="fb4da-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="fb4da-111">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="fb4da-112">Каталог</span><span class="sxs-lookup"><span data-stu-id="fb4da-112">Directory</span></span>         | [<span data-ttu-id="fb4da-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="fb4da-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="fb4da-114">Да</span><span class="sxs-lookup"><span data-stu-id="fb4da-114">Y</span></span>   | <span data-ttu-id="fb4da-115">Нет</span><span class="sxs-lookup"><span data-stu-id="fb4da-115">N</span></span>        |
| <span data-ttu-id="fb4da-116">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="fb4da-116">Directory\_Parent</span></span> | [<span data-ttu-id="fb4da-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="fb4da-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="fb4da-118">Нет</span><span class="sxs-lookup"><span data-stu-id="fb4da-118">N</span></span>   | <span data-ttu-id="fb4da-119">Да</span><span class="sxs-lookup"><span data-stu-id="fb4da-119">Y</span></span>        |
| <span data-ttu-id="fb4da-120">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="fb4da-120">DefaultDir</span></span>        | [<span data-ttu-id="fb4da-121">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="fb4da-121">DefaultDir</span></span>](defaultdir.md) | <span data-ttu-id="fb4da-122">Нет</span><span class="sxs-lookup"><span data-stu-id="fb4da-122">N</span></span>   | <span data-ttu-id="fb4da-123">Нет</span><span class="sxs-lookup"><span data-stu-id="fb4da-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fb4da-124">Столбцы</span><span class="sxs-lookup"><span data-stu-id="fb4da-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fb4da-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Каталоги</span><span class="sxs-lookup"><span data-stu-id="fb4da-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span></span>
</dt> <dd>

<span data-ttu-id="fb4da-126">Столбец Directory содержит уникальный идентификатор для каталога или пути к каталогу.</span><span class="sxs-lookup"><span data-stu-id="fb4da-126">The Directory column contains a unique identifier for a directory or directory path.</span></span> <span data-ttu-id="fb4da-127">Этот столбец может содержать имя свойства, для которого задан полный путь к целевому каталогу.</span><span class="sxs-lookup"><span data-stu-id="fb4da-127">This column can contain the name of a property that is set to the full path of a target directory.</span></span> <span data-ttu-id="fb4da-128">Если этот столбец содержит свойство, то целевой каталог принимает имя, указанное в столбце Дефаултдир, и принимает родительский каталог, указанный в \_ родительском столбце каталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-128">If this column contains a property, the target directory takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="fb4da-129">Исходный каталог всегда принимает имя, указанное в столбце Дефаултдир, и принимает родительский каталог, указанный в \_ столбце родительский каталог.</span><span class="sxs-lookup"><span data-stu-id="fb4da-129">The source directory always takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="fb4da-130">Если \_ родительский столбец каталога либо равен null, либо равен значению столбца каталога, то столбец Directory представляет корневой целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="fb4da-130">If the Directory\_Parent column is either null or equal to the value of the Directory column, the Directory column represents a root target directory.</span></span> <span data-ttu-id="fb4da-131">В таблице Directory может быть указан только один корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="fb4da-131">Only one root directory may be specified in the Directory table.</span></span>

</dd> <dt>

<span data-ttu-id="fb4da-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="fb4da-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directory\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="fb4da-133">Этот столбец является ссылкой на родительский каталог каталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-133">This column is a reference to the directory's parent directory.</span></span> <span data-ttu-id="fb4da-134">Запись, имеющая \_ родительский столбец каталога, равная null или равная столбцу каталога, представляет корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="fb4da-134">A record that has a Directory\_Parent column equal to null or equal to the Directory column represents a root directory.</span></span> <span data-ttu-id="fb4da-135">Полный путь к родительскому каталогу разрешается по ссылке в \_ родительском столбце каталога. это внешний ключ в столбце каталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-135">The full path of the parent directory is resolved by reference in the Directory\_Parent column is an external key into the Directory column.</span></span> <span data-ttu-id="fb4da-136">Например, если папка имеет родительский каталог с именем ПДИР, родительский каталог ПДИР указывается в \_ родительском столбце каталога строки с пдир в столбце Directory.</span><span class="sxs-lookup"><span data-stu-id="fb4da-136">For example, if a folder has a parent directory named PDIR, the parent directory of PDIR is given in the Directory\_Parent column of the row with PDIR in the Directory column.</span></span>

</dd> <dt>

<span data-ttu-id="fb4da-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>дефаултдир</span><span class="sxs-lookup"><span data-stu-id="fb4da-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span></span>
</dt> <dd>

<span data-ttu-id="fb4da-138">Столбец Дефаултдир содержит имя каталога (локализуемое) в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="fb4da-138">The DefaultDir column contains the directory's name (localizable)under the parent directory.</span></span> <span data-ttu-id="fb4da-139">По умолчанию это имя целевого и исходного каталогов.</span><span class="sxs-lookup"><span data-stu-id="fb4da-139">By default, this is the name of both the target and source directories.</span></span> <span data-ttu-id="fb4da-140">Чтобы указать разные имена исходного и целевого каталогов, разделите имена целевых и исходных файлов двоеточием следующим образом: \[ TargetName \] : \[ SourceName \] .</span><span class="sxs-lookup"><span data-stu-id="fb4da-140">To specify different source and target directory names, separate the target and source names with a colon as follows: \[targetname\]:\[sourcename\].</span></span>

<span data-ttu-id="fb4da-141">Если значение родительского столбца каталога равно \_ null или равно столбцу каталога, то в столбце дефаултдир указывается имя корневого исходного каталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-141">If the value of the Directory\_Parent column is null or is equal to the Directory column, the DefaultDir column specifies the name of a root source directory.</span></span>

<span data-ttu-id="fb4da-142">Для некорневого исходного каталога точка (.), указанная в столбце Дефаултдир для имени исходного каталога или имени целевого каталога, указывает, что каталог должен находиться в родительском каталоге без подкаталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-142">For a non-root source directory, a period (.) entered in the DefaultDir column for the source directory name or the target directory name indicates the directory should be located in its parent directory without a subdirectory.</span></span>

<span data-ttu-id="fb4da-143">Имена каталогов в этом столбце могут быть отформатированы как пары длинных имен коротких имен файлов \| .</span><span class="sxs-lookup"><span data-stu-id="fb4da-143">The directory names in this column may be formatted as short filename \| long filename pairs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb4da-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb4da-144">Remarks</span></span>

<span data-ttu-id="fb4da-145">Каждая запись в таблице представляет каталог как в исходном, так и в целевом изображениях.</span><span class="sxs-lookup"><span data-stu-id="fb4da-145">Each record in the table represents a directory in both the source and the destination images.</span></span> <span data-ttu-id="fb4da-146">Таблица каталогов должна указывать один корневой каталог со значением столбца каталога, равным свойству [**targetDir**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="fb4da-146">The Directory table must specify a single root directory with a Directory column value equal to the [**TARGETDIR**](targetdir.md) property.</span></span>

<span data-ttu-id="fb4da-147">Для [административной установки](administrative-installation.md)установите административный образ в корневой каталог targetDir и используйте имена исходных каталогов для разрешения целевых каталогов.</span><span class="sxs-lookup"><span data-stu-id="fb4da-147">For an [administrative installation](administrative-installation.md), install the administrative image into the root directory named TARGETDIR and use the source directory names to resolve the target directories.</span></span>

<span data-ttu-id="fb4da-148">Примечание. установщик устанавливает ряд стандартных [свойств](properties.md) для путей к системным папкам.</span><span class="sxs-lookup"><span data-stu-id="fb4da-148">Note the installer sets a number of standard [properties](properties.md) to system folder paths.</span></span> <span data-ttu-id="fb4da-149">Список свойств, для которых заданы системные папки, см. в [справочнике по свойствам](property-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="fb4da-149">See the [Property Reference](property-reference.md) for a list of the properties that are set to system folders.</span></span>

<span data-ttu-id="fb4da-150">Разрешение каталога выполняется во время [действия костфинализе](costfinalize-action.md) и выполняется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="fb4da-150">Directory resolution is performed during the [CostFinalize action](costfinalize-action.md) and is done as follows:</span></span>

### <a name="root-destination-directory"></a><span data-ttu-id="fb4da-151">Корневой каталог назначения</span><span class="sxs-lookup"><span data-stu-id="fb4da-151">Root Destination Directory</span></span>

<span data-ttu-id="fb4da-152">Может существовать только один корневой каталог назначения.</span><span class="sxs-lookup"><span data-stu-id="fb4da-152">There may only be a single root destination directory.</span></span> <span data-ttu-id="fb4da-153">Чтобы указать корневой каталог назначения, задайте для столбца каталога значение свойства [**targetDir**](targetdir.md) , а для столбца дефаултдир — значение свойства [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="fb4da-153">To specify the root destination directory, set the Directory column to the [**TARGETDIR**](targetdir.md) property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="fb4da-154">Если определено свойство **targetDir** , целевой каталог разрешается в значение свойства.</span><span class="sxs-lookup"><span data-stu-id="fb4da-154">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="fb4da-155">Если свойство **targetDir** не определено, для разрешения пути используется свойство [**рутдриве**](rootdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="fb4da-155">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span>

### <a name="root-source-directory"></a><span data-ttu-id="fb4da-156">Корневой исходный каталог</span><span class="sxs-lookup"><span data-stu-id="fb4da-156">Root Source Directory</span></span>

<span data-ttu-id="fb4da-157">Значение столбца Дефаултдир для записи корневого каталога должно быть установлено в свойство [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="fb4da-157">The value of the DefaultDir column for the root directory entry must be set to the [**SourceDir**](sourcedir.md) property.</span></span>

### <a name="non-root-destination-directories"></a><span data-ttu-id="fb4da-158">Некорневые каталоги назначения</span><span class="sxs-lookup"><span data-stu-id="fb4da-158">Non-root Destination Directories</span></span>

<span data-ttu-id="fb4da-159">Значение каталога для некорневого каталога также интерпретируется как имя свойства, определяющего расположение назначения.</span><span class="sxs-lookup"><span data-stu-id="fb4da-159">The Directory value for a non-root directory is also interpreted as the name of a property defining the location of the destination.</span></span> <span data-ttu-id="fb4da-160">Если свойство определено, целевой каталог разрешается в значение свойства.</span><span class="sxs-lookup"><span data-stu-id="fb4da-160">If the property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="fb4da-161">Если свойство не определено, конечный каталог разрешается в подкаталог, находящиеся под разрешенным целевым каталогом для \_ родительской записи каталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-161">If the property is not defined, the destination directory is resolved to a subdirectory beneath the resolved destination directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="fb4da-162">Значение Дефаултдир определяет имя подкаталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-162">The DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="non-root-source-directories"></a><span data-ttu-id="fb4da-163">Некорневые каталоги исходных файлов</span><span class="sxs-lookup"><span data-stu-id="fb4da-163">Non-root Source Directories</span></span>

<span data-ttu-id="fb4da-164">Исходный каталог для некорневого каталога разрешается в подкаталог разрешенного исходного каталога для \_ родительской записи каталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-164">The source directory for a non-root directory is resolved to a subdirectory of the resolved source directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="fb4da-165">Опять же, значение Дефаултдир определяет имя подкаталога.</span><span class="sxs-lookup"><span data-stu-id="fb4da-165">Again, the DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="short-or-long-file-names"></a><span data-ttu-id="fb4da-166">Короткие или длинные имена файлов</span><span class="sxs-lookup"><span data-stu-id="fb4da-166">Short or Long File Names</span></span>

<span data-ttu-id="fb4da-167">При разрешении целевых каталогов используются короткие имена файлов, указанные в столбце Дефаултдир, если задано свойство [**шортфиленамес**](shortfilenames.md) или том, на котором находится каталог, не поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="fb4da-167">When resolving destination directories, the short file names specified in the DefaultDir column are used if either the [**SHORTFILENAMES**](shortfilenames.md) property is set or the volume the directory is located on does not support long file names.</span></span> <span data-ttu-id="fb4da-168">В противном случае используется длинное имя файла.</span><span class="sxs-lookup"><span data-stu-id="fb4da-168">Otherwise, the long file name is used.</span></span>

<span data-ttu-id="fb4da-169">Обратите внимание, что когда каталоги разрешаются во время действия Костфинализе, ключи в таблице Directory становятся [свойствами](properties.md) , для которых заданы пути к каталогам.</span><span class="sxs-lookup"><span data-stu-id="fb4da-169">Note that when the directories are resolved during the CostFinalize action, the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span>

[<span data-ttu-id="fb4da-170">Таблица Креатефолдер</span><span class="sxs-lookup"><span data-stu-id="fb4da-170">CreateFolder Table</span></span>](createfolder-table.md)

<span data-ttu-id="fb4da-171">Сведения о создании пустых папок во время установки см. в разделе [Креатефолдер Table](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="fb4da-171">For creating empty folders during an installation, see [CreateFolder Table](createfolder-table.md).</span></span>

[<span data-ttu-id="fb4da-172">Использование таблицы Directory</span><span class="sxs-lookup"><span data-stu-id="fb4da-172">Using the Directory Table</span></span>](using-the-directory-table.md)

<span data-ttu-id="fb4da-173">Дополнительные сведения о таблице Directory, включая примеры, см. [в разделе Использование таблицы Directory](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="fb4da-173">For more information about the Directory table, including samples, see [Using the Directory Table](using-the-directory-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="fb4da-174">Проверка</span><span class="sxs-lookup"><span data-stu-id="fb4da-174">Validation</span></span>

<dl>

[<span data-ttu-id="fb4da-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="fb4da-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fb4da-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="fb4da-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fb4da-177">ICE07</span><span class="sxs-lookup"><span data-stu-id="fb4da-177">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="fb4da-178">ICE30</span><span class="sxs-lookup"><span data-stu-id="fb4da-178">ICE30</span></span>](ice30.md)  
[<span data-ttu-id="fb4da-179">ICE32</span><span class="sxs-lookup"><span data-stu-id="fb4da-179">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="fb4da-180">ICE38</span><span class="sxs-lookup"><span data-stu-id="fb4da-180">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="fb4da-181">ICE46</span><span class="sxs-lookup"><span data-stu-id="fb4da-181">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="fb4da-182">ICE48</span><span class="sxs-lookup"><span data-stu-id="fb4da-182">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="fb4da-183">ICE56</span><span class="sxs-lookup"><span data-stu-id="fb4da-183">ICE56</span></span>](ice56.md)  
[<span data-ttu-id="fb4da-184">ICE57</span><span class="sxs-lookup"><span data-stu-id="fb4da-184">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="fb4da-185">ICE64</span><span class="sxs-lookup"><span data-stu-id="fb4da-185">ICE64</span></span>](ice64.md)  
[<span data-ttu-id="fb4da-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="fb4da-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="fb4da-187">ICE90</span><span class="sxs-lookup"><span data-stu-id="fb4da-187">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="fb4da-188">ICE91</span><span class="sxs-lookup"><span data-stu-id="fb4da-188">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="fb4da-189">ICE99</span><span class="sxs-lookup"><span data-stu-id="fb4da-189">ICE99</span></span>](ice99.md)  
</dl>

 

 



