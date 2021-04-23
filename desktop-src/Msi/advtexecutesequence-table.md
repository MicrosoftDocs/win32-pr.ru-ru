---
description: В таблице Адвтексекутесекуенце перечислены действия, которые вызывает установщик при выполнении действия объявления верхнего уровня.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Таблица Адвтексекутесекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909123"
---
# <a name="advtexecutesequence-table"></a><span data-ttu-id="76ccd-103">Таблица Адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="76ccd-103">AdvtExecuteSequence Table</span></span>

<span data-ttu-id="76ccd-104">В таблице Адвтексекутесекуенце перечислены действия, которые вызывает установщик при выполнении [действия объявления](advertise-action.md) верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="76ccd-104">The AdvtExecuteSequence table lists actions the installer calls when the top-level [ADVERTISE action](advertise-action.md) is executed.</span></span>

<span data-ttu-id="76ccd-105">В таблице Адвтексекутесекуенце можно использовать только следующие действия.</span><span class="sxs-lookup"><span data-stu-id="76ccd-105">Only the following actions can be used in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="76ccd-106">В этой таблице нельзя использовать настраиваемые действия.</span><span class="sxs-lookup"><span data-stu-id="76ccd-106">Custom actions cannot be used in this table.</span></span>

[<span data-ttu-id="76ccd-107">костфинализе</span><span class="sxs-lookup"><span data-stu-id="76ccd-107">CostFinalize</span></span>](costfinalize-action.md)

[<span data-ttu-id="76ccd-108">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="76ccd-108">CostInitialize</span></span>](costinitialize-action.md)

[<span data-ttu-id="76ccd-109">креатешорткутс</span><span class="sxs-lookup"><span data-stu-id="76ccd-109">CreateShortcuts</span></span>](createshortcuts-action.md)

[<span data-ttu-id="76ccd-110">Функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="76ccd-110">InstallFinalize</span></span>](installfinalize-action.md)

[<span data-ttu-id="76ccd-111">инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="76ccd-111">InstallInitialize</span></span>](installinitialize-action.md)

[<span data-ttu-id="76ccd-112">инсталлвалидате</span><span class="sxs-lookup"><span data-stu-id="76ccd-112">InstallValidate</span></span>](installvalidate-action.md)

[<span data-ttu-id="76ccd-113">мсипублишассемблиес</span><span class="sxs-lookup"><span data-stu-id="76ccd-113">MsiPublishAssemblies</span></span>](msipublishassemblies-action.md)

[<span data-ttu-id="76ccd-114">публишкомпонентс</span><span class="sxs-lookup"><span data-stu-id="76ccd-114">PublishComponents</span></span>](publishcomponents-action.md)

[<span data-ttu-id="76ccd-115">публишфеатурес</span><span class="sxs-lookup"><span data-stu-id="76ccd-115">PublishFeatures</span></span>](publishfeatures-action.md)

[<span data-ttu-id="76ccd-116">публишпродукт</span><span class="sxs-lookup"><span data-stu-id="76ccd-116">PublishProduct</span></span>](publishproduct-action.md)

