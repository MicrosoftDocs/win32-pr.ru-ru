---
description: В таблице команд содержатся сведения о командах, связанных с расширениями имен файлов, которые должны быть созданы как часть объявления продукта. Каждая строка создает набор разделов и значений реестра.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Таблица команд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674491"
---
# <a name="verb-table"></a><span data-ttu-id="d425d-104">Таблица команд</span><span class="sxs-lookup"><span data-stu-id="d425d-104">Verb Table</span></span>

<span data-ttu-id="d425d-105">В таблице команд содержатся сведения о командах, связанных с расширениями имен файлов, которые должны быть созданы как часть объявления продукта.</span><span class="sxs-lookup"><span data-stu-id="d425d-105">The Verb table contains command-verb information associated with file name extensions that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="d425d-106">Каждая строка создает набор разделов и значений реестра.</span><span class="sxs-lookup"><span data-stu-id="d425d-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="d425d-107">Таблица команд содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="d425d-107">The Verb table has the following columns.</span></span>



| <span data-ttu-id="d425d-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="d425d-108">Column</span></span>      | <span data-ttu-id="d425d-109">Type</span><span class="sxs-lookup"><span data-stu-id="d425d-109">Type</span></span>                       | <span data-ttu-id="d425d-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="d425d-110">Key</span></span> | <span data-ttu-id="d425d-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="d425d-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="d425d-112">Расширение\_</span><span class="sxs-lookup"><span data-stu-id="d425d-112">Extension\_</span></span> | [<span data-ttu-id="d425d-113">Text</span><span class="sxs-lookup"><span data-stu-id="d425d-113">Text</span></span>](text.md)           | <span data-ttu-id="d425d-114">Да</span><span class="sxs-lookup"><span data-stu-id="d425d-114">Y</span></span>   | <span data-ttu-id="d425d-115">Нет</span><span class="sxs-lookup"><span data-stu-id="d425d-115">N</span></span>        |
| <span data-ttu-id="d425d-116">Команда</span><span class="sxs-lookup"><span data-stu-id="d425d-116">Verb</span></span>        | [<span data-ttu-id="d425d-117">Text</span><span class="sxs-lookup"><span data-stu-id="d425d-117">Text</span></span>](text.md)           | <span data-ttu-id="d425d-118">Да</span><span class="sxs-lookup"><span data-stu-id="d425d-118">Y</span></span>   | <span data-ttu-id="d425d-119">Нет</span><span class="sxs-lookup"><span data-stu-id="d425d-119">N</span></span>        |
| <span data-ttu-id="d425d-120">Последовательность</span><span class="sxs-lookup"><span data-stu-id="d425d-120">Sequence</span></span>    | [<span data-ttu-id="d425d-121">Integer</span><span class="sxs-lookup"><span data-stu-id="d425d-121">Integer</span></span>](integer.md)     | <span data-ttu-id="d425d-122">Нет</span><span class="sxs-lookup"><span data-stu-id="d425d-122">N</span></span>   | <span data-ttu-id="d425d-123">Да</span><span class="sxs-lookup"><span data-stu-id="d425d-123">Y</span></span>        |
| <span data-ttu-id="d425d-124">Get-Help</span><span class="sxs-lookup"><span data-stu-id="d425d-124">Command</span></span>     | [<span data-ttu-id="d425d-125">Формате</span><span class="sxs-lookup"><span data-stu-id="d425d-125">Formatted</span></span>](formatted.md) | <span data-ttu-id="d425d-126">Нет</span><span class="sxs-lookup"><span data-stu-id="d425d-126">N</span></span>   | <span data-ttu-id="d425d-127">Да</span><span class="sxs-lookup"><span data-stu-id="d425d-127">Y</span></span>        |
| <span data-ttu-id="d425d-128">Аргумент</span><span class="sxs-lookup"><span data-stu-id="d425d-128">Argument</span></span>    | [<span data-ttu-id="d425d-129">Формате</span><span class="sxs-lookup"><span data-stu-id="d425d-129">Formatted</span></span>](formatted.md) | <span data-ttu-id="d425d-130">Нет</span><span class="sxs-lookup"><span data-stu-id="d425d-130">N</span></span>   | <span data-ttu-id="d425d-131">Да</span><span class="sxs-lookup"><span data-stu-id="d425d-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d425d-132">Столбцы</span><span class="sxs-lookup"><span data-stu-id="d425d-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d425d-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Продлен\_</span><span class="sxs-lookup"><span data-stu-id="d425d-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="d425d-134">Расширение, связанное со строкой таблицы.</span><span class="sxs-lookup"><span data-stu-id="d425d-134">The extension associated with the table row.</span></span> <span data-ttu-id="d425d-135">Этот столбец является внешним ключом к первому столбцу [таблицы расширений](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="d425d-135">This column is an external key to the first column of the [Extension table](extension-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d425d-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Переключател</span><span class="sxs-lookup"><span data-stu-id="d425d-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span>
</dt> <dd>

<span data-ttu-id="d425d-137">Команда для команды.</span><span class="sxs-lookup"><span data-stu-id="d425d-137">The verb for the command.</span></span>

</dd> <dt>

<span data-ttu-id="d425d-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="d425d-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="d425d-139">Последовательность команд.</span><span class="sxs-lookup"><span data-stu-id="d425d-139">The sequence of the commands.</span></span> <span data-ttu-id="d425d-140">Для подготовки упорядоченного списка к значению по умолчанию для ключа оболочки используются только команды, для которых столбец последовательности имеет значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="d425d-140">Only verbs for which the Sequence column is non-Null are used to prepare an ordered list for the default value of the shell key.</span></span> <span data-ttu-id="d425d-141">Команда с наименьшим значением в этом столбце станет глаголом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d425d-141">The Verb with the lowest value in this column becomes the default verb.</span></span>

</dd> <dt>

<span data-ttu-id="d425d-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Кнопки</span><span class="sxs-lookup"><span data-stu-id="d425d-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="d425d-143">Локализуемый текст, отображаемый в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="d425d-143">The localizable text displayed on the context menu.</span></span>

</dd> <dt>

<span data-ttu-id="d425d-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Параметр</span><span class="sxs-lookup"><span data-stu-id="d425d-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="d425d-145">Значение для аргументов команды.</span><span class="sxs-lookup"><span data-stu-id="d425d-145">Value for the command arguments.</span></span>

<span data-ttu-id="d425d-146">Обратите внимание, что разрешение свойств в поле Argument ограничено.</span><span class="sxs-lookup"><span data-stu-id="d425d-146">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="d425d-147">Свойство, отформатированное как \[ *свойство* \] в этом поле, может быть разрешено только в том случае, если свойство уже имеет предполагаемое значение при установке компонента, владеющего этой командой.</span><span class="sxs-lookup"><span data-stu-id="d425d-147">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component owning the verb is installed.</span></span> <span data-ttu-id="d425d-148">Например, для аргумента " \[ \#MyDoc.doc\] ", чтобы разрешить правильное значение, один и тот же процесс должен установить файл MyDoc.doc и компонент, которому принадлежит команда.</span><span class="sxs-lookup"><span data-stu-id="d425d-148">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d425d-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d425d-149">Remarks</span></span>

<span data-ttu-id="d425d-150">Эта таблица упоминается при выполнении [действия регистерекстенсионинфо](registerextensioninfo-action.md) или [унрегистерекстенсионинфо](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d425d-150">This table is referred to when the [RegisterExtensionInfo action](registerextensioninfo-action.md) or the [UnregisterExtensionInfo action](unregisterextensioninfo-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="d425d-151">Проверка</span><span class="sxs-lookup"><span data-stu-id="d425d-151">Validation</span></span>

<dl>

[<span data-ttu-id="d425d-152">ICE03</span><span class="sxs-lookup"><span data-stu-id="d425d-152">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d425d-153">ICE06</span><span class="sxs-lookup"><span data-stu-id="d425d-153">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d425d-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="d425d-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d425d-155">ICE46</span><span class="sxs-lookup"><span data-stu-id="d425d-155">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="d425d-156">ICE69</span><span class="sxs-lookup"><span data-stu-id="d425d-156">ICE69</span></span>](ice69.md)  
</dl>

 

 



