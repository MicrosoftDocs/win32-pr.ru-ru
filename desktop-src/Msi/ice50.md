---
description: ICE50 проверяет, что значки ярлыков отображаются правильно и соответствуют их расширению целевого файла.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999108"
---
# <a name="ice50"></a><span data-ttu-id="e1f90-103">ICE50</span><span class="sxs-lookup"><span data-stu-id="e1f90-103">ICE50</span></span>

<span data-ttu-id="e1f90-104">ICE50 проверяет, что значки ярлыков отображаются правильно и соответствуют их расширению целевого файла.</span><span class="sxs-lookup"><span data-stu-id="e1f90-104">ICE50 checks that shortcut icons are specified to display correctly and match their target file's extension.</span></span>

## <a name="result"></a><span data-ttu-id="e1f90-105">Результат</span><span class="sxs-lookup"><span data-stu-id="e1f90-105">Result</span></span>

<span data-ttu-id="e1f90-106">ICE50 отправляет сообщение об ошибке, если расширение файла значка и целевого объекта не совпадает.</span><span class="sxs-lookup"><span data-stu-id="e1f90-106">ICE50 posts an error message if the extension of the icon and target files do not match.</span></span> <span data-ttu-id="e1f90-107">ICE50 отправляет предупреждение, если значки хранятся в файлах, которые не имеют расширения EXE или ICO.</span><span class="sxs-lookup"><span data-stu-id="e1f90-107">ICE50 posts a warning if icons are stored in files that do not have an .exe or .ico extension.</span></span>

## <a name="example"></a><span data-ttu-id="e1f90-108">Пример</span><span class="sxs-lookup"><span data-stu-id="e1f90-108">Example</span></span>

<span data-ttu-id="e1f90-109">ICE50 сообщает об ошибке в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="e1f90-109">ICE50 reports the following error for the example shown.</span></span>



| <span data-ttu-id="e1f90-110">Ошибка или предупреждение ICE50</span><span class="sxs-lookup"><span data-stu-id="e1f90-110">ICE50 error or warning</span></span>                                                                                                              | <span data-ttu-id="e1f90-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e1f90-111">Description</span></span>                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f90-112">Расширение значка "Icon2. dat" для ярлыка "Shortcut2" не соответствует расширению файла ключа для компонента "Component2".</span><span class="sxs-lookup"><span data-stu-id="e1f90-112">The extension of Icon 'Icon2.dat' for Shortcut 'Shortcut2' does not match the extension of the Key File for component 'Component2'.</span></span> | <span data-ttu-id="e1f90-113">Если расширения значка и целевого файла не совпадают, при объявлении компонента ярлык не будет иметь правильное контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="e1f90-113">If the extensions of the icon and the target file do not match, the shortcut will not have the correct context menu when the component is advertised.</span></span> <span data-ttu-id="e1f90-114">Чтобы устранить эту ошибку, переименуйте значок в соответствии с расширением целевого файла.</span><span class="sxs-lookup"><span data-stu-id="e1f90-114">To fix this error, rename the icon to match the extension of the target file.</span></span><br/> |
| <span data-ttu-id="e1f90-115">Расширение значка "Icon1.bat" для ярлыка "Shortcut1" не является "exe" или "ICO".</span><span class="sxs-lookup"><span data-stu-id="e1f90-115">The extension of Icon 'Icon1.bat' for Shortcut 'Shortcut1' is not "exe" or "ico".</span></span> <span data-ttu-id="e1f90-116">Значок будет отображаться неправильно.</span><span class="sxs-lookup"><span data-stu-id="e1f90-116">The Icon will not be displayed correctly.</span></span>         | <span data-ttu-id="e1f90-117">Не все версии оболочки правильно отображают значки, хранящиеся в файлах, у которых нет расширений "exe" или "ICO".</span><span class="sxs-lookup"><span data-stu-id="e1f90-117">Not all versions of the shell correctly display icons stored in files that do not have extensions of "exe" or "ico".</span></span> <span data-ttu-id="e1f90-118">Чтобы устранить это предупреждение, переименуйте значок с расширением "exe" или "ICO".</span><span class="sxs-lookup"><span data-stu-id="e1f90-118">To fix this warning, rename the icon have an extension of "exe" or "ico".</span></span><br/>                                      |



 

