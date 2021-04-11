---
description: Таблица Инифиле содержит сведения о ini-файле, которые приложение должно установить в ini-файл.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Таблица Инифиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080672"
---
# <a name="inifile-table"></a><span data-ttu-id="0f1cc-103">Таблица Инифиле</span><span class="sxs-lookup"><span data-stu-id="0f1cc-103">IniFile Table</span></span>

<span data-ttu-id="0f1cc-104">Таблица Инифиле содержит сведения о ini-файле, которые приложение должно установить в ini-файл.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-104">The IniFile table contains the .ini information that the application needs to set in an .ini file.</span></span>

<span data-ttu-id="0f1cc-105">Таблица Инифиле содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-105">The IniFile table has the following columns.</span></span>



| <span data-ttu-id="0f1cc-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="0f1cc-106">Column</span></span>      | <span data-ttu-id="0f1cc-107">Type</span><span class="sxs-lookup"><span data-stu-id="0f1cc-107">Type</span></span>                         | <span data-ttu-id="0f1cc-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="0f1cc-108">Key</span></span> | <span data-ttu-id="0f1cc-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="0f1cc-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="0f1cc-110">инифиле</span><span class="sxs-lookup"><span data-stu-id="0f1cc-110">IniFile</span></span>     | [<span data-ttu-id="0f1cc-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0f1cc-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="0f1cc-112">Да</span><span class="sxs-lookup"><span data-stu-id="0f1cc-112">Y</span></span>   | <span data-ttu-id="0f1cc-113">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-113">N</span></span>        |
| <span data-ttu-id="0f1cc-114">FileName</span><span class="sxs-lookup"><span data-stu-id="0f1cc-114">FileName</span></span>    | [<span data-ttu-id="0f1cc-115">FileName</span><span class="sxs-lookup"><span data-stu-id="0f1cc-115">FileName</span></span>](text.md)         | <span data-ttu-id="0f1cc-116">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-116">N</span></span>   | <span data-ttu-id="0f1cc-117">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-117">N</span></span>        |
| <span data-ttu-id="0f1cc-118">дирпроперти</span><span class="sxs-lookup"><span data-stu-id="0f1cc-118">DirProperty</span></span> | [<span data-ttu-id="0f1cc-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0f1cc-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="0f1cc-120">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-120">N</span></span>   | <span data-ttu-id="0f1cc-121">Да</span><span class="sxs-lookup"><span data-stu-id="0f1cc-121">Y</span></span>        |
| <span data-ttu-id="0f1cc-122">Section</span><span class="sxs-lookup"><span data-stu-id="0f1cc-122">Section</span></span>     | [<span data-ttu-id="0f1cc-123">Формате</span><span class="sxs-lookup"><span data-stu-id="0f1cc-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="0f1cc-124">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-124">N</span></span>   | <span data-ttu-id="0f1cc-125">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-125">N</span></span>        |
| <span data-ttu-id="0f1cc-126">Ключ</span><span class="sxs-lookup"><span data-stu-id="0f1cc-126">Key</span></span>         | [<span data-ttu-id="0f1cc-127">Формате</span><span class="sxs-lookup"><span data-stu-id="0f1cc-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="0f1cc-128">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-128">N</span></span>   | <span data-ttu-id="0f1cc-129">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-129">N</span></span>        |
| <span data-ttu-id="0f1cc-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0f1cc-130">Value</span></span>       | [<span data-ttu-id="0f1cc-131">Формате</span><span class="sxs-lookup"><span data-stu-id="0f1cc-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="0f1cc-132">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-132">N</span></span>   | <span data-ttu-id="0f1cc-133">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-133">N</span></span>        |
| <span data-ttu-id="0f1cc-134">Действие</span><span class="sxs-lookup"><span data-stu-id="0f1cc-134">Action</span></span>      | [<span data-ttu-id="0f1cc-135">Integer</span><span class="sxs-lookup"><span data-stu-id="0f1cc-135">Integer</span></span>](integer.md)       | <span data-ttu-id="0f1cc-136">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-136">N</span></span>   | <span data-ttu-id="0f1cc-137">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-137">N</span></span>        |
| <span data-ttu-id="0f1cc-138">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="0f1cc-138">Component\_</span></span> | [<span data-ttu-id="0f1cc-139">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0f1cc-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="0f1cc-140">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-140">N</span></span>   | <span data-ttu-id="0f1cc-141">Нет</span><span class="sxs-lookup"><span data-stu-id="0f1cc-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0f1cc-142">Столбцы</span><span class="sxs-lookup"><span data-stu-id="0f1cc-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0f1cc-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>инифиле</span><span class="sxs-lookup"><span data-stu-id="0f1cc-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span></span>
</dt> <dd>

<span data-ttu-id="0f1cc-144">Ключ для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="0f1cc-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Файлов</span><span class="sxs-lookup"><span data-stu-id="0f1cc-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="0f1cc-146">Локализуемое имя ini-файла, в который записываются сведения.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-146">The localizable name of the .ini file in which to write the information.</span></span>

</dd> <dt>

<span data-ttu-id="0f1cc-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>дирпроперти</span><span class="sxs-lookup"><span data-stu-id="0f1cc-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="0f1cc-148">Имя свойства со значением, которое разрешается в полный путь к папке, содержащей ini-файл.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-148">Name of a property having a value that resolves to the full path of the folder containing the .ini file.</span></span> <span data-ttu-id="0f1cc-149">Свойство может быть именем каталога в [таблице Directory](directory-table.md), свойством, заданным [таблицей аппсеарч](appsearch-table.md), или любым другим свойством, представляющим полный путь.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span> <span data-ttu-id="0f1cc-150">Если это поле оставлено пустым, ini-файл создается в папке с полным путем, указанным в свойстве [**виндовсфолдер**](windowsfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="0f1cc-150">If this field is left blank, the .ini file is created in the folder having the full path specified by the [**WindowsFolder**](windowsfolder.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="0f1cc-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Раздела</span><span class="sxs-lookup"><span data-stu-id="0f1cc-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="0f1cc-152">Раздел Localizable. ini-файла.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-152">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="0f1cc-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел</span><span class="sxs-lookup"><span data-stu-id="0f1cc-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="0f1cc-154">Ключ локализуемого файла. ini в разделе.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-154">The localizable .ini file key within the section.</span></span>

</dd> <dt>

<span data-ttu-id="0f1cc-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="0f1cc-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="0f1cc-156">Локализуемое значение, которое необходимо записать.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-156">The localizable value to be written.</span></span>

</dd> <dt>

<span data-ttu-id="0f1cc-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="0f1cc-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="0f1cc-158">Тип изменения, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-158">The type of modification to be made.</span></span>



| <span data-ttu-id="0f1cc-159">Константа</span><span class="sxs-lookup"><span data-stu-id="0f1cc-159">Constant</span></span>                         | <span data-ttu-id="0f1cc-160">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="0f1cc-160">Hexadecimal</span></span> | <span data-ttu-id="0f1cc-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="0f1cc-161">Decimal</span></span> | <span data-ttu-id="0f1cc-162">Изменение</span><span class="sxs-lookup"><span data-stu-id="0f1cc-162">Modification</span></span>                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0f1cc-163">**мсидбинифилеактионаддлине**</span><span class="sxs-lookup"><span data-stu-id="0f1cc-163">**msidbIniFileActionAddLine**</span></span>    | <span data-ttu-id="0f1cc-164">0x000</span><span class="sxs-lookup"><span data-stu-id="0f1cc-164">0x000</span></span>       | <span data-ttu-id="0f1cc-165">0</span><span class="sxs-lookup"><span data-stu-id="0f1cc-165">0</span></span>       | <span data-ttu-id="0f1cc-166">Создает или обновляет запись ini-элемента.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-166">Creates or updates a .ini entry.</span></span>                                                 |
| <span data-ttu-id="0f1cc-167">**мсидбинифилеактионкреателине**</span><span class="sxs-lookup"><span data-stu-id="0f1cc-167">**msidbIniFileActionCreateLine**</span></span> | <span data-ttu-id="0f1cc-168">0x001</span><span class="sxs-lookup"><span data-stu-id="0f1cc-168">0x001</span></span>       | <span data-ttu-id="0f1cc-169">1</span><span class="sxs-lookup"><span data-stu-id="0f1cc-169">1</span></span>       | <span data-ttu-id="0f1cc-170">Создает запись ini, только если запись еще не существует.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-170">Creates a .ini entry only if the entry does not already exist.</span></span>                   |
| <span data-ttu-id="0f1cc-171">**мсидбинифилеактионаддтаг**</span><span class="sxs-lookup"><span data-stu-id="0f1cc-171">**msidbIniFileActionAddTag**</span></span>     | <span data-ttu-id="0f1cc-172">0x003</span><span class="sxs-lookup"><span data-stu-id="0f1cc-172">0x003</span></span>       | <span data-ttu-id="0f1cc-173">3</span><span class="sxs-lookup"><span data-stu-id="0f1cc-173">3</span></span>       | <span data-ttu-id="0f1cc-174">Создает новую запись или добавляет к существующей записи новое значение с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-174">Creates a new entry or appends a new comma-separated value to an existing entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0f1cc-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="0f1cc-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="0f1cc-176">Внешний ключ в первый столбец [таблицы Component](component-table.md) , ссылающийся на компонент, который управляет установкой значения. ini.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-176">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f1cc-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f1cc-177">Remarks</span></span>

<span data-ttu-id="0f1cc-178">Сведения о ini-файле записываются, когда соответствующий компонент был выбран для установки в качестве локального или запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="0f1cc-178">The .ini file information is written out when the corresponding component has been selected to be installed as local or run from source.</span></span>

<span data-ttu-id="0f1cc-179">Эта таблица упоминается при выполнении [действия вритеинивалуес](writeinivalues-action.md) или [ремовеинивалуес](removeinivalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0f1cc-179">This table is referred to when the [WriteIniValues action](writeinivalues-action.md) or the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="0f1cc-180">Проверка</span><span class="sxs-lookup"><span data-stu-id="0f1cc-180">Validation</span></span>

<dl>

[<span data-ttu-id="0f1cc-181">ICE03</span><span class="sxs-lookup"><span data-stu-id="0f1cc-181">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0f1cc-182">ICE06</span><span class="sxs-lookup"><span data-stu-id="0f1cc-182">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0f1cc-183">ICE32</span><span class="sxs-lookup"><span data-stu-id="0f1cc-183">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="0f1cc-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="0f1cc-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="0f1cc-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="0f1cc-185">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="0f1cc-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="0f1cc-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="0f1cc-187">ICE91</span><span class="sxs-lookup"><span data-stu-id="0f1cc-187">ICE91</span></span>](ice91.md)  
</dl>

 

 