[<span data-ttu-id="76ccd-117">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="76ccd-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)

[<span data-ttu-id="76ccd-118">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="76ccd-118">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)

[<span data-ttu-id="76ccd-119">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="76ccd-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

[<span data-ttu-id="76ccd-120">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="76ccd-120">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="76ccd-121">Столбцы идентичны столбцам [таблицы инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="76ccd-121">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="76ccd-122">Таблица Адвтексекутесекуенце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="76ccd-122">The AdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="76ccd-123">Столбец</span><span class="sxs-lookup"><span data-stu-id="76ccd-123">Column</span></span>    | <span data-ttu-id="76ccd-124">Type</span><span class="sxs-lookup"><span data-stu-id="76ccd-124">Type</span></span>                         | <span data-ttu-id="76ccd-125">Ключ</span><span class="sxs-lookup"><span data-stu-id="76ccd-125">Key</span></span> | <span data-ttu-id="76ccd-126">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="76ccd-126">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="76ccd-127">Действие</span><span class="sxs-lookup"><span data-stu-id="76ccd-127">Action</span></span>    | [<span data-ttu-id="76ccd-128">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="76ccd-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="76ccd-129">Да</span><span class="sxs-lookup"><span data-stu-id="76ccd-129">Y</span></span>   | <span data-ttu-id="76ccd-130">Нет</span><span class="sxs-lookup"><span data-stu-id="76ccd-130">N</span></span>        |
| <span data-ttu-id="76ccd-131">Условие</span><span class="sxs-lookup"><span data-stu-id="76ccd-131">Condition</span></span> | [<span data-ttu-id="76ccd-132">Condition</span><span class="sxs-lookup"><span data-stu-id="76ccd-132">Condition</span></span>](condition.md)   | <span data-ttu-id="76ccd-133">Нет</span><span class="sxs-lookup"><span data-stu-id="76ccd-133">N</span></span>   | <span data-ttu-id="76ccd-134">Да</span><span class="sxs-lookup"><span data-stu-id="76ccd-134">Y</span></span>        |
| <span data-ttu-id="76ccd-135">Последовательность</span><span class="sxs-lookup"><span data-stu-id="76ccd-135">Sequence</span></span>  | [<span data-ttu-id="76ccd-136">Integer</span><span class="sxs-lookup"><span data-stu-id="76ccd-136">Integer</span></span>](integer.md)       | <span data-ttu-id="76ccd-137">Нет</span><span class="sxs-lookup"><span data-stu-id="76ccd-137">N</span></span>   | <span data-ttu-id="76ccd-138">Да</span><span class="sxs-lookup"><span data-stu-id="76ccd-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="76ccd-139">Столбцы</span><span class="sxs-lookup"><span data-stu-id="76ccd-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="76ccd-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="76ccd-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="76ccd-141">Имя [стандартного действия](standard-actions.md) , которое должен выполнить установщик.</span><span class="sxs-lookup"><span data-stu-id="76ccd-141">Name of the [standard action](standard-actions.md) the installer is to execute.</span></span> <span data-ttu-id="76ccd-142">Это первичный ключ таблицы.</span><span class="sxs-lookup"><span data-stu-id="76ccd-142">This is the primary key of the table.</span></span>

</dd> <dt>

<span data-ttu-id="76ccd-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="76ccd-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="76ccd-144">Логическое выражение.</span><span class="sxs-lookup"><span data-stu-id="76ccd-144">Logical expression.</span></span> <span data-ttu-id="76ccd-145">Если результат вычисления выражения равен false, действие пропускается.</span><span class="sxs-lookup"><span data-stu-id="76ccd-145">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="76ccd-146">Если синтаксис выражения недопустим, последовательность завершается, возвращая Иесбадактиондата.</span><span class="sxs-lookup"><span data-stu-id="76ccd-146">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="76ccd-147">Дополнительные сведения о синтаксисе условных операторов см. в разделе [Синтаксис условных](conditional-statement-syntax.md)инструкций.</span><span class="sxs-lookup"><span data-stu-id="76ccd-147">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="76ccd-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="76ccd-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="76ccd-149">Положительное значение указывает на расположение последовательности действия.</span><span class="sxs-lookup"><span data-stu-id="76ccd-149">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="76ccd-150">Следующие отрицательные значения указывают, что действие вызывается, если установщик возвращает флаг завершения.</span><span class="sxs-lookup"><span data-stu-id="76ccd-150">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="76ccd-151">Каждый флаг завершения (отрицательное значение) можно использовать без более чем одного действия.</span><span class="sxs-lookup"><span data-stu-id="76ccd-151">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="76ccd-152">Несколько действий могут иметь флаги завершения, но они должны быть разными флагами.</span><span class="sxs-lookup"><span data-stu-id="76ccd-152">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="76ccd-153">Флаги завершения (отрицательные значения) обычно используются с [диалоговыми окнами](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="76ccd-153">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="76ccd-154">Флаг завершения</span><span class="sxs-lookup"><span data-stu-id="76ccd-154">Termination flag</span></span>          | <span data-ttu-id="76ccd-155">Значение</span><span class="sxs-lookup"><span data-stu-id="76ccd-155">Value</span></span> | <span data-ttu-id="76ccd-156">Описание</span><span class="sxs-lookup"><span data-stu-id="76ccd-156">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76ccd-157">мсидоактионстатуссукцесс</span><span class="sxs-lookup"><span data-stu-id="76ccd-157">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="76ccd-158">-1</span><span class="sxs-lookup"><span data-stu-id="76ccd-158">-1</span></span>    | <span data-ttu-id="76ccd-159">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="76ccd-159">Successful completion.</span></span> <span data-ttu-id="76ccd-160">Используется с диалоговыми окнами [выхода](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="76ccd-160">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="76ccd-161">мсидоактионстатусусерексит</span><span class="sxs-lookup"><span data-stu-id="76ccd-161">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="76ccd-162">-2</span><span class="sxs-lookup"><span data-stu-id="76ccd-162">-2</span></span>    | <span data-ttu-id="76ccd-163">Пользователь завершает установку.</span><span class="sxs-lookup"><span data-stu-id="76ccd-163">User terminates install.</span></span> <span data-ttu-id="76ccd-164">Используется с диалоговыми окнами [усерексит](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="76ccd-164">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="76ccd-165">мсидоактионстатусфаилуре</span><span class="sxs-lookup"><span data-stu-id="76ccd-165">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="76ccd-166">–3</span><span class="sxs-lookup"><span data-stu-id="76ccd-166">-3</span></span>    | <span data-ttu-id="76ccd-167">Неустранимое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="76ccd-167">Fatal exit terminates.</span></span> <span data-ttu-id="76ccd-168">Используется с диалоговыми окнами [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="76ccd-168">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="76ccd-169">мсидоактионстатуссуспенд</span><span class="sxs-lookup"><span data-stu-id="76ccd-169">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="76ccd-170">–4</span><span class="sxs-lookup"><span data-stu-id="76ccd-170">-4</span></span>    | <span data-ttu-id="76ccd-171">Установка приостановлена.</span><span class="sxs-lookup"><span data-stu-id="76ccd-171">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="76ccd-172">Ноль, все остальные отрицательные числа или значение NULL указывают на то, что действие никогда не вызывается.</span><span class="sxs-lookup"><span data-stu-id="76ccd-172">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="76ccd-173">Проверка</span><span class="sxs-lookup"><span data-stu-id="76ccd-173">Validation</span></span>

<dl>

[<span data-ttu-id="76ccd-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="76ccd-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="76ccd-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="76ccd-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="76ccd-176">ICE12</span><span class="sxs-lookup"><span data-stu-id="76ccd-176">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="76ccd-177">ICE13</span><span class="sxs-lookup"><span data-stu-id="76ccd-177">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="76ccd-178">ICE27</span><span class="sxs-lookup"><span data-stu-id="76ccd-178">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="76ccd-179">ICE46</span><span class="sxs-lookup"><span data-stu-id="76ccd-179">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="76ccd-180">ICE72</span><span class="sxs-lookup"><span data-stu-id="76ccd-180">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="76ccd-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="76ccd-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="76ccd-182">ICE82</span><span class="sxs-lookup"><span data-stu-id="76ccd-182">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="76ccd-183">ICE83</span><span class="sxs-lookup"><span data-stu-id="76ccd-183">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="76ccd-184">ICE84</span><span class="sxs-lookup"><span data-stu-id="76ccd-184">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="76ccd-185">ICE86</span><span class="sxs-lookup"><span data-stu-id="76ccd-185">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="76ccd-186">ICEM04</span><span class="sxs-lookup"><span data-stu-id="76ccd-186">ICEM04</span></span>](icem04.md)  
</dl>

 

 



