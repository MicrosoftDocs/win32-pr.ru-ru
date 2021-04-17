---
description: ICE12 проверяет таблицы CustomAction, Directory, Админексекутесекуенце, Админуисекуенце, Адвтексекутесекуенце, Инсталлексекутесекуенце и InstallUISequence базы данных установщик Windows.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663675"
---
# <a name="ice12"></a><span data-ttu-id="09d43-103">ICE12</span><span class="sxs-lookup"><span data-stu-id="09d43-103">ICE12</span></span>

<span data-ttu-id="09d43-104">ICE12 запрашивает таблицы [CustomAction](customaction-table.md), [Directory](directory-table.md), [админексекутесекуенце](adminexecutesequence-table.md), [админуисекуенце](adminuisequence-table.md), [адвтексекутесекуенце](advtexecutesequence-table.md), [инсталлексекутесекуенце](installexecutesequence-table.md)и [InstallUISequence](installuisequence-table.md) , чтобы проверить следующее:</span><span class="sxs-lookup"><span data-stu-id="09d43-104">ICE12 queries the [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [InstallUISequence](installuisequence-table.md) tables to validate the following:</span></span>

-   <span data-ttu-id="09d43-105">Это [действие костфинализе](costfinalize-action.md) выполняется во всех таблицах последовательностей, содержащих действия типа [пользовательское действие 35](custom-action-type-35.md) или [тип настраиваемого действия 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="09d43-105">That the [CostFinalize action](costfinalize-action.md) occurs in any sequence table containing actions of the type [Custom Action Type 35](custom-action-type-35.md) or [Custom Action Type 51](custom-action-type-51.md).</span></span>
-   <span data-ttu-id="09d43-106">Каждый [тип настраиваемого действия 35](custom-action-type-35.md) поступает после [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="09d43-106">That every [Custom Action Type 35](custom-action-type-35.md) comes after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="09d43-107">в таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="09d43-107">in the sequence tables.</span></span>
-   <span data-ttu-id="09d43-108">Каждый [тип настраиваемого действия 51](custom-action-type-51.md) , который имеет внешний ключ к таблице каталога в исходном столбце таблицы CustomAction, предшествует [действию костфинализе](costfinalize-action.md) в таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="09d43-108">That every [Custom Action Type 51](custom-action-type-51.md) that has a foreign key to the Directory table in the Source column of the CustomAction table comes before the [CostFinalize action](costfinalize-action.md) in the sequence tables.</span></span>

<span data-ttu-id="09d43-109">Обратите внимание, что ICE12 не проверяет форматированный текст в целевом столбце таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="09d43-109">Note that ICE12 does not validate the formatted text in the Target column of the CustomAction table.</span></span>

## <a name="result"></a><span data-ttu-id="09d43-110">Результат</span><span class="sxs-lookup"><span data-stu-id="09d43-110">Result</span></span>

<span data-ttu-id="09d43-111">ICE12 отправляет сообщение об ошибке, если проверка настраиваемых действий, заданных в свойстве каталога, завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="09d43-111">ICE12 posts an error message if validation of the custom actions that set a directory property fails.</span></span>

## <a name="example"></a><span data-ttu-id="09d43-112">Пример</span><span class="sxs-lookup"><span data-stu-id="09d43-112">Example</span></span>

<span data-ttu-id="09d43-113">ICE12 будет публиковать три ошибки для показанного примера.</span><span class="sxs-lookup"><span data-stu-id="09d43-113">ICE12 would post three errors for the example shown.</span></span>

-   <span data-ttu-id="09d43-114">Папка "MyFolder" для CA1 не найдена в таблице Directory</span><span class="sxs-lookup"><span data-stu-id="09d43-114">For CA1, Folder 'MyFolder' not found in Directory table</span></span>
-   <span data-ttu-id="09d43-115">Для CA2 последовательность "80" предшествует Костфинализе в таблице Инсталлексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="09d43-115">For CA2, Sequence '80' comes before CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="09d43-116">Он должен следовать после ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="09d43-116">It must come after (CF@100)</span></span>
-   <span data-ttu-id="09d43-117">Для CA3 последовательность "125" поступает после Костфинализе в таблице Инсталлексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="09d43-117">For CA3, Sequence '125' comes after CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="09d43-118">Он должен предшествовать ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="09d43-118">It must come before (CF@100)</span></span>

<span data-ttu-id="09d43-119">[Таблица CustomAction](customaction-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="09d43-119">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="09d43-120">Действие</span><span class="sxs-lookup"><span data-stu-id="09d43-120">Action</span></span> | <span data-ttu-id="09d43-121">Тип</span><span class="sxs-lookup"><span data-stu-id="09d43-121">Type</span></span> | <span data-ttu-id="09d43-122">Источник</span><span class="sxs-lookup"><span data-stu-id="09d43-122">Source</span></span>        |
|--------|------|---------------|
| <span data-ttu-id="09d43-123">CA1</span><span class="sxs-lookup"><span data-stu-id="09d43-123">CA1</span></span>    | <span data-ttu-id="09d43-124">35</span><span class="sxs-lookup"><span data-stu-id="09d43-124">35</span></span>   | <span data-ttu-id="09d43-125">MyFolder</span><span class="sxs-lookup"><span data-stu-id="09d43-125">MyFolder</span></span>      |
| <span data-ttu-id="09d43-126">CA2</span><span class="sxs-lookup"><span data-stu-id="09d43-126">CA2</span></span>    | <span data-ttu-id="09d43-127">35</span><span class="sxs-lookup"><span data-stu-id="09d43-127">35</span></span>   | <span data-ttu-id="09d43-128">виндовсфолдер</span><span class="sxs-lookup"><span data-stu-id="09d43-128">WindowsFolder</span></span> |
| <span data-ttu-id="09d43-129">CA3</span><span class="sxs-lookup"><span data-stu-id="09d43-129">CA3</span></span>    | <span data-ttu-id="09d43-130">51</span><span class="sxs-lookup"><span data-stu-id="09d43-130">51</span></span>   | <span data-ttu-id="09d43-131">виндовсфолдер</span><span class="sxs-lookup"><span data-stu-id="09d43-131">WindowsFolder</span></span> |



 

[<span data-ttu-id="09d43-132">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="09d43-132">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="09d43-133">Каталог</span><span class="sxs-lookup"><span data-stu-id="09d43-133">Directory</span></span>     | <span data-ttu-id="09d43-134">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="09d43-134">Directory\_Parent</span></span> | <span data-ttu-id="09d43-135">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="09d43-135">DefaultDir</span></span>    |
|---------------|-------------------|---------------|
| <span data-ttu-id="09d43-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="09d43-136">TARGETDIR</span></span>     |                   | <span data-ttu-id="09d43-137">SourceDir</span><span class="sxs-lookup"><span data-stu-id="09d43-137">SourceDir</span></span>     |
| <span data-ttu-id="09d43-138">виндовсфолдер</span><span class="sxs-lookup"><span data-stu-id="09d43-138">WindowsFolder</span></span> | <span data-ttu-id="09d43-139">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="09d43-139">TARGETDIR</span></span>         | <span data-ttu-id="09d43-140">виндовсфолдер</span><span class="sxs-lookup"><span data-stu-id="09d43-140">WindowsFolder</span></span> |



 

<span data-ttu-id="09d43-141">[Таблица инсталлексекутесекуенце](installexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="09d43-141">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="09d43-142">Действие</span><span class="sxs-lookup"><span data-stu-id="09d43-142">Action</span></span>       | <span data-ttu-id="09d43-143">Последовательность</span><span class="sxs-lookup"><span data-stu-id="09d43-143">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="09d43-144">костфинализе</span><span class="sxs-lookup"><span data-stu-id="09d43-144">CostFinalize</span></span> | <span data-ttu-id="09d43-145">100</span><span class="sxs-lookup"><span data-stu-id="09d43-145">100</span></span>      |
| <span data-ttu-id="09d43-146">CA2</span><span class="sxs-lookup"><span data-stu-id="09d43-146">CA2</span></span>          | <span data-ttu-id="09d43-147">80</span><span class="sxs-lookup"><span data-stu-id="09d43-147">80</span></span>       |
| <span data-ttu-id="09d43-148">CA3</span><span class="sxs-lookup"><span data-stu-id="09d43-148">CA3</span></span>          | <span data-ttu-id="09d43-149">125</span><span class="sxs-lookup"><span data-stu-id="09d43-149">125</span></span>      |



 

<span data-ttu-id="09d43-150">Чтобы исправить ошибку для CA1, измените запись в ее исходном столбце в таблице CustomAction на существующую запись в таблице Directory или добавьте MyFolder в таблицу Directory.</span><span class="sxs-lookup"><span data-stu-id="09d43-150">To fix the error for CA1 change its entry in its Source column in the CustomAction table to an existing entry in the Directory table or add MyFolder to the Directory table.</span></span>

<span data-ttu-id="09d43-151">Чтобы исправить ошибку для CA2, измените ее последовательность в таблице Инсталлексекутесекуенце таким, чтобы она появилась после действия Костфинализе.</span><span class="sxs-lookup"><span data-stu-id="09d43-151">To fix the error for CA2, change its sequence in the InstallExecuteSequence table such that it comes after the CostFinalize action.</span></span>

<span data-ttu-id="09d43-152">Чтобы исправить ошибку для CA3, измените ее последовательность в таблице Инсталлексекутесекуенце таким, чтобы она наступила перед действием Костфинализе.</span><span class="sxs-lookup"><span data-stu-id="09d43-152">To fix the error for CA3, change its sequence in the InstallExecuteSequence table such that it comes before the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09d43-153">См. также</span><span class="sxs-lookup"><span data-stu-id="09d43-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09d43-154">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="09d43-154">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



