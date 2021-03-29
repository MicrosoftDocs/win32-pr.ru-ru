---
description: Эта таблица содержит список файлов, которые будут перемещены или скопированы из указанного исходного каталога в указанный каталог назначения.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Таблица MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818577"
---
# <a name="movefile-table"></a><span data-ttu-id="6d466-103">Таблица MoveFile</span><span class="sxs-lookup"><span data-stu-id="6d466-103">MoveFile Table</span></span>

<span data-ttu-id="6d466-104">Эта таблица содержит список файлов, которые будут перемещены или скопированы из указанного исходного каталога в указанный каталог назначения.</span><span class="sxs-lookup"><span data-stu-id="6d466-104">This table contains a list of files to be moved or copied from a specified source directory to a specified destination directory.</span></span>

<span data-ttu-id="6d466-105">Таблица MoveFile содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="6d466-105">The MoveFile table has the following columns.</span></span>



| <span data-ttu-id="6d466-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="6d466-106">Column</span></span>       | <span data-ttu-id="6d466-107">Type</span><span class="sxs-lookup"><span data-stu-id="6d466-107">Type</span></span>                         | <span data-ttu-id="6d466-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="6d466-108">Key</span></span> | <span data-ttu-id="6d466-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="6d466-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="6d466-110">филекэй</span><span class="sxs-lookup"><span data-stu-id="6d466-110">FileKey</span></span>      | [<span data-ttu-id="6d466-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6d466-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="6d466-112">Да</span><span class="sxs-lookup"><span data-stu-id="6d466-112">Y</span></span>   | <span data-ttu-id="6d466-113">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-113">N</span></span>        |
| <span data-ttu-id="6d466-114">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="6d466-114">Component\_</span></span>  | [<span data-ttu-id="6d466-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6d466-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="6d466-116">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-116">N</span></span>   | <span data-ttu-id="6d466-117">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-117">N</span></span>        |
| <span data-ttu-id="6d466-118">SourceName</span><span class="sxs-lookup"><span data-stu-id="6d466-118">SourceName</span></span>   | [<span data-ttu-id="6d466-119">Text</span><span class="sxs-lookup"><span data-stu-id="6d466-119">Text</span></span>](text.md)             | <span data-ttu-id="6d466-120">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-120">N</span></span>   | <span data-ttu-id="6d466-121">Да</span><span class="sxs-lookup"><span data-stu-id="6d466-121">Y</span></span>        |
| <span data-ttu-id="6d466-122">дестнаме</span><span class="sxs-lookup"><span data-stu-id="6d466-122">DestName</span></span>     | [<span data-ttu-id="6d466-123">Имя файла</span><span class="sxs-lookup"><span data-stu-id="6d466-123">Filename</span></span>](filename.md)     | <span data-ttu-id="6d466-124">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-124">N</span></span>   | <span data-ttu-id="6d466-125">Да</span><span class="sxs-lookup"><span data-stu-id="6d466-125">Y</span></span>        |
| <span data-ttu-id="6d466-126">SourceFolder</span><span class="sxs-lookup"><span data-stu-id="6d466-126">SourceFolder</span></span> | [<span data-ttu-id="6d466-127">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6d466-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="6d466-128">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-128">N</span></span>   | <span data-ttu-id="6d466-129">Да</span><span class="sxs-lookup"><span data-stu-id="6d466-129">Y</span></span>        |
| <span data-ttu-id="6d466-130">DestFolder</span><span class="sxs-lookup"><span data-stu-id="6d466-130">DestFolder</span></span>   | [<span data-ttu-id="6d466-131">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6d466-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="6d466-132">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-132">N</span></span>   | <span data-ttu-id="6d466-133">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-133">N</span></span>        |
| <span data-ttu-id="6d466-134">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d466-134">Options</span></span>      | [<span data-ttu-id="6d466-135">Integer</span><span class="sxs-lookup"><span data-stu-id="6d466-135">Integer</span></span>](integer.md)       | <span data-ttu-id="6d466-136">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-136">N</span></span>   | <span data-ttu-id="6d466-137">Нет</span><span class="sxs-lookup"><span data-stu-id="6d466-137">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6d466-138">Столбцы</span><span class="sxs-lookup"><span data-stu-id="6d466-138">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6d466-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>филекэй</span><span class="sxs-lookup"><span data-stu-id="6d466-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="6d466-140">Первичный ключ, однозначно определяющий определенную запись MoveFile.</span><span class="sxs-lookup"><span data-stu-id="6d466-140">Primary key that uniquely identifies a particular MoveFile record.</span></span>

</dd> <dt>

<span data-ttu-id="6d466-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="6d466-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="6d466-142">Внешний ключ в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="6d466-142">External key into the [Component table](component-table.md).</span></span> <span data-ttu-id="6d466-143">Если компонент, на который ссылается этот ключ, не выбран для установки или удаления, для этой записи MoveFile не выполняются никакие действия.</span><span class="sxs-lookup"><span data-stu-id="6d466-143">If the component referenced by this key is not selected for installation or removal, then no action is taken on this MoveFile entry.</span></span>

</dd> <dt>

<span data-ttu-id="6d466-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span><span class="sxs-lookup"><span data-stu-id="6d466-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span></span>
</dt> <dd>

<span data-ttu-id="6d466-145">Этот столбец содержит Локализуемое имя перемещаемых или копируемых исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="6d466-145">This column contains the localizable name of the source files to be moved or copied.</span></span> <span data-ttu-id="6d466-146">Этот столбец можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="6d466-146">This column may be left blank.</span></span> <span data-ttu-id="6d466-147">См. описание столбца SourceFolder.</span><span class="sxs-lookup"><span data-stu-id="6d466-147">See the description of the SourceFolder column.</span></span> <span data-ttu-id="6d466-148">Это поле должно содержать длинное имя файла и может содержать символы-шаблоны ( \* и?).</span><span class="sxs-lookup"><span data-stu-id="6d466-148">This field must contain a long file name and may contain wildcard characters (\* and ?).</span></span>

</dd> <dt>

<span data-ttu-id="6d466-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>дестнаме</span><span class="sxs-lookup"><span data-stu-id="6d466-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="6d466-150">Этот столбец содержит Локализуемое имя, присваиваемое исходному файлу после его перемещения или копирования.</span><span class="sxs-lookup"><span data-stu-id="6d466-150">This column contains the localizable name to be given to the original file after it is moved or copied.</span></span> <span data-ttu-id="6d466-151">Если это поле пустое, то конечному файлу присваивается то же имя, что и у исходного файла.</span><span class="sxs-lookup"><span data-stu-id="6d466-151">If this field is blank, then the destination file is given the same name as the source file.</span></span>

</dd> <dt>

<span data-ttu-id="6d466-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span><span class="sxs-lookup"><span data-stu-id="6d466-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span></span>
</dt> <dd>

<span data-ttu-id="6d466-153">Этот столбец содержит имя свойства со значением, которое разрешается в полный путь к исходному каталогу.</span><span class="sxs-lookup"><span data-stu-id="6d466-153">This column contains the name of a property having a value that resolves to the full path to the source directory.</span></span> <span data-ttu-id="6d466-154">Если столбец SourceName оставлен пустым, то предполагается, что свойство, названное в столбце SourceFolder, содержит полный путь к самому исходному файлу (включая имя файла).</span><span class="sxs-lookup"><span data-stu-id="6d466-154">If the SourceName column is left blank, then the property named in the SourceFolder column is assumed to contain the full path to the source file itself (including the file name).</span></span>

</dd> <dt>

<span data-ttu-id="6d466-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="6d466-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="6d466-156">Имя свойства, значение которого разрешается в полный путь к целевому каталогу.</span><span class="sxs-lookup"><span data-stu-id="6d466-156">The name of a property whose value resolves to the full path to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="6d466-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Параметры</span><span class="sxs-lookup"><span data-stu-id="6d466-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="6d466-158">Целочисленное значение, определяющее режим работы.</span><span class="sxs-lookup"><span data-stu-id="6d466-158">Integer value specifying the operating mode.</span></span>



| <span data-ttu-id="6d466-159">Константа</span><span class="sxs-lookup"><span data-stu-id="6d466-159">Constant</span></span>                     | <span data-ttu-id="6d466-160">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="6d466-160">Hexadecimal</span></span> | <span data-ttu-id="6d466-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="6d466-161">Decimal</span></span> | <span data-ttu-id="6d466-162">Значение</span><span class="sxs-lookup"><span data-stu-id="6d466-162">Meaning</span></span>               |
|------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="6d466-163">(нет)</span><span class="sxs-lookup"><span data-stu-id="6d466-163">(none)</span></span>                       | <span data-ttu-id="6d466-164">0x000</span><span class="sxs-lookup"><span data-stu-id="6d466-164">0x000</span></span>       | <span data-ttu-id="6d466-165">0</span><span class="sxs-lookup"><span data-stu-id="6d466-165">0</span></span>       | <span data-ttu-id="6d466-166">Скопируйте исходный файл.</span><span class="sxs-lookup"><span data-stu-id="6d466-166">Copy the source file.</span></span> |
| <span data-ttu-id="6d466-167">**мсидбмовефилеоптионсмове**</span><span class="sxs-lookup"><span data-stu-id="6d466-167">**msidbMoveFileOptionsMove**</span></span> | <span data-ttu-id="6d466-168">0x001</span><span class="sxs-lookup"><span data-stu-id="6d466-168">0x001</span></span>       | <span data-ttu-id="6d466-169">1</span><span class="sxs-lookup"><span data-stu-id="6d466-169">1</span></span>       | <span data-ttu-id="6d466-170">Переместите исходный файл.</span><span class="sxs-lookup"><span data-stu-id="6d466-170">Move the source file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d466-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d466-171">Remarks</span></span>

<span data-ttu-id="6d466-172">Если в столбце \* SourceName таблицы MoveFile указан подстановочный знак "", а имя целевого файла указано в столбце дестнаме, то все перемещенные или скопированные файлы сохранили имена в источниках.</span><span class="sxs-lookup"><span data-stu-id="6d466-172">If a "\*" wildcard is entered in the SourceName column of the MoveFile table and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="6d466-173">Эта таблица обрабатывается [действием мовефилес](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="6d466-173">This table is processed by the [MoveFiles action](movefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="6d466-174">Проверка</span><span class="sxs-lookup"><span data-stu-id="6d466-174">Validation</span></span>

<dl>

[<span data-ttu-id="6d466-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="6d466-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6d466-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="6d466-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6d466-177">ICE18</span><span class="sxs-lookup"><span data-stu-id="6d466-177">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="6d466-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="6d466-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="6d466-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="6d466-179">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="6d466-180">ICE85</span><span class="sxs-lookup"><span data-stu-id="6d466-180">ICE85</span></span>](ice85.md)  
</dl>

 

 



