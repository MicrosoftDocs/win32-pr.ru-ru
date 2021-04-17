---
description: В таблице Инсталлуисекуенце перечислены действия, выполняемые при выполнении действия по установке верхнего уровня, а для внутреннего уровня пользовательского интерфейса — полный пользовательский интерфейс или сокращенный пользовательский интерфейс.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Таблица Инсталлуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684237"
---
# <a name="installuisequence-table"></a><span data-ttu-id="2fbe3-103">Таблица Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="2fbe3-103">InstallUISequence Table</span></span>

<span data-ttu-id="2fbe3-104">В таблице Инсталлуисекуенце перечислены действия, выполняемые при выполнении [действия по установке](install-action.md) верхнего уровня, а для внутреннего уровня пользовательского интерфейса — полный пользовательский интерфейс или СОКРАЩЕНный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-104">The InstallUISequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="2fbe3-105">Установщик пропускает действия в этой таблице, если на уровне пользовательского интерфейса задан базовый пользовательский интерфейс или нет пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="2fbe3-106">См. [сведения о пользовательском интерфейсе](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="2fbe3-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="2fbe3-107">Действия в последовательности установки вплоть до [действия инсталлвалидате](installvalidate-action.md)и диалоговых окон выхода находятся в таблице инсталлуисекуенце.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-107">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and the exit dialog boxes, are located in the InstallUISequence table.</span></span> <span data-ttu-id="2fbe3-108">Все действия из Инсталлвалидате в конце последовательности установки находятся в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fbe3-108">All actions from the InstallValidate through the end of the install sequence are in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="2fbe3-109">Так как таблица Инсталлексекутесекуенце должна быть изолированной, она имеет необходимые действия инициализации, такие как [лаунчкондитионс](launchconditions-action.md), [костинитиализе](costinitialize-action.md), [филекост](filecost-action.md)и [костфинализе](costfinalize-action.md), а также [действие ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="2fbe3-109">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and the [CostFinalize](costfinalize-action.md), and [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="2fbe3-110">Таблица Инсталлуисекуенце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-110">The InstallUISequence table has the following columns.</span></span>



| <span data-ttu-id="2fbe3-111">Столбец</span><span class="sxs-lookup"><span data-stu-id="2fbe3-111">Column</span></span>    | <span data-ttu-id="2fbe3-112">Type</span><span class="sxs-lookup"><span data-stu-id="2fbe3-112">Type</span></span>                         | <span data-ttu-id="2fbe3-113">Ключ</span><span class="sxs-lookup"><span data-stu-id="2fbe3-113">Key</span></span> | <span data-ttu-id="2fbe3-114">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="2fbe3-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="2fbe3-115">Действие</span><span class="sxs-lookup"><span data-stu-id="2fbe3-115">Action</span></span>    | [<span data-ttu-id="2fbe3-116">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="2fbe3-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="2fbe3-117">Да</span><span class="sxs-lookup"><span data-stu-id="2fbe3-117">Y</span></span>   | <span data-ttu-id="2fbe3-118">Нет</span><span class="sxs-lookup"><span data-stu-id="2fbe3-118">N</span></span>        |
| <span data-ttu-id="2fbe3-119">Условие</span><span class="sxs-lookup"><span data-stu-id="2fbe3-119">Condition</span></span> | [<span data-ttu-id="2fbe3-120">Condition</span><span class="sxs-lookup"><span data-stu-id="2fbe3-120">Condition</span></span>](condition.md)   | <span data-ttu-id="2fbe3-121">Нет</span><span class="sxs-lookup"><span data-stu-id="2fbe3-121">N</span></span>   | <span data-ttu-id="2fbe3-122">Да</span><span class="sxs-lookup"><span data-stu-id="2fbe3-122">Y</span></span>        |
| <span data-ttu-id="2fbe3-123">Последовательность</span><span class="sxs-lookup"><span data-stu-id="2fbe3-123">Sequence</span></span>  | [<span data-ttu-id="2fbe3-124">Integer</span><span class="sxs-lookup"><span data-stu-id="2fbe3-124">Integer</span></span>](integer.md)       | <span data-ttu-id="2fbe3-125">Нет</span><span class="sxs-lookup"><span data-stu-id="2fbe3-125">N</span></span>   | <span data-ttu-id="2fbe3-126">Да</span><span class="sxs-lookup"><span data-stu-id="2fbe3-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2fbe3-127">Столбцы</span><span class="sxs-lookup"><span data-stu-id="2fbe3-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2fbe3-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="2fbe3-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="2fbe3-129">Имя выполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-129">Name of the action to execute.</span></span> <span data-ttu-id="2fbe3-130">Это либо встроенное действие, пользовательское действие, либо мастер пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-130">This is either a built-in action, a custom action, or a user interface wizard.</span></span>

<span data-ttu-id="2fbe3-131">Первичный ключ таблицы.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="2fbe3-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="2fbe3-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="2fbe3-133">Это поле содержит условное выражение.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-133">This field contains a conditional expression.</span></span> <span data-ttu-id="2fbe3-134">Если выражение принимает значение false, действие пропускается.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-134">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="2fbe3-135">Если синтаксис выражения является недопустимым, последовательность завершается, возвращая Иесбадактиондата.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-135">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="2fbe3-136">Дополнительные сведения о синтаксисе условных операторов см. в разделе [Синтаксис условных](conditional-statement-syntax.md)инструкций.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-136">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fbe3-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="2fbe3-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="2fbe3-138">Число в этом столбце определяет расположение последовательности, в которой выполняется это действие.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-138">The number in this column determines the sequence position in which this action is run.</span></span>

<span data-ttu-id="2fbe3-139">Положительное значение представляет собой расположение последовательности.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-139">A positive value represents the sequence position.</span></span> <span data-ttu-id="2fbe3-140">Значение NULL указывает, что действие никогда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-140">A Null value indicates that the action is never run.</span></span> <span data-ttu-id="2fbe3-141">Следующие отрицательные значения указывают на то, что это действие выполняется, если установщик возвращает соответствующий флаг завершения.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-141">The following negative values indicate that this action is executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="2fbe3-142">Каждый флаг завершения (отрицательное значение) можно использовать без более чем одного действия.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="2fbe3-143">Несколько действий могут иметь флаги завершения, но они должны быть разными флагами.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="2fbe3-144">Флаги завершения (отрицательные значения) обычно используются с [диалоговыми окнами](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="2fbe3-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="2fbe3-145">Флаг завершения</span><span class="sxs-lookup"><span data-stu-id="2fbe3-145">Termination flag</span></span>          | <span data-ttu-id="2fbe3-146">Значение</span><span class="sxs-lookup"><span data-stu-id="2fbe3-146">Value</span></span> | <span data-ttu-id="2fbe3-147">Описание</span><span class="sxs-lookup"><span data-stu-id="2fbe3-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2fbe3-148">мсидоактионстатуссукцесс</span><span class="sxs-lookup"><span data-stu-id="2fbe3-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="2fbe3-149">-1</span><span class="sxs-lookup"><span data-stu-id="2fbe3-149">-1</span></span>    | <span data-ttu-id="2fbe3-150">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-150">Successful completion.</span></span> <span data-ttu-id="2fbe3-151">Используется с диалоговыми окнами [выхода](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2fbe3-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="2fbe3-152">мсидоактионстатусусерексит</span><span class="sxs-lookup"><span data-stu-id="2fbe3-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="2fbe3-153">-2</span><span class="sxs-lookup"><span data-stu-id="2fbe3-153">-2</span></span>    | <span data-ttu-id="2fbe3-154">Пользователь завершает установку.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-154">User terminates install.</span></span> <span data-ttu-id="2fbe3-155">Используется с диалоговыми окнами [усерексит](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2fbe3-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="2fbe3-156">мсидоактионстатусфаилуре</span><span class="sxs-lookup"><span data-stu-id="2fbe3-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="2fbe3-157">–3</span><span class="sxs-lookup"><span data-stu-id="2fbe3-157">-3</span></span>    | <span data-ttu-id="2fbe3-158">Неустранимое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-158">Fatal exit terminates.</span></span> <span data-ttu-id="2fbe3-159">Используется с диалоговыми окнами [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2fbe3-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="2fbe3-160">мсидоактионстатуссуспенд</span><span class="sxs-lookup"><span data-stu-id="2fbe3-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="2fbe3-161">–4</span><span class="sxs-lookup"><span data-stu-id="2fbe3-161">-4</span></span>    | <span data-ttu-id="2fbe3-162">Установка приостановлена.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="2fbe3-163">Ноль, все остальные отрицательные числа или значение NULL указывают на то, что действие никогда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fbe3-163">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fbe3-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2fbe3-164">Remarks</span></span>

<span data-ttu-id="2fbe3-165">Связанный локализованный текст для просмотра хода выполнения или ведения журнала указывается в [таблице актионтекст](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fbe3-165">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="2fbe3-166">Пример таблицы последовательности см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fbe3-166">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="2fbe3-167">Проверка</span><span class="sxs-lookup"><span data-stu-id="2fbe3-167">Validation</span></span>

<dl>

[<span data-ttu-id="2fbe3-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="2fbe3-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2fbe3-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="2fbe3-169">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2fbe3-170">ICE12</span><span class="sxs-lookup"><span data-stu-id="2fbe3-170">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="2fbe3-171">ICE13</span><span class="sxs-lookup"><span data-stu-id="2fbe3-171">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="2fbe3-172">ICE20</span><span class="sxs-lookup"><span data-stu-id="2fbe3-172">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="2fbe3-173">ICE26</span><span class="sxs-lookup"><span data-stu-id="2fbe3-173">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="2fbe3-174">ICE27</span><span class="sxs-lookup"><span data-stu-id="2fbe3-174">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="2fbe3-175">ICE28</span><span class="sxs-lookup"><span data-stu-id="2fbe3-175">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="2fbe3-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="2fbe3-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="2fbe3-177">ICE75</span><span class="sxs-lookup"><span data-stu-id="2fbe3-177">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="2fbe3-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="2fbe3-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="2fbe3-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="2fbe3-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="2fbe3-180">ICE86</span><span class="sxs-lookup"><span data-stu-id="2fbe3-180">ICE86</span></span>](ice86.md)  
</dl>

 

 



