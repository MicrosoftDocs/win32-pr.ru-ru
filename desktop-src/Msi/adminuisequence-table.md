---
description: В таблице Админуисекуенце перечислены действия, которые установщик вызывает последовательно, когда выполняется АДМИНИСТРАТИВное действие верхнего уровня и уровень внутреннего пользовательского интерфейса настроен на полный пользовательский интерфейс или ограниченный пользовательский интерфейс.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Таблица Админуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650735"
---
# <a name="adminuisequence-table"></a><span data-ttu-id="5f496-103">Таблица Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="5f496-103">AdminUISequence Table</span></span>

<span data-ttu-id="5f496-104">В таблице Админуисекуенце перечислены действия, которые установщик вызывает последовательно, когда выполняется [Административное действие](admin-action.md) верхнего уровня и уровень внутреннего пользовательского интерфейса настроен на полный пользовательский интерфейс или ОГРАНИЧЕНный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5f496-104">The AdminUISequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="5f496-105">Установщик пропускает действия в этой таблице, если на уровне пользовательского интерфейса задан базовый пользовательский интерфейс или нет пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5f496-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="5f496-106">См. [сведения о пользовательском интерфейсе](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="5f496-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="5f496-107">Действия администратора в последовательности установки до [действия инсталлвалидате](installvalidate-action.md)и всех диалоговых окон выхода находятся в таблице админуисекуенце.</span><span class="sxs-lookup"><span data-stu-id="5f496-107">ADMIN actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the AdminUISequence table.</span></span> <span data-ttu-id="5f496-108">Все действия из Инсталлвалидате в конце последовательности установки находятся в [таблице админексекутесекуенце](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="5f496-108">All actions from the InstallValidate through the end of the install sequence are in the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="5f496-109">Так как таблица Админексекутесекуенце должна быть изолированной, она также содержит все необходимые действия инициализации, такие как [лаунчкондитионс](launchconditions-action.md), [костинитиализе](costinitialize-action.md), [филекост](filecost-action.md)и [костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="5f496-109">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span> <span data-ttu-id="5f496-110">У него также есть [действие ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="5f496-110">It also has the [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="5f496-111">Столбцы идентичны столбцам [таблицы инсталлуисекуенце](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="5f496-111">The columns are identical to those of the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="5f496-112">Таблица Админуисекуенце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="5f496-112">The AdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="5f496-113">Столбец</span><span class="sxs-lookup"><span data-stu-id="5f496-113">Column</span></span>    | <span data-ttu-id="5f496-114">Type</span><span class="sxs-lookup"><span data-stu-id="5f496-114">Type</span></span>                         | <span data-ttu-id="5f496-115">Ключ</span><span class="sxs-lookup"><span data-stu-id="5f496-115">Key</span></span> | <span data-ttu-id="5f496-116">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="5f496-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="5f496-117">Действие</span><span class="sxs-lookup"><span data-stu-id="5f496-117">Action</span></span>    | [<span data-ttu-id="5f496-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="5f496-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="5f496-119">Да</span><span class="sxs-lookup"><span data-stu-id="5f496-119">Y</span></span>   | <span data-ttu-id="5f496-120">Нет</span><span class="sxs-lookup"><span data-stu-id="5f496-120">N</span></span>        |
| <span data-ttu-id="5f496-121">Условие</span><span class="sxs-lookup"><span data-stu-id="5f496-121">Condition</span></span> | [<span data-ttu-id="5f496-122">Condition</span><span class="sxs-lookup"><span data-stu-id="5f496-122">Condition</span></span>](condition.md)   | <span data-ttu-id="5f496-123">Нет</span><span class="sxs-lookup"><span data-stu-id="5f496-123">N</span></span>   | <span data-ttu-id="5f496-124">Да</span><span class="sxs-lookup"><span data-stu-id="5f496-124">Y</span></span>        |
| <span data-ttu-id="5f496-125">Последовательность</span><span class="sxs-lookup"><span data-stu-id="5f496-125">Sequence</span></span>  | [<span data-ttu-id="5f496-126">Integer</span><span class="sxs-lookup"><span data-stu-id="5f496-126">Integer</span></span>](integer.md)       | <span data-ttu-id="5f496-127">Нет</span><span class="sxs-lookup"><span data-stu-id="5f496-127">N</span></span>   | <span data-ttu-id="5f496-128">Да</span><span class="sxs-lookup"><span data-stu-id="5f496-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5f496-129">Столбцы</span><span class="sxs-lookup"><span data-stu-id="5f496-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5f496-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="5f496-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="5f496-131">Имя выполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="5f496-131">Name of the action to execute.</span></span> <span data-ttu-id="5f496-132">Это либо стандартное действие, мастер пользовательского интерфейса, либо пользовательское действие, указанное в [таблице CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="5f496-132">This is either a standard action, a user interface wizard, or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="5f496-133">Первичный ключ таблицы.</span><span class="sxs-lookup"><span data-stu-id="5f496-133">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="5f496-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="5f496-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="5f496-135">Логическое выражение.</span><span class="sxs-lookup"><span data-stu-id="5f496-135">Logical expression.</span></span> <span data-ttu-id="5f496-136">Если результат вычисления выражения равен false, действие пропускается.</span><span class="sxs-lookup"><span data-stu-id="5f496-136">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="5f496-137">Если синтаксис выражения недопустим, последовательность завершается, возвращая Иесбадактиондата.</span><span class="sxs-lookup"><span data-stu-id="5f496-137">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="5f496-138">Дополнительные сведения о синтаксисе условных операторов см. в разделе [Синтаксис условных](conditional-statement-syntax.md)инструкций.</span><span class="sxs-lookup"><span data-stu-id="5f496-138">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f496-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="5f496-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="5f496-140">Положительное значение указывает на расположение последовательности действия.</span><span class="sxs-lookup"><span data-stu-id="5f496-140">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="5f496-141">Следующие отрицательные значения указывают, что действие вызывается, если установщик возвращает флаг завершения.</span><span class="sxs-lookup"><span data-stu-id="5f496-141">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="5f496-142">Каждый флаг завершения (отрицательное значение) можно использовать без более чем одного действия.</span><span class="sxs-lookup"><span data-stu-id="5f496-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="5f496-143">Несколько действий могут иметь флаги завершения, но они должны быть разными флагами.</span><span class="sxs-lookup"><span data-stu-id="5f496-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="5f496-144">Флаги завершения (отрицательные значения) обычно используются с [диалоговыми окнами](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="5f496-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="5f496-145">Флаг завершения</span><span class="sxs-lookup"><span data-stu-id="5f496-145">Termination flag</span></span>          | <span data-ttu-id="5f496-146">Значение</span><span class="sxs-lookup"><span data-stu-id="5f496-146">Value</span></span> | <span data-ttu-id="5f496-147">Описание</span><span class="sxs-lookup"><span data-stu-id="5f496-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5f496-148">мсидоактионстатуссукцесс</span><span class="sxs-lookup"><span data-stu-id="5f496-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="5f496-149">-1</span><span class="sxs-lookup"><span data-stu-id="5f496-149">-1</span></span>    | <span data-ttu-id="5f496-150">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="5f496-150">Successful completion.</span></span> <span data-ttu-id="5f496-151">Используется с диалоговыми окнами [выхода](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="5f496-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="5f496-152">мсидоактионстатусусерексит</span><span class="sxs-lookup"><span data-stu-id="5f496-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="5f496-153">-2</span><span class="sxs-lookup"><span data-stu-id="5f496-153">-2</span></span>    | <span data-ttu-id="5f496-154">Пользователь завершает установку.</span><span class="sxs-lookup"><span data-stu-id="5f496-154">User terminates install.</span></span> <span data-ttu-id="5f496-155">Используется с диалоговыми окнами [усерексит](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="5f496-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="5f496-156">мсидоактионстатусфаилуре</span><span class="sxs-lookup"><span data-stu-id="5f496-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="5f496-157">–3</span><span class="sxs-lookup"><span data-stu-id="5f496-157">-3</span></span>    | <span data-ttu-id="5f496-158">Неустранимое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="5f496-158">Fatal exit terminates.</span></span> <span data-ttu-id="5f496-159">Используется с диалоговыми окнами [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="5f496-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="5f496-160">мсидоактионстатуссуспенд</span><span class="sxs-lookup"><span data-stu-id="5f496-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="5f496-161">–4</span><span class="sxs-lookup"><span data-stu-id="5f496-161">-4</span></span>    | <span data-ttu-id="5f496-162">Установка приостановлена.</span><span class="sxs-lookup"><span data-stu-id="5f496-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="5f496-163">Ноль, все остальные отрицательные числа или значение NULL указывают на то, что действие никогда не вызывается.</span><span class="sxs-lookup"><span data-stu-id="5f496-163">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="5f496-164">Проверка</span><span class="sxs-lookup"><span data-stu-id="5f496-164">Validation</span></span>

<dl>

[<span data-ttu-id="5f496-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="5f496-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5f496-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="5f496-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5f496-167">ICE12</span><span class="sxs-lookup"><span data-stu-id="5f496-167">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="5f496-168">ICE13</span><span class="sxs-lookup"><span data-stu-id="5f496-168">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="5f496-169">ICE20</span><span class="sxs-lookup"><span data-stu-id="5f496-169">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="5f496-170">ICE26</span><span class="sxs-lookup"><span data-stu-id="5f496-170">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="5f496-171">ICE27</span><span class="sxs-lookup"><span data-stu-id="5f496-171">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="5f496-172">ICE28</span><span class="sxs-lookup"><span data-stu-id="5f496-172">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="5f496-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="5f496-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="5f496-174">ICE75</span><span class="sxs-lookup"><span data-stu-id="5f496-174">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="5f496-175">ICE79</span><span class="sxs-lookup"><span data-stu-id="5f496-175">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="5f496-176">ICE82</span><span class="sxs-lookup"><span data-stu-id="5f496-176">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="5f496-177">ICE84</span><span class="sxs-lookup"><span data-stu-id="5f496-177">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="5f496-178">ICE86</span><span class="sxs-lookup"><span data-stu-id="5f496-178">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="5f496-179">ICE96</span><span class="sxs-lookup"><span data-stu-id="5f496-179">ICE96</span></span>](ice96.md)  
[<span data-ttu-id="5f496-180">ICEM04</span><span class="sxs-lookup"><span data-stu-id="5f496-180">ICEM04</span></span>](icem04.md)  
</dl>

 

 



