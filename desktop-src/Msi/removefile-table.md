---
description: Таблица Ремовефиле содержит список файлов, которые будут удалены действием Ремовефилес. Установка значения NULL для столбца FileName в этой таблице поддерживает удаление пустых папок.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Таблица Ремовефиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911332"
---
# <a name="removefile-table"></a><span data-ttu-id="2c6a8-104">Таблица Ремовефиле</span><span class="sxs-lookup"><span data-stu-id="2c6a8-104">RemoveFile Table</span></span>

<span data-ttu-id="2c6a8-105">Таблица Ремовефиле содержит список файлов, которые будут удалены [действием ремовефилес](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="2c6a8-105">The RemoveFile table contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span> <span data-ttu-id="2c6a8-106">Установка значения NULL для столбца FileName в этой таблице поддерживает удаление пустых папок.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-106">Setting the FileName column of this table to Null supports the removal of empty folders.</span></span>

<span data-ttu-id="2c6a8-107">Таблица Ремовефиле содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-107">The RemoveFile table has the following columns.</span></span>



| <span data-ttu-id="2c6a8-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="2c6a8-108">Column</span></span>      | <span data-ttu-id="2c6a8-109">Type</span><span class="sxs-lookup"><span data-stu-id="2c6a8-109">Type</span></span>                                     | <span data-ttu-id="2c6a8-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="2c6a8-110">Key</span></span> | <span data-ttu-id="2c6a8-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="2c6a8-111">Nullable</span></span> |
|-------------|------------------------------------------|-----|----------|
| <span data-ttu-id="2c6a8-112">филекэй</span><span class="sxs-lookup"><span data-stu-id="2c6a8-112">FileKey</span></span>     | [<span data-ttu-id="2c6a8-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="2c6a8-113">Identifier</span></span>](identifier.md)             | <span data-ttu-id="2c6a8-114">Да</span><span class="sxs-lookup"><span data-stu-id="2c6a8-114">Y</span></span>   | <span data-ttu-id="2c6a8-115">Нет</span><span class="sxs-lookup"><span data-stu-id="2c6a8-115">N</span></span>        |
| <span data-ttu-id="2c6a8-116">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="2c6a8-116">Component\_</span></span> | [<span data-ttu-id="2c6a8-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="2c6a8-117">Identifier</span></span>](identifier.md)             | <span data-ttu-id="2c6a8-118">Нет</span><span class="sxs-lookup"><span data-stu-id="2c6a8-118">N</span></span>   | <span data-ttu-id="2c6a8-119">Нет</span><span class="sxs-lookup"><span data-stu-id="2c6a8-119">N</span></span>        |
| <span data-ttu-id="2c6a8-120">FileName</span><span class="sxs-lookup"><span data-stu-id="2c6a8-120">FileName</span></span>    | [<span data-ttu-id="2c6a8-121">вилдкардфиленаме</span><span class="sxs-lookup"><span data-stu-id="2c6a8-121">WildCardFilename</span></span>](wildcardfilename.md) | <span data-ttu-id="2c6a8-122">Нет</span><span class="sxs-lookup"><span data-stu-id="2c6a8-122">N</span></span>   | <span data-ttu-id="2c6a8-123">Да</span><span class="sxs-lookup"><span data-stu-id="2c6a8-123">Y</span></span>        |
| <span data-ttu-id="2c6a8-124">дирпроперти</span><span class="sxs-lookup"><span data-stu-id="2c6a8-124">DirProperty</span></span> | [<span data-ttu-id="2c6a8-125">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="2c6a8-125">Identifier</span></span>](identifier.md)             | <span data-ttu-id="2c6a8-126">Нет</span><span class="sxs-lookup"><span data-stu-id="2c6a8-126">N</span></span>   | <span data-ttu-id="2c6a8-127">Нет</span><span class="sxs-lookup"><span data-stu-id="2c6a8-127">N</span></span>        |
| <span data-ttu-id="2c6a8-128">InstallMode</span><span class="sxs-lookup"><span data-stu-id="2c6a8-128">InstallMode</span></span> | [<span data-ttu-id="2c6a8-129">Integer</span><span class="sxs-lookup"><span data-stu-id="2c6a8-129">Integer</span></span>](integer.md)                   | <span data-ttu-id="2c6a8-130">Нет</span><span class="sxs-lookup"><span data-stu-id="2c6a8-130">N</span></span>   | <span data-ttu-id="2c6a8-131">Нет</span><span class="sxs-lookup"><span data-stu-id="2c6a8-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2c6a8-132">Столбцы</span><span class="sxs-lookup"><span data-stu-id="2c6a8-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2c6a8-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>филекэй</span><span class="sxs-lookup"><span data-stu-id="2c6a8-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="2c6a8-134">Первичный ключ, используемый для распознавания этой конкретной записи таблицы.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-134">Primary key used to identify this particular table entry.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a8-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="2c6a8-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="2c6a8-136">Внешний ключ первый столбец [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="2c6a8-136">External key the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="2c6a8-137">Это поле ссылается на компонент, который управляет удаляемым файлом.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-137">This field references the component that controls the file to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a8-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Файлов</span><span class="sxs-lookup"><span data-stu-id="2c6a8-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="2c6a8-139">Этот столбец содержит Локализуемое имя удаляемого файла.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-139">This column contains the localizable name of the file to be removed.</span></span> <span data-ttu-id="2c6a8-140">Если этот столбец имеет значение null, то указанная папка будет удалена, если она пуста.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-140">If this column is null, then the specified folder will be removed if it is empty.</span></span> <span data-ttu-id="2c6a8-141">Все файлы, соответствующие подстановочному знаку, будут удалены из указанного каталога.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-141">All of the files that match the wildcard will be removed from the specified directory.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a8-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>дирпроперти</span><span class="sxs-lookup"><span data-stu-id="2c6a8-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="2c6a8-143">Имя свойства, значение которого предполагается преобразовать в полный путь к папке удаляемого файла.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-143">Name of a property whose value is assumed to resolve to the full path to the folder of the file to be removed.</span></span> <span data-ttu-id="2c6a8-144">Свойство может быть именем каталога в [таблице Directory](directory-table.md), свойством, заданным [таблицей аппсеарч](appsearch-table.md), или любым другим свойством, представляющим полный путь.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-144">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a8-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span><span class="sxs-lookup"><span data-stu-id="2c6a8-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span></span>
</dt> <dd>

<span data-ttu-id="2c6a8-146">Должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-146">Must be one of the following values.</span></span>



| <span data-ttu-id="2c6a8-147">Константа</span><span class="sxs-lookup"><span data-stu-id="2c6a8-147">Constant</span></span>                                | <span data-ttu-id="2c6a8-148">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="2c6a8-148">Hexadecimal</span></span> | <span data-ttu-id="2c6a8-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="2c6a8-149">Decimal</span></span> | <span data-ttu-id="2c6a8-150">Описание</span><span class="sxs-lookup"><span data-stu-id="2c6a8-150">Description</span></span>                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6a8-151">**мсидбремовефилеинсталлмодеонинсталл**</span><span class="sxs-lookup"><span data-stu-id="2c6a8-151">**msidbRemoveFileInstallModeOnInstall**</span></span> | <span data-ttu-id="2c6a8-152">0x001</span><span class="sxs-lookup"><span data-stu-id="2c6a8-152">0x001</span></span>       | <span data-ttu-id="2c6a8-153">1</span><span class="sxs-lookup"><span data-stu-id="2c6a8-153">1</span></span>       | <span data-ttu-id="2c6a8-154">Удаляйте только при установке связанного компонента (Мсиинсталлстателокал или Мсиинсталлстатесаурце).</span><span class="sxs-lookup"><span data-stu-id="2c6a8-154">Remove only when the associated component is being installed (msiInstallStateLocal or msiInstallStateSource).</span></span> |
| <span data-ttu-id="2c6a8-155">**мсидбремовефилеинсталлмодеонремове**</span><span class="sxs-lookup"><span data-stu-id="2c6a8-155">**msidbRemoveFileInstallModeOnRemove**</span></span>  | <span data-ttu-id="2c6a8-156">0x002</span><span class="sxs-lookup"><span data-stu-id="2c6a8-156">0x002</span></span>       | <span data-ttu-id="2c6a8-157">2</span><span class="sxs-lookup"><span data-stu-id="2c6a8-157">2</span></span>       | <span data-ttu-id="2c6a8-158">Удаляется только при удалении связанного компонента (Мсиинсталлстатеабсент).</span><span class="sxs-lookup"><span data-stu-id="2c6a8-158">Remove only when the associated component is being removed (msiInstallStateAbsent).</span></span>                           |
| <span data-ttu-id="2c6a8-159">**мсидбремовефилеинсталлмодеонбос**</span><span class="sxs-lookup"><span data-stu-id="2c6a8-159">**msidbRemoveFileInstallModeOnBoth**</span></span>    | <span data-ttu-id="2c6a8-160">0x003</span><span class="sxs-lookup"><span data-stu-id="2c6a8-160">0x003</span></span>       | <span data-ttu-id="2c6a8-161">3</span><span class="sxs-lookup"><span data-stu-id="2c6a8-161">3</span></span>       | <span data-ttu-id="2c6a8-162">Удалите один из указанных выше вариантов.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-162">Remove in either of the above cases.</span></span>                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c6a8-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c6a8-163">Remarks</span></span>

<span data-ttu-id="2c6a8-164">Ссылки на файлы в этой таблице обрабатываются [действием ремовефилес](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="2c6a8-164">The file references in this table are processed by the [RemoveFiles action](removefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="2c6a8-165">Проверка</span><span class="sxs-lookup"><span data-stu-id="2c6a8-165">Validation</span></span>

<dl>

[<span data-ttu-id="2c6a8-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="2c6a8-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2c6a8-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="2c6a8-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2c6a8-168">ICE18</span><span class="sxs-lookup"><span data-stu-id="2c6a8-168">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="2c6a8-169">ICE32</span><span class="sxs-lookup"><span data-stu-id="2c6a8-169">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2c6a8-170">ICE45</span><span class="sxs-lookup"><span data-stu-id="2c6a8-170">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="2c6a8-171">ICE64</span><span class="sxs-lookup"><span data-stu-id="2c6a8-171">ICE64</span></span>](ice64.md)  
</dl>

 

 



