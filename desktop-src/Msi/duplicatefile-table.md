---
description: Таблица Дупликатефиле содержит список файлов, которые должны дублироваться, либо в каталог, отличный от исходного файла, либо в тот же каталог, но с другим именем. Исходный файл должен быть файлом, установленным действием Инсталлфилес.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Таблица Дупликатефиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080921"
---
# <a name="duplicatefile-table"></a><span data-ttu-id="bda37-104">Таблица Дупликатефиле</span><span class="sxs-lookup"><span data-stu-id="bda37-104">DuplicateFile Table</span></span>

<span data-ttu-id="bda37-105">Таблица Дупликатефиле содержит список файлов, которые должны дублироваться, либо в каталог, отличный от исходного файла, либо в тот же каталог, но с другим именем.</span><span class="sxs-lookup"><span data-stu-id="bda37-105">The DuplicateFile table contains a list of files that are to be duplicated, either to a different directory than the original file or to the same directory but with a different name.</span></span> <span data-ttu-id="bda37-106">Исходный файл должен быть файлом, установленным [действием инсталлфилес](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="bda37-106">The original file must be a file installed by the [InstallFiles action](installfiles-action.md).</span></span>

<span data-ttu-id="bda37-107">Таблица Дупликатефиле содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="bda37-107">The DuplicateFile table has the following columns.</span></span>



| <span data-ttu-id="bda37-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="bda37-108">Column</span></span>      | <span data-ttu-id="bda37-109">Type</span><span class="sxs-lookup"><span data-stu-id="bda37-109">Type</span></span>                         | <span data-ttu-id="bda37-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="bda37-110">Key</span></span> | <span data-ttu-id="bda37-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="bda37-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="bda37-112">филекэй</span><span class="sxs-lookup"><span data-stu-id="bda37-112">FileKey</span></span>     | [<span data-ttu-id="bda37-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="bda37-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="bda37-114">Да</span><span class="sxs-lookup"><span data-stu-id="bda37-114">Y</span></span>   | <span data-ttu-id="bda37-115">Нет</span><span class="sxs-lookup"><span data-stu-id="bda37-115">N</span></span>        |
| <span data-ttu-id="bda37-116">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="bda37-116">Component\_</span></span> | [<span data-ttu-id="bda37-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="bda37-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="bda37-118">Нет</span><span class="sxs-lookup"><span data-stu-id="bda37-118">N</span></span>   | <span data-ttu-id="bda37-119">Нет</span><span class="sxs-lookup"><span data-stu-id="bda37-119">N</span></span>        |
| <span data-ttu-id="bda37-120">Файл\_</span><span class="sxs-lookup"><span data-stu-id="bda37-120">File\_</span></span>      | [<span data-ttu-id="bda37-121">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="bda37-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="bda37-122">Нет</span><span class="sxs-lookup"><span data-stu-id="bda37-122">N</span></span>   | <span data-ttu-id="bda37-123">Нет</span><span class="sxs-lookup"><span data-stu-id="bda37-123">N</span></span>        |
| <span data-ttu-id="bda37-124">дестнаме</span><span class="sxs-lookup"><span data-stu-id="bda37-124">DestName</span></span>    | [<span data-ttu-id="bda37-125">Имя файла</span><span class="sxs-lookup"><span data-stu-id="bda37-125">Filename</span></span>](filename.md)     | <span data-ttu-id="bda37-126">Нет</span><span class="sxs-lookup"><span data-stu-id="bda37-126">N</span></span>   | <span data-ttu-id="bda37-127">Да</span><span class="sxs-lookup"><span data-stu-id="bda37-127">Y</span></span>        |
| <span data-ttu-id="bda37-128">DestFolder</span><span class="sxs-lookup"><span data-stu-id="bda37-128">DestFolder</span></span>  | [<span data-ttu-id="bda37-129">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="bda37-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="bda37-130">Нет</span><span class="sxs-lookup"><span data-stu-id="bda37-130">N</span></span>   | <span data-ttu-id="bda37-131">Да</span><span class="sxs-lookup"><span data-stu-id="bda37-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bda37-132">Столбцы</span><span class="sxs-lookup"><span data-stu-id="bda37-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bda37-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>филекэй</span><span class="sxs-lookup"><span data-stu-id="bda37-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="bda37-134">Первичный ключ, нелокализованный токен, идентифицирующий уникальную запись Дупликатефиле.</span><span class="sxs-lookup"><span data-stu-id="bda37-134">A primary key, a non-localized token, identifying a unique DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="bda37-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="bda37-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="bda37-136">Внешний ключ к первому столбцу [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="bda37-136">An external key to the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="bda37-137">Если компонент, идентифицируемый ключом, не выбран для установки или удаления, для этой записи Дупликатефиле не выполняются никакие действия.</span><span class="sxs-lookup"><span data-stu-id="bda37-137">If the component identified by the key is not selected for installation or removal, then no action is taken on this DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="bda37-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="bda37-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="bda37-139">Внешний ключ в [таблице File](file-table.md) , представляющий исходный файл, который должен дублироваться.</span><span class="sxs-lookup"><span data-stu-id="bda37-139">Foreign key into the [File table](file-table.md) representing the original file that is to be duplicated.</span></span>

</dd> <dt>

<span data-ttu-id="bda37-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>дестнаме</span><span class="sxs-lookup"><span data-stu-id="bda37-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="bda37-141">Локализуемое имя, присваиваемое дублированному файлу.</span><span class="sxs-lookup"><span data-stu-id="bda37-141">Localizable name to be given to the duplicate file.</span></span> <span data-ttu-id="bda37-142">Если это поле пустое, то конечному файлу присваивается то же имя, что и у исходного файла.</span><span class="sxs-lookup"><span data-stu-id="bda37-142">If this field is blank, then the destination file is given the same name as the original file.</span></span>

</dd> <dt>

<span data-ttu-id="bda37-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="bda37-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="bda37-144">Имя свойства, которое является полным путем к месту копирования повторяющегося файла.</span><span class="sxs-lookup"><span data-stu-id="bda37-144">Name of a property that is the full path to where the duplicate file is to be copied.</span></span> <span data-ttu-id="bda37-145">Если этот каталог совпадает с каталогом, содержащим исходный файл, а имя предложенного повторяющегося файла совпадает с исходным, то никаких действий не происходит.</span><span class="sxs-lookup"><span data-stu-id="bda37-145">If this directory is the same as the directory containing the original file and the name for the proposed duplicate file is the same as the original, then no action takes place.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bda37-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bda37-146">Remarks</span></span>

<span data-ttu-id="bda37-147">Таблица обрабатывается [действием дупликатефилес](duplicatefiles-action.md) и [действием ремоведупликатефилес](removeduplicatefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="bda37-147">The table is processed by the [DuplicateFiles action](duplicatefiles-action.md) and the [RemoveDuplicateFiles action](removeduplicatefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="bda37-148">Проверка</span><span class="sxs-lookup"><span data-stu-id="bda37-148">Validation</span></span>

<dl>

[<span data-ttu-id="bda37-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="bda37-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="bda37-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="bda37-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="bda37-151">ICE18</span><span class="sxs-lookup"><span data-stu-id="bda37-151">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="bda37-152">ICE32</span><span class="sxs-lookup"><span data-stu-id="bda37-152">ICE32</span></span>](ice32.md)  
</dl>

 

 



