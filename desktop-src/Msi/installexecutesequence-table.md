---
description: В таблице Инсталлексекутесекуенце перечислены действия, выполняемые при выполнении действия по установке верхнего уровня.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Таблица Инсталлексекутесекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897110"
---
# <a name="installexecutesequence-table"></a><span data-ttu-id="7830f-103">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="7830f-103">InstallExecuteSequence Table</span></span>

<span data-ttu-id="7830f-104">В таблице Инсталлексекутесекуенце перечислены действия, выполняемые при выполнении [действия по установке](install-action.md) верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="7830f-104">The InstallExecuteSequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed.</span></span>

<span data-ttu-id="7830f-105">Действия в последовательности установки вплоть до [действия инсталлвалидате](installvalidate-action.md)и все диалоговые окна выхода находятся в [таблице инсталлуисекуенце](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="7830f-105">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="7830f-106">Все действия из Инсталлвалидате в конце последовательности установки находятся в таблице Инсталлексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="7830f-106">All actions from the InstallValidate through the end of the install sequence are in the InstallExecuteSequence table.</span></span> <span data-ttu-id="7830f-107">Так как таблица Инсталлексекутесекуенце должна быть изолированной, она имеет необходимые действия инициализации, такие как [лаунчкондитионс](launchconditions-action.md), [костинитиализе](costinitialize-action.md), [филекост](filecost-action.md)и [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7830f-107">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="7830f-108">[Настраиваемые действия](custom-actions.md) , для которых требуется пользовательский интерфейс, должны использовать [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) вместо созданных диалоговых окон, созданных с помощью [диалоговой таблицы](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="7830f-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="7830f-109">Таблица Инсталлексекутесекуенце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="7830f-109">The InstallExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="7830f-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="7830f-110">Column</span></span>    | <span data-ttu-id="7830f-111">Type</span><span class="sxs-lookup"><span data-stu-id="7830f-111">Type</span></span>                         | <span data-ttu-id="7830f-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="7830f-112">Key</span></span> | <span data-ttu-id="7830f-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="7830f-113">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="7830f-114">Действие</span><span class="sxs-lookup"><span data-stu-id="7830f-114">Action</span></span>    | [<span data-ttu-id="7830f-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7830f-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="7830f-116">Да</span><span class="sxs-lookup"><span data-stu-id="7830f-116">Y</span></span>   | <span data-ttu-id="7830f-117">Нет</span><span class="sxs-lookup"><span data-stu-id="7830f-117">N</span></span>        |
| <span data-ttu-id="7830f-118">Условие</span><span class="sxs-lookup"><span data-stu-id="7830f-118">Condition</span></span> | [<span data-ttu-id="7830f-119">Condition</span><span class="sxs-lookup"><span data-stu-id="7830f-119">Condition</span></span>](condition.md)   | <span data-ttu-id="7830f-120">Нет</span><span class="sxs-lookup"><span data-stu-id="7830f-120">N</span></span>   | <span data-ttu-id="7830f-121">Да</span><span class="sxs-lookup"><span data-stu-id="7830f-121">Y</span></span>        |
| <span data-ttu-id="7830f-122">Последовательность</span><span class="sxs-lookup"><span data-stu-id="7830f-122">Sequence</span></span>  | [<span data-ttu-id="7830f-123">Integer</span><span class="sxs-lookup"><span data-stu-id="7830f-123">Integer</span></span>](integer.md)       | <span data-ttu-id="7830f-124">Нет</span><span class="sxs-lookup"><span data-stu-id="7830f-124">N</span></span>   | <span data-ttu-id="7830f-125">Да</span><span class="sxs-lookup"><span data-stu-id="7830f-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7830f-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="7830f-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7830f-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="7830f-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="7830f-128">Имя выполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="7830f-128">Name of the action to execute.</span></span> <span data-ttu-id="7830f-129">Это либо встроенное действие, либо пользовательское действие.</span><span class="sxs-lookup"><span data-stu-id="7830f-129">This is either a built-in action or a custom action.</span></span>

<span data-ttu-id="7830f-130">Первичный ключ таблицы.</span><span class="sxs-lookup"><span data-stu-id="7830f-130">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="7830f-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="7830f-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="7830f-132">Это поле содержит условное выражение.</span><span class="sxs-lookup"><span data-stu-id="7830f-132">This field contains a conditional expression.</span></span> <span data-ttu-id="7830f-133">Если выражение принимает значение false, действие пропускается.</span><span class="sxs-lookup"><span data-stu-id="7830f-133">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="7830f-134">Если синтаксис выражения является недопустимым, последовательность завершается, возвращая Иесбадактиондата.</span><span class="sxs-lookup"><span data-stu-id="7830f-134">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="7830f-135">Дополнительные сведения о синтаксисе условных операторов см. в разделе [Синтаксис условных](conditional-statement-syntax.md)инструкций.</span><span class="sxs-lookup"><span data-stu-id="7830f-135">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="7830f-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="7830f-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="7830f-137">Число, определяющее расположение последовательности, в которой должно выполняться это действие.</span><span class="sxs-lookup"><span data-stu-id="7830f-137">Number that determines the sequence position in which this action is to be executed.</span></span>

<span data-ttu-id="7830f-138">Положительное значение представляет собой расположение последовательности.</span><span class="sxs-lookup"><span data-stu-id="7830f-138">A positive value represents the sequence position.</span></span> <span data-ttu-id="7830f-139">Значение NULL указывает, что действие не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7830f-139">A Null value indicates that the action is not executed.</span></span> <span data-ttu-id="7830f-140">Следующие отрицательные значения указывают, что это действие должно выполняться, если установщик возвращает соответствующий флаг завершения.</span><span class="sxs-lookup"><span data-stu-id="7830f-140">The following negative values indicate that this action is to be executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="7830f-141">Каждый флаг завершения (отрицательное значение) можно использовать без более чем одного действия.</span><span class="sxs-lookup"><span data-stu-id="7830f-141">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="7830f-142">Несколько действий могут иметь флаги завершения, но они должны быть разными флагами.</span><span class="sxs-lookup"><span data-stu-id="7830f-142">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="7830f-143">Флаги завершения (отрицательные значения) обычно используются с [диалоговыми окнами](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="7830f-143">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="7830f-144">Флаг завершения</span><span class="sxs-lookup"><span data-stu-id="7830f-144">Termination flag</span></span>          | <span data-ttu-id="7830f-145">Значение</span><span class="sxs-lookup"><span data-stu-id="7830f-145">Value</span></span> | <span data-ttu-id="7830f-146">Описание</span><span class="sxs-lookup"><span data-stu-id="7830f-146">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7830f-147">мсидоактионстатуссукцесс</span><span class="sxs-lookup"><span data-stu-id="7830f-147">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="7830f-148">-1</span><span class="sxs-lookup"><span data-stu-id="7830f-148">-1</span></span>    | <span data-ttu-id="7830f-149">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="7830f-149">Successful completion.</span></span> <span data-ttu-id="7830f-150">Используется с диалоговыми окнами [выхода](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="7830f-150">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="7830f-151">мсидоактионстатусусерексит</span><span class="sxs-lookup"><span data-stu-id="7830f-151">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="7830f-152">-2</span><span class="sxs-lookup"><span data-stu-id="7830f-152">-2</span></span>    | <span data-ttu-id="7830f-153">Пользователь завершает установку.</span><span class="sxs-lookup"><span data-stu-id="7830f-153">User terminates install.</span></span> <span data-ttu-id="7830f-154">Используется с диалоговыми окнами [усерексит](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="7830f-154">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="7830f-155">мсидоактионстатусфаилуре</span><span class="sxs-lookup"><span data-stu-id="7830f-155">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="7830f-156">–3</span><span class="sxs-lookup"><span data-stu-id="7830f-156">-3</span></span>    | <span data-ttu-id="7830f-157">Неустранимое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="7830f-157">Fatal exit terminates.</span></span> <span data-ttu-id="7830f-158">Используется с диалоговыми окнами [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="7830f-158">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="7830f-159">мсидоактионстатуссуспенд</span><span class="sxs-lookup"><span data-stu-id="7830f-159">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="7830f-160">–4</span><span class="sxs-lookup"><span data-stu-id="7830f-160">-4</span></span>    | <span data-ttu-id="7830f-161">Установка приостановлена.</span><span class="sxs-lookup"><span data-stu-id="7830f-161">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="7830f-162">Ноль, все остальные отрицательные числа или значение NULL указывают на то, что действие никогда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7830f-162">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7830f-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7830f-163">Remarks</span></span>

<span data-ttu-id="7830f-164">Локализованный текст, отображающий ход выполнения или ведение журнала, указывается в [таблице актионтекст](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="7830f-164">Localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="7830f-165">Пример таблицы последовательности см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="7830f-165">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="7830f-166">Проверка</span><span class="sxs-lookup"><span data-stu-id="7830f-166">Validation</span></span>

<dl>

[<span data-ttu-id="7830f-167">ICE03</span><span class="sxs-lookup"><span data-stu-id="7830f-167">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7830f-168">ICE06</span><span class="sxs-lookup"><span data-stu-id="7830f-168">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7830f-169">ICE12</span><span class="sxs-lookup"><span data-stu-id="7830f-169">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="7830f-170">ICE13</span><span class="sxs-lookup"><span data-stu-id="7830f-170">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="7830f-171">ICE26</span><span class="sxs-lookup"><span data-stu-id="7830f-171">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="7830f-172">ICE27</span><span class="sxs-lookup"><span data-stu-id="7830f-172">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="7830f-173">ICE28</span><span class="sxs-lookup"><span data-stu-id="7830f-173">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="7830f-174">ICE46</span><span class="sxs-lookup"><span data-stu-id="7830f-174">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="7830f-175">ICE63</span><span class="sxs-lookup"><span data-stu-id="7830f-175">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="7830f-176">ICE75</span><span class="sxs-lookup"><span data-stu-id="7830f-176">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="7830f-177">ICE77</span><span class="sxs-lookup"><span data-stu-id="7830f-177">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="7830f-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="7830f-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="7830f-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="7830f-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="7830f-180">ICE83</span><span class="sxs-lookup"><span data-stu-id="7830f-180">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="7830f-181">ICE84</span><span class="sxs-lookup"><span data-stu-id="7830f-181">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="7830f-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="7830f-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



