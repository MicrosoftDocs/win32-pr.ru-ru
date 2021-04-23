---
description: В таблице Админексекутесекуенце перечислены действия, которые установщик вызывает последовательно при выполнении действия администратора верхнего уровня.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Таблица Админексекутесекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662957"
---
# <a name="adminexecutesequence-table"></a><span data-ttu-id="aa7fa-103">Таблица Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="aa7fa-103">AdminExecuteSequence Table</span></span>

<span data-ttu-id="aa7fa-104">В таблице Админексекутесекуенце перечислены действия, которые установщик вызывает последовательно при выполнении [действия администратора](admin-action.md) верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-104">The AdminExecuteSequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed.</span></span>

<span data-ttu-id="aa7fa-105">Действия администратора в последовательности установки вплоть до [действий инсталлвалидате](installvalidate-action.md) и любые диалоговые окна выхода находятся в [таблице админуисекуенце](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa7fa-105">ADMIN actions in the install sequence, up to the [InstallValidate action](installvalidate-action.md) and any exit dialog boxes, are located in the [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="aa7fa-106">Действия администратора из действия Инсталлвалидате в конце последовательности установки находятся в таблице Админексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-106">ADMIN actions from the InstallValidate action through the end of the install sequence are in the AdminExecuteSequence table.</span></span> <span data-ttu-id="aa7fa-107">Так как таблица Админексекутесекуенце должна быть изолированной, она также содержит все необходимые действия инициализации, такие как [лаунчкондитионс](launchconditions-action.md), [костинитиализе](costinitialize-action.md), [филекост](filecost-action.md)и [костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="aa7fa-107">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span>

<span data-ttu-id="aa7fa-108">[Настраиваемые действия](custom-actions.md) , для которых требуется пользовательский интерфейс, должны использовать [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) вместо созданных диалоговых окон, созданных с помощью [диалоговой таблицы](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa7fa-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="aa7fa-109">Столбцы идентичны столбцам [таблицы инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa7fa-109">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="aa7fa-110">Таблица Админексекутесекуенце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-110">The AdminExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="aa7fa-111">Столбец</span><span class="sxs-lookup"><span data-stu-id="aa7fa-111">Column</span></span>    | <span data-ttu-id="aa7fa-112">Type</span><span class="sxs-lookup"><span data-stu-id="aa7fa-112">Type</span></span>                         | <span data-ttu-id="aa7fa-113">Ключ</span><span class="sxs-lookup"><span data-stu-id="aa7fa-113">Key</span></span> | <span data-ttu-id="aa7fa-114">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="aa7fa-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="aa7fa-115">Действие</span><span class="sxs-lookup"><span data-stu-id="aa7fa-115">Action</span></span>    | [<span data-ttu-id="aa7fa-116">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="aa7fa-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="aa7fa-117">Да</span><span class="sxs-lookup"><span data-stu-id="aa7fa-117">Y</span></span>   | <span data-ttu-id="aa7fa-118">Нет</span><span class="sxs-lookup"><span data-stu-id="aa7fa-118">N</span></span>        |
| <span data-ttu-id="aa7fa-119">Условие</span><span class="sxs-lookup"><span data-stu-id="aa7fa-119">Condition</span></span> | [<span data-ttu-id="aa7fa-120">Condition</span><span class="sxs-lookup"><span data-stu-id="aa7fa-120">Condition</span></span>](condition.md)   | <span data-ttu-id="aa7fa-121">Нет</span><span class="sxs-lookup"><span data-stu-id="aa7fa-121">N</span></span>   | <span data-ttu-id="aa7fa-122">Да</span><span class="sxs-lookup"><span data-stu-id="aa7fa-122">Y</span></span>        |
| <span data-ttu-id="aa7fa-123">Последовательность</span><span class="sxs-lookup"><span data-stu-id="aa7fa-123">Sequence</span></span>  | [<span data-ttu-id="aa7fa-124">Integer</span><span class="sxs-lookup"><span data-stu-id="aa7fa-124">Integer</span></span>](integer.md)       | <span data-ttu-id="aa7fa-125">Нет</span><span class="sxs-lookup"><span data-stu-id="aa7fa-125">N</span></span>   | <span data-ttu-id="aa7fa-126">Да</span><span class="sxs-lookup"><span data-stu-id="aa7fa-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="aa7fa-127">Столбцы</span><span class="sxs-lookup"><span data-stu-id="aa7fa-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="aa7fa-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="aa7fa-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="aa7fa-129">Имя выполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-129">Name of the action to execute.</span></span> <span data-ttu-id="aa7fa-130">Это либо стандартное действие, либо пользовательское действие, указанное в [таблице CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa7fa-130">This is either a standard action or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="aa7fa-131">Первичный ключ таблицы.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="aa7fa-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="aa7fa-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="aa7fa-133">Логическое выражение.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-133">Logical expression.</span></span> <span data-ttu-id="aa7fa-134">Если результат вычисления выражения равен false, действие пропускается.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-134">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="aa7fa-135">Если синтаксис выражения недопустим, последовательность завершается, возвращая Иесбадактиондата.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-135">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="aa7fa-136">Сведения о синтаксисе условных операторов см. в разделе [Синтаксис условных](conditional-statement-syntax.md)инструкций.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-136">For information on the syntax of conditional statements see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7fa-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="aa7fa-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="aa7fa-138">Положительное значение указывает на расположение последовательности действия.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-138">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="aa7fa-139">Следующие отрицательные значения указывают, что действие вызывается, если установщик возвращает флаг завершения.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-139">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="aa7fa-140">Каждый флаг завершения (отрицательное значение) можно использовать без более чем одного действия.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-140">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="aa7fa-141">Несколько действий могут иметь флаги завершения, но они должны быть разными флагами.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-141">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="aa7fa-142">Флаги завершения (отрицательные значения) обычно используются с [диалоговыми окнами](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="aa7fa-142">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="aa7fa-143">Флаг завершения</span><span class="sxs-lookup"><span data-stu-id="aa7fa-143">Termination flag</span></span>          | <span data-ttu-id="aa7fa-144">Значение</span><span class="sxs-lookup"><span data-stu-id="aa7fa-144">Value</span></span> | <span data-ttu-id="aa7fa-145">Описание</span><span class="sxs-lookup"><span data-stu-id="aa7fa-145">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7fa-146">мсидоактионстатуссукцесс</span><span class="sxs-lookup"><span data-stu-id="aa7fa-146">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="aa7fa-147">-1</span><span class="sxs-lookup"><span data-stu-id="aa7fa-147">-1</span></span>    | <span data-ttu-id="aa7fa-148">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-148">Successful completion.</span></span> <span data-ttu-id="aa7fa-149">Используется с диалоговыми окнами [выхода](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="aa7fa-149">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="aa7fa-150">мсидоактионстатусусерексит</span><span class="sxs-lookup"><span data-stu-id="aa7fa-150">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="aa7fa-151">-2</span><span class="sxs-lookup"><span data-stu-id="aa7fa-151">-2</span></span>    | <span data-ttu-id="aa7fa-152">Пользователь завершает установку.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-152">User terminates install.</span></span> <span data-ttu-id="aa7fa-153">Используется с диалоговыми окнами [усерексит](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="aa7fa-153">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="aa7fa-154">мсидоактионстатусфаилуре</span><span class="sxs-lookup"><span data-stu-id="aa7fa-154">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="aa7fa-155">–3</span><span class="sxs-lookup"><span data-stu-id="aa7fa-155">-3</span></span>    | <span data-ttu-id="aa7fa-156">Неустранимое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-156">Fatal exit terminates.</span></span> <span data-ttu-id="aa7fa-157">Используется с диалоговыми окнами [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="aa7fa-157">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="aa7fa-158">мсидоактионстатуссуспенд</span><span class="sxs-lookup"><span data-stu-id="aa7fa-158">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="aa7fa-159">–4</span><span class="sxs-lookup"><span data-stu-id="aa7fa-159">-4</span></span>    | <span data-ttu-id="aa7fa-160">Установка приостановлена.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-160">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="aa7fa-161">Ноль, все остальные отрицательные числа или значение NULL указывают на то, что действие никогда не вызывается.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-161">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="aa7fa-162">Проверка</span><span class="sxs-lookup"><span data-stu-id="aa7fa-162">Validation</span></span>

<dl>

[<span data-ttu-id="aa7fa-163">ICE03</span><span class="sxs-lookup"><span data-stu-id="aa7fa-163">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="aa7fa-164">ICE06</span><span class="sxs-lookup"><span data-stu-id="aa7fa-164">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="aa7fa-165">ICE12</span><span class="sxs-lookup"><span data-stu-id="aa7fa-165">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="aa7fa-166">ICE13</span><span class="sxs-lookup"><span data-stu-id="aa7fa-166">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="aa7fa-167">ICE26</span><span class="sxs-lookup"><span data-stu-id="aa7fa-167">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="aa7fa-168">ICE27</span><span class="sxs-lookup"><span data-stu-id="aa7fa-168">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="aa7fa-169">ICE28</span><span class="sxs-lookup"><span data-stu-id="aa7fa-169">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="aa7fa-170">ICE75</span><span class="sxs-lookup"><span data-stu-id="aa7fa-170">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="aa7fa-171">ICE77</span><span class="sxs-lookup"><span data-stu-id="aa7fa-171">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="aa7fa-172">ICE79</span><span class="sxs-lookup"><span data-stu-id="aa7fa-172">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="aa7fa-173">ICE82</span><span class="sxs-lookup"><span data-stu-id="aa7fa-173">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="aa7fa-174">ICE84</span><span class="sxs-lookup"><span data-stu-id="aa7fa-174">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="aa7fa-175">ICE86</span><span class="sxs-lookup"><span data-stu-id="aa7fa-175">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="aa7fa-176">ICEM04</span><span class="sxs-lookup"><span data-stu-id="aa7fa-176">ICEM04</span></span>](icem04.md)  
</dl>

 

 



