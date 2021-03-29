---
description: Таблица CustomAction предоставляет средства для интеграции пользовательского кода и данных в установку. Источником выполняемого кода может быть поток, содержащийся в базе данных, недавно установленный файл или существующий исполняемый файл.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Таблица CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810391"
---
# <a name="customaction-table"></a><span data-ttu-id="cc73a-104">Таблица CustomAction</span><span class="sxs-lookup"><span data-stu-id="cc73a-104">CustomAction Table</span></span>

<span data-ttu-id="cc73a-105">Таблица CustomAction предоставляет средства для интеграции пользовательского кода и данных в установку.</span><span class="sxs-lookup"><span data-stu-id="cc73a-105">The CustomAction table provides the means of integrating custom code and data into the installation.</span></span> <span data-ttu-id="cc73a-106">Источником выполняемого кода может быть поток, содержащийся в базе данных, недавно установленный файл или существующий исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="cc73a-106">The source of the code that is executed can be a stream contained within the database, a recently installed file, or an existing executable file.</span></span>

<span data-ttu-id="cc73a-107">Таблица CustomAction содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="cc73a-107">The CustomAction table has the following columns.</span></span>



| <span data-ttu-id="cc73a-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="cc73a-108">Column</span></span>       | <span data-ttu-id="cc73a-109">Type</span><span class="sxs-lookup"><span data-stu-id="cc73a-109">Type</span></span>                               | <span data-ttu-id="cc73a-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="cc73a-110">Key</span></span> | <span data-ttu-id="cc73a-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="cc73a-111">Nullable</span></span> |
|--------------|------------------------------------|-----|----------|
| <span data-ttu-id="cc73a-112">Действие</span><span class="sxs-lookup"><span data-stu-id="cc73a-112">Action</span></span>       | [<span data-ttu-id="cc73a-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="cc73a-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="cc73a-114">Да</span><span class="sxs-lookup"><span data-stu-id="cc73a-114">Y</span></span>   | <span data-ttu-id="cc73a-115">Нет</span><span class="sxs-lookup"><span data-stu-id="cc73a-115">N</span></span>        |
| <span data-ttu-id="cc73a-116">Тип</span><span class="sxs-lookup"><span data-stu-id="cc73a-116">Type</span></span>         | [<span data-ttu-id="cc73a-117">Integer</span><span class="sxs-lookup"><span data-stu-id="cc73a-117">Integer</span></span>](integer.md)             | <span data-ttu-id="cc73a-118">Нет</span><span class="sxs-lookup"><span data-stu-id="cc73a-118">N</span></span>   | <span data-ttu-id="cc73a-119">Нет</span><span class="sxs-lookup"><span data-stu-id="cc73a-119">N</span></span>        |
| <span data-ttu-id="cc73a-120">Источник</span><span class="sxs-lookup"><span data-stu-id="cc73a-120">Source</span></span>       | [<span data-ttu-id="cc73a-121">кустомсаурце</span><span class="sxs-lookup"><span data-stu-id="cc73a-121">CustomSource</span></span>](customsource.md)   | <span data-ttu-id="cc73a-122">Нет</span><span class="sxs-lookup"><span data-stu-id="cc73a-122">N</span></span>   | <span data-ttu-id="cc73a-123">Да</span><span class="sxs-lookup"><span data-stu-id="cc73a-123">Y</span></span>        |
| <span data-ttu-id="cc73a-124">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="cc73a-124">Target</span></span>       | [<span data-ttu-id="cc73a-125">Формате</span><span class="sxs-lookup"><span data-stu-id="cc73a-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="cc73a-126">Нет</span><span class="sxs-lookup"><span data-stu-id="cc73a-126">N</span></span>   | <span data-ttu-id="cc73a-127">Да</span><span class="sxs-lookup"><span data-stu-id="cc73a-127">Y</span></span>        |
| <span data-ttu-id="cc73a-128">ExtendedType</span><span class="sxs-lookup"><span data-stu-id="cc73a-128">ExtendedType</span></span> | [<span data-ttu-id="cc73a-129">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="cc73a-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="cc73a-130">Нет</span><span class="sxs-lookup"><span data-stu-id="cc73a-130">N</span></span>   | <span data-ttu-id="cc73a-131">Да</span><span class="sxs-lookup"><span data-stu-id="cc73a-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cc73a-132">Столбцы</span><span class="sxs-lookup"><span data-stu-id="cc73a-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cc73a-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="cc73a-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="cc73a-134">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="cc73a-134">Name of the action.</span></span> <span data-ttu-id="cc73a-135">Действие обычно отображается в таблице последовательности, если оно не вызвано другим пользовательским действием.</span><span class="sxs-lookup"><span data-stu-id="cc73a-135">The action normally appears in a sequence table unless it is called by another custom action.</span></span> <span data-ttu-id="cc73a-136">Если имя соответствует любому встроенному действию, то пользовательское действие никогда не вызывается.</span><span class="sxs-lookup"><span data-stu-id="cc73a-136">If the name matches any built-in action, then the custom action is never called.</span></span>

<span data-ttu-id="cc73a-137">Первичный ключ таблицы.</span><span class="sxs-lookup"><span data-stu-id="cc73a-137">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="cc73a-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Тип</span><span class="sxs-lookup"><span data-stu-id="cc73a-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="cc73a-139">Поле флаговых битов, определяющее базовый тип настраиваемого действия и параметров.</span><span class="sxs-lookup"><span data-stu-id="cc73a-139">A field of flag bits specifying the basic type of custom action and options.</span></span> <span data-ttu-id="cc73a-140">Список базовых типов см. в разделе [сводный список всех типов настраиваемых действий](summary-list-of-all-custom-action-types.md) .</span><span class="sxs-lookup"><span data-stu-id="cc73a-140">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a list of the basic types.</span></span> <span data-ttu-id="cc73a-141">См. раздел Параметры [обработки возвращаемых пользователем действий](custom-action-return-processing-options.md), [Параметры планирования выполнения настраиваемых](custom-action-execution-scheduling-options.md)действий, [параметр скрытого целевого действия](custom-action-hidden-target-option.md)и [настраиваемого действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="cc73a-141">See [Custom Action Return Processing Options](custom-action-return-processing-options.md), [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md), [Custom Action Hidden Target Option](custom-action-hidden-target-option.md), and [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc73a-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Источника</span><span class="sxs-lookup"><span data-stu-id="cc73a-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="cc73a-143">Имя свойства или внешний ключ в другую таблицу.</span><span class="sxs-lookup"><span data-stu-id="cc73a-143">A property name or external key into another table.</span></span> <span data-ttu-id="cc73a-144">Описание возможных источников настраиваемых действий см. в разделе [источники настраиваемых действий](custom-action-sources.md) и [сводный список всех типов настраиваемых действий](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="cc73a-144">For a discussion of the possible custom action sources, see [Custom Action Sources](custom-action-sources.md) and the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span> <span data-ttu-id="cc73a-145">Например, исходный столбец может содержать внешний ключ в первом столбце одной из следующих таблиц, содержащих источник пользовательского кода действия.</span><span class="sxs-lookup"><span data-stu-id="cc73a-145">For example, the Source column may contain an external key into the first column of one of the following tables containing the source of the custom action code.</span></span>

<span data-ttu-id="cc73a-146">[Таблица каталогов](directory-table.md) для вызова существующих исполняемых файлов.</span><span class="sxs-lookup"><span data-stu-id="cc73a-146">[Directory table](directory-table.md) for calling existing executables.</span></span>

<span data-ttu-id="cc73a-147">[Таблица файлов](file-table.md) для вызова исполняемых файлов и библиотек DLL, которые были только что установлены.</span><span class="sxs-lookup"><span data-stu-id="cc73a-147">[File table](file-table.md) for calling executables and DLLs that have just been installed.</span></span>

<span data-ttu-id="cc73a-148">[Двоичная таблица](binary-table.md) для вызова исполняемых файлов, библиотек DLL и данных, хранящихся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cc73a-148">[Binary table](binary-table.md) for calling executables, DLLs, and data stored in the database.</span></span>

<span data-ttu-id="cc73a-149">[Таблица свойств](property-table.md) для вызова исполняемых файлов, пути к которым хранятся в свойстве.</span><span class="sxs-lookup"><span data-stu-id="cc73a-149">[Property table](property-table.md) for calling executables whose paths are held by a property.</span></span>

</dd> <dt>

<span data-ttu-id="cc73a-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Мишень</span><span class="sxs-lookup"><span data-stu-id="cc73a-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="cc73a-151">Параметр выполнения, зависящий от базового типа настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="cc73a-151">An execution parameter that depends on the basic type of custom action.</span></span> <span data-ttu-id="cc73a-152">Сведения о том, что следует вводить в этом поле для каждого типа настраиваемого действия, см. в [списке типов пользовательских действий](summary-list-of-all-custom-action-types.md) .</span><span class="sxs-lookup"><span data-stu-id="cc73a-152">See the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a description of what should be entered in this field for each type of custom action.</span></span> <span data-ttu-id="cc73a-153">Например, это поле может содержать следующие сведения в зависимости от настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="cc73a-153">For example, this field may contain the following depending on the custom action.</span></span>



| <span data-ttu-id="cc73a-154">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="cc73a-154">Target</span></span>                                    | <span data-ttu-id="cc73a-155">Пользовательское действие</span><span class="sxs-lookup"><span data-stu-id="cc73a-155">Custom action</span></span>                         |
|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="cc73a-156">Точка входа (обязательно)</span><span class="sxs-lookup"><span data-stu-id="cc73a-156">Entry point (required)</span></span>                    | <span data-ttu-id="cc73a-157">Вызов библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="cc73a-157">Calling a DLL.</span></span>                        |
| <span data-ttu-id="cc73a-158">Имя исполняемого файла с аргументами (обязательно)</span><span class="sxs-lookup"><span data-stu-id="cc73a-158">Executable name with arguments (required)</span></span> | <span data-ttu-id="cc73a-159">Вызов существующего исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="cc73a-159">Calling an existing executable.</span></span>       |
| <span data-ttu-id="cc73a-160">Аргументы командной строки (необязательно)</span><span class="sxs-lookup"><span data-stu-id="cc73a-160">Command line arguments (optional)</span></span>         | <span data-ttu-id="cc73a-161">Вызов только что установленного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="cc73a-161">Calling an executable just installed.</span></span> |
| <span data-ttu-id="cc73a-162">Имя целевого файла (обязательно)</span><span class="sxs-lookup"><span data-stu-id="cc73a-162">Target file name (required)</span></span>               | <span data-ttu-id="cc73a-163">Создание файла на основе пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="cc73a-163">Creating a file from custom data.</span></span>     |
| <span data-ttu-id="cc73a-164">NULL</span><span class="sxs-lookup"><span data-stu-id="cc73a-164">Null</span></span>                                      | <span data-ttu-id="cc73a-165">Выполнение кода скрипта.</span><span class="sxs-lookup"><span data-stu-id="cc73a-165">Executing script code.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="cc73a-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span><span class="sxs-lookup"><span data-stu-id="cc73a-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span></span>
</dt> <dd>

<span data-ttu-id="cc73a-167">Введите значение **мсидбкустомактионтипепатчунинсталл** в этом поле, чтобы указать настраиваемое действие с [параметром удаления исправления настраиваемого действия](custom-action-patch-uninstall-option.md).</span><span class="sxs-lookup"><span data-stu-id="cc73a-167">Enter the **msidbCustomActionTypePatchUninstall** value in this field to specify a custom action with the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md).</span></span>

<span data-ttu-id="cc73a-168">**[Установщик Windows 4,0 и более ранних версий](not-supported-in-windows-installer-4-0.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cc73a-168">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="cc73a-169">Этот параметр доступен, начиная с установщик Windows 4,5.</span><span class="sxs-lookup"><span data-stu-id="cc73a-169">This option is available beginning with Windows Installer 4.5.</span></span>

</dd> </dl>

<span data-ttu-id="cc73a-170">Дополнительные сведения см. в разделах, посвященных [настраиваемым действиям](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="cc73a-170">For more information, see all the topics under [Custom Actions](custom-actions.md).</span></span>

## <a name="validation"></a><span data-ttu-id="cc73a-171">Проверка</span><span class="sxs-lookup"><span data-stu-id="cc73a-171">Validation</span></span>

<dl>

[<span data-ttu-id="cc73a-172">ICE03</span><span class="sxs-lookup"><span data-stu-id="cc73a-172">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cc73a-173">ICE06</span><span class="sxs-lookup"><span data-stu-id="cc73a-173">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cc73a-174">ICE12</span><span class="sxs-lookup"><span data-stu-id="cc73a-174">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="cc73a-175">ICE27</span><span class="sxs-lookup"><span data-stu-id="cc73a-175">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="cc73a-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="cc73a-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="cc73a-177">ICE63</span><span class="sxs-lookup"><span data-stu-id="cc73a-177">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="cc73a-178">ICE68</span><span class="sxs-lookup"><span data-stu-id="cc73a-178">ICE68</span></span>](ice68.md)  
[<span data-ttu-id="cc73a-179">ICE72</span><span class="sxs-lookup"><span data-stu-id="cc73a-179">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="cc73a-180">ICE75</span><span class="sxs-lookup"><span data-stu-id="cc73a-180">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="cc73a-181">ICE77</span><span class="sxs-lookup"><span data-stu-id="cc73a-181">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="cc73a-182">ICE80</span><span class="sxs-lookup"><span data-stu-id="cc73a-182">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="cc73a-183">ICE88</span><span class="sxs-lookup"><span data-stu-id="cc73a-183">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="cc73a-184">ICE93</span><span class="sxs-lookup"><span data-stu-id="cc73a-184">ICE93</span></span>](ice93.md)  
</dl>

 

 