<span data-ttu-id="e1f90-119">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1f90-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="e1f90-120">Файл</span><span class="sxs-lookup"><span data-stu-id="e1f90-120">File</span></span>  | <span data-ttu-id="e1f90-121">FileName</span><span class="sxs-lookup"><span data-stu-id="e1f90-121">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="e1f90-122">Файл1</span><span class="sxs-lookup"><span data-stu-id="e1f90-122">File1</span></span> | <span data-ttu-id="e1f90-123">File1.bat</span><span class="sxs-lookup"><span data-stu-id="e1f90-123">File1.bat</span></span> |
| <span data-ttu-id="e1f90-124">Файл2</span><span class="sxs-lookup"><span data-stu-id="e1f90-124">File2</span></span> | <span data-ttu-id="e1f90-125">File2.pl</span><span class="sxs-lookup"><span data-stu-id="e1f90-125">File2.pl</span></span>  |



 

<span data-ttu-id="e1f90-126">[Таблица компонентов](feature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1f90-126">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="e1f90-127">Функция</span><span class="sxs-lookup"><span data-stu-id="e1f90-127">Feature</span></span>  |
|----------|
| <span data-ttu-id="e1f90-128">Feature1</span><span class="sxs-lookup"><span data-stu-id="e1f90-128">Feature1</span></span> |



 

<span data-ttu-id="e1f90-129">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1f90-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="e1f90-130">Компонент</span><span class="sxs-lookup"><span data-stu-id="e1f90-130">Component</span></span>  | <span data-ttu-id="e1f90-131">Путь</span><span class="sxs-lookup"><span data-stu-id="e1f90-131">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="e1f90-132">Component1</span><span class="sxs-lookup"><span data-stu-id="e1f90-132">Component1</span></span> | <span data-ttu-id="e1f90-133">Файл1</span><span class="sxs-lookup"><span data-stu-id="e1f90-133">File1</span></span>   |
| <span data-ttu-id="e1f90-134">Component2</span><span class="sxs-lookup"><span data-stu-id="e1f90-134">Component2</span></span> | <span data-ttu-id="e1f90-135">Файл2</span><span class="sxs-lookup"><span data-stu-id="e1f90-135">File2</span></span>   |



 

[<span data-ttu-id="e1f90-136">Таблица значков</span><span class="sxs-lookup"><span data-stu-id="e1f90-136">Icon Table</span></span>](icon-table.md)



| <span data-ttu-id="e1f90-137">Имя</span><span class="sxs-lookup"><span data-stu-id="e1f90-137">Name</span></span>      | <span data-ttu-id="e1f90-138">Данные</span><span class="sxs-lookup"><span data-stu-id="e1f90-138">Data</span></span>            |
|-----------|-----------------|
| <span data-ttu-id="e1f90-139">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="e1f90-139">Icon1.bat</span></span> | <span data-ttu-id="e1f90-140">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="e1f90-140">\[Binary Data\]</span></span> |
| <span data-ttu-id="e1f90-141">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="e1f90-141">Icon2.dat</span></span> | <span data-ttu-id="e1f90-142">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="e1f90-142">\[Binary Data\]</span></span> |



 

<span data-ttu-id="e1f90-143">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1f90-143">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="e1f90-144">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="e1f90-144">Shortcut</span></span>  | <span data-ttu-id="e1f90-145">Компонент</span><span class="sxs-lookup"><span data-stu-id="e1f90-145">Component</span></span>  | <span data-ttu-id="e1f90-146">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="e1f90-146">Target</span></span>   | <span data-ttu-id="e1f90-147">Значок\_</span><span class="sxs-lookup"><span data-stu-id="e1f90-147">Icon\_</span></span>    |
|-----------|------------|----------|-----------|
| <span data-ttu-id="e1f90-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="e1f90-148">Shortcut1</span></span> | <span data-ttu-id="e1f90-149">Component1</span><span class="sxs-lookup"><span data-stu-id="e1f90-149">Component1</span></span> | <span data-ttu-id="e1f90-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="e1f90-150">Feature1</span></span> | <span data-ttu-id="e1f90-151">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="e1f90-151">Icon1.bat</span></span> |
| <span data-ttu-id="e1f90-152">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="e1f90-152">Shortcut2</span></span> | <span data-ttu-id="e1f90-153">Component2</span><span class="sxs-lookup"><span data-stu-id="e1f90-153">Component2</span></span> | <span data-ttu-id="e1f90-154">Feature1</span><span class="sxs-lookup"><span data-stu-id="e1f90-154">Feature1</span></span> | <span data-ttu-id="e1f90-155">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="e1f90-155">Icon2.dat</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e1f90-156">См. также</span><span class="sxs-lookup"><span data-stu-id="e1f90-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1f90-157">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="e1f90-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




