---
description: Таблица Ремовеинифиле содержит сведения, которые необходимо удалить из ini-файла приложения.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Таблица Ремовеинифиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664541"
---
# <a name="removeinifile-table"></a><span data-ttu-id="e7b62-103">Таблица Ремовеинифиле</span><span class="sxs-lookup"><span data-stu-id="e7b62-103">RemoveIniFile Table</span></span>

<span data-ttu-id="e7b62-104">Таблица Ремовеинифиле содержит сведения, которые необходимо удалить из ini-файла приложения.</span><span class="sxs-lookup"><span data-stu-id="e7b62-104">The RemoveIniFile table contains the information an application needs to delete from a .ini file.</span></span>

<span data-ttu-id="e7b62-105">Таблица Ремовеинифиле содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="e7b62-105">The RemoveIniFile table has the following columns.</span></span>



| <span data-ttu-id="e7b62-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="e7b62-106">Column</span></span>        | <span data-ttu-id="e7b62-107">Type</span><span class="sxs-lookup"><span data-stu-id="e7b62-107">Type</span></span>                         | <span data-ttu-id="e7b62-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="e7b62-108">Key</span></span> | <span data-ttu-id="e7b62-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="e7b62-109">Nullable</span></span> |
|---------------|------------------------------|-----|----------|
| <span data-ttu-id="e7b62-110">ремовеинифиле</span><span class="sxs-lookup"><span data-stu-id="e7b62-110">RemoveIniFile</span></span> | [<span data-ttu-id="e7b62-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e7b62-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="e7b62-112">Да</span><span class="sxs-lookup"><span data-stu-id="e7b62-112">Y</span></span>   | <span data-ttu-id="e7b62-113">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-113">N</span></span>        |
| <span data-ttu-id="e7b62-114">FileName</span><span class="sxs-lookup"><span data-stu-id="e7b62-114">FileName</span></span>      | [<span data-ttu-id="e7b62-115">FileName</span><span class="sxs-lookup"><span data-stu-id="e7b62-115">FileName</span></span>](text.md)         | <span data-ttu-id="e7b62-116">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-116">N</span></span>   | <span data-ttu-id="e7b62-117">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-117">N</span></span>        |
| <span data-ttu-id="e7b62-118">дирпроперти</span><span class="sxs-lookup"><span data-stu-id="e7b62-118">DirProperty</span></span>   | [<span data-ttu-id="e7b62-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e7b62-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="e7b62-120">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-120">N</span></span>   | <span data-ttu-id="e7b62-121">Да</span><span class="sxs-lookup"><span data-stu-id="e7b62-121">Y</span></span>        |
| <span data-ttu-id="e7b62-122">Section</span><span class="sxs-lookup"><span data-stu-id="e7b62-122">Section</span></span>       | [<span data-ttu-id="e7b62-123">Формате</span><span class="sxs-lookup"><span data-stu-id="e7b62-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e7b62-124">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-124">N</span></span>   | <span data-ttu-id="e7b62-125">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-125">N</span></span>        |
| <span data-ttu-id="e7b62-126">Ключ</span><span class="sxs-lookup"><span data-stu-id="e7b62-126">Key</span></span>           | [<span data-ttu-id="e7b62-127">Формате</span><span class="sxs-lookup"><span data-stu-id="e7b62-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e7b62-128">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-128">N</span></span>   | <span data-ttu-id="e7b62-129">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-129">N</span></span>        |
| <span data-ttu-id="e7b62-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e7b62-130">Value</span></span>         | [<span data-ttu-id="e7b62-131">Формате</span><span class="sxs-lookup"><span data-stu-id="e7b62-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e7b62-132">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-132">N</span></span>   | <span data-ttu-id="e7b62-133">Да</span><span class="sxs-lookup"><span data-stu-id="e7b62-133">Y</span></span>        |
| <span data-ttu-id="e7b62-134">Действие</span><span class="sxs-lookup"><span data-stu-id="e7b62-134">Action</span></span>        | [<span data-ttu-id="e7b62-135">Integer</span><span class="sxs-lookup"><span data-stu-id="e7b62-135">Integer</span></span>](integer.md)       | <span data-ttu-id="e7b62-136">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-136">N</span></span>   | <span data-ttu-id="e7b62-137">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-137">N</span></span>        |
| <span data-ttu-id="e7b62-138">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="e7b62-138">Component\_</span></span>   | [<span data-ttu-id="e7b62-139">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e7b62-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="e7b62-140">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-140">N</span></span>   | <span data-ttu-id="e7b62-141">Нет</span><span class="sxs-lookup"><span data-stu-id="e7b62-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e7b62-142">Столбцы</span><span class="sxs-lookup"><span data-stu-id="e7b62-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e7b62-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>ремовеинифиле</span><span class="sxs-lookup"><span data-stu-id="e7b62-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span></span>
</dt> <dd>

<span data-ttu-id="e7b62-144">Ключ для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="e7b62-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="e7b62-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Файлов</span><span class="sxs-lookup"><span data-stu-id="e7b62-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="e7b62-146">Имя ini-файла, в который необходимо удалить данные.</span><span class="sxs-lookup"><span data-stu-id="e7b62-146">The .ini file name in which to delete the information.</span></span>

</dd> <dt>

<span data-ttu-id="e7b62-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>дирпроперти</span><span class="sxs-lookup"><span data-stu-id="e7b62-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="e7b62-148">Имя свойства, значение которого предполагается преобразовать в полный путь к папке удаляемого ini-файла.</span><span class="sxs-lookup"><span data-stu-id="e7b62-148">Name of a property whose value is assumed to resolve to the full path to the folder of the .ini file to be removed.</span></span> <span data-ttu-id="e7b62-149">Свойство может быть именем каталога в [таблице Directory](directory-table.md), свойством, заданным [таблицей аппсеарч](appsearch-table.md), или любым другим свойством, представляющим полный путь.</span><span class="sxs-lookup"><span data-stu-id="e7b62-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="e7b62-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Раздела</span><span class="sxs-lookup"><span data-stu-id="e7b62-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="e7b62-151">Раздел Localizable. ini-файла.</span><span class="sxs-lookup"><span data-stu-id="e7b62-151">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="e7b62-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел</span><span class="sxs-lookup"><span data-stu-id="e7b62-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="e7b62-153">Ключ локализуемого файла. ini ниже раздела.</span><span class="sxs-lookup"><span data-stu-id="e7b62-153">The localizable .ini file key below the section.</span></span>

</dd> <dt>

<span data-ttu-id="e7b62-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="e7b62-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="e7b62-155">Локализуемое значение, которое необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="e7b62-155">The localizable value to be deleted.</span></span> <span data-ttu-id="e7b62-156">Значение является обязательным, если действие равно 4.</span><span class="sxs-lookup"><span data-stu-id="e7b62-156">The value is required when Action is 4.</span></span>

</dd> <dt>

<span data-ttu-id="e7b62-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="e7b62-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="e7b62-158">Тип изменения, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="e7b62-158">The type of modification to be made.</span></span>



| <span data-ttu-id="e7b62-159">Константа</span><span class="sxs-lookup"><span data-stu-id="e7b62-159">Constant</span></span>                         | <span data-ttu-id="e7b62-160">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="e7b62-160">Hexadecimal</span></span> | <span data-ttu-id="e7b62-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="e7b62-161">Decimal</span></span> | <span data-ttu-id="e7b62-162">Значение</span><span class="sxs-lookup"><span data-stu-id="e7b62-162">Meaning</span></span>                          |
|----------------------------------|-------------|---------|----------------------------------|
| <span data-ttu-id="e7b62-163">**мсидбинифилеактионремовелине**</span><span class="sxs-lookup"><span data-stu-id="e7b62-163">**msidbIniFileActionRemoveLine**</span></span> | <span data-ttu-id="e7b62-164">0x002</span><span class="sxs-lookup"><span data-stu-id="e7b62-164">0x002</span></span>       | <span data-ttu-id="e7b62-165">2</span><span class="sxs-lookup"><span data-stu-id="e7b62-165">2</span></span>       | <span data-ttu-id="e7b62-166">Удаляет запись ini.</span><span class="sxs-lookup"><span data-stu-id="e7b62-166">Deletes .ini entry.</span></span>              |
| <span data-ttu-id="e7b62-167">**мсидбинифилеактионремоветаг**</span><span class="sxs-lookup"><span data-stu-id="e7b62-167">**msidbIniFileActionRemoveTag**</span></span>  | <span data-ttu-id="e7b62-168">0x004</span><span class="sxs-lookup"><span data-stu-id="e7b62-168">0x004</span></span>       | <span data-ttu-id="e7b62-169">4</span><span class="sxs-lookup"><span data-stu-id="e7b62-169">4</span></span>       | <span data-ttu-id="e7b62-170">Удаляет тег из INI-записи.</span><span class="sxs-lookup"><span data-stu-id="e7b62-170">Deletes a tag from a .ini entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e7b62-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="e7b62-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e7b62-172">Внешний ключ в первый столбец [таблицы Component](component-table.md) , ссылающийся на компонент, который управляет удалением значения ini.</span><span class="sxs-lookup"><span data-stu-id="e7b62-172">External key into first column of the [Component table](component-table.md) referencing the component that controls the deletion of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7b62-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7b62-173">Remarks</span></span>

<span data-ttu-id="e7b62-174">Сведения о ini-файле удаляются при выборе соответствующего компонента для установки (локально или из источника).</span><span class="sxs-lookup"><span data-stu-id="e7b62-174">The .ini file information is deleted when the corresponding Component has been selected to be installed, either locally or run from source.</span></span>

<span data-ttu-id="e7b62-175">Эта таблица упоминается при выполнении [действия ремовеинивалуес](removeinivalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b62-175">This table is referred to when the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

<span data-ttu-id="e7b62-176">Если столбец каталога \_ указан как null, то расположение ini-файла является стандартным расположением Windows ini, которое по умолчанию является каталогом Windows.</span><span class="sxs-lookup"><span data-stu-id="e7b62-176">If the Directory\_ column is specified as null, the ini file location is the standard Windows ini location which is the Windows directory by default.</span></span>

<span data-ttu-id="e7b62-177">Удаление последнего значения из раздела приводит к удалению этого раздела.</span><span class="sxs-lookup"><span data-stu-id="e7b62-177">Removing the last value from a section deletes that section.</span></span> <span data-ttu-id="e7b62-178">Нет другого способа удалить весь раздел, кроме удаления всех его значений.</span><span class="sxs-lookup"><span data-stu-id="e7b62-178">There is no other way to delete an entire section other than removing all its values.</span></span>

## <a name="validation"></a><span data-ttu-id="e7b62-179">Проверка</span><span class="sxs-lookup"><span data-stu-id="e7b62-179">Validation</span></span>

<dl>

[<span data-ttu-id="e7b62-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="e7b62-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e7b62-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="e7b62-181">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e7b62-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="e7b62-182">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e7b62-183">ICE40</span><span class="sxs-lookup"><span data-stu-id="e7b62-183">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="e7b62-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="e7b62-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="e7b62-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="e7b62-185">ICE69</span></span>](ice69.md)  
</dl>

 

 



