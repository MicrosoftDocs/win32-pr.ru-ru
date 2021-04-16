---
description: Ниже приведен пример таблицы последовательностей.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Подробный пример таблицы последовательности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664575"
---
# <a name="sequence-table-detailed-example"></a><span data-ttu-id="f9621-103">Подробный пример таблицы последовательности</span><span class="sxs-lookup"><span data-stu-id="f9621-103">Sequence Table Detailed Example</span></span>

<span data-ttu-id="f9621-104">Ниже приведен пример таблицы последовательностей.</span><span class="sxs-lookup"><span data-stu-id="f9621-104">Here is an example of a sequence table.</span></span>



| <span data-ttu-id="f9621-105">Действие</span><span class="sxs-lookup"><span data-stu-id="f9621-105">Action</span></span>                                          | <span data-ttu-id="f9621-106">Условие</span><span class="sxs-lookup"><span data-stu-id="f9621-106">Condition</span></span>                                                       | <span data-ttu-id="f9621-107">Последовательность</span><span class="sxs-lookup"><span data-stu-id="f9621-107">Sequence</span></span> |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [<span data-ttu-id="f9621-108">лаунчкондитионс</span><span class="sxs-lookup"><span data-stu-id="f9621-108">LaunchConditions</span></span>](launchconditions-action.md) |                                                                 |          |
| [<span data-ttu-id="f9621-109">аппсеарч</span><span class="sxs-lookup"><span data-stu-id="f9621-109">AppSearch</span></span>](appsearch-action.md)               |                                                                 | <span data-ttu-id="f9621-110">200</span><span class="sxs-lookup"><span data-stu-id="f9621-110">200</span></span>      |
| [<span data-ttu-id="f9621-111">ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="f9621-111">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="f9621-112">\_Проверка CCP</span><span class="sxs-lookup"><span data-stu-id="f9621-112">CCP\_TEST</span></span>                                                       | <span data-ttu-id="f9621-113">300</span><span class="sxs-lookup"><span data-stu-id="f9621-113">300</span></span>      |
| <span data-ttu-id="f9621-114">ккпдиалог</span><span class="sxs-lookup"><span data-stu-id="f9621-114">CCPDialog</span></span>                                       | <span data-ttu-id="f9621-115">НЕ \_ удалось выполнить CCP \_</span><span class="sxs-lookup"><span data-stu-id="f9621-115">NOT\_CCP\_SUCCESS</span></span>                                               | <span data-ttu-id="f9621-116">400</span><span class="sxs-lookup"><span data-stu-id="f9621-116">400</span></span>      |
| <span data-ttu-id="f9621-117">микустомконфиг</span><span class="sxs-lookup"><span data-stu-id="f9621-117">MyCustomConfig</span></span>                                  | <span data-ttu-id="f9621-118">НЕ [ **установлено**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f9621-118">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="f9621-119">500</span><span class="sxs-lookup"><span data-stu-id="f9621-119">500</span></span>      |
| [<span data-ttu-id="f9621-120">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="f9621-120">CostInitialize</span></span>](costinitialize-action.md)     |                                                                 | <span data-ttu-id="f9621-121">600</span><span class="sxs-lookup"><span data-stu-id="f9621-121">600</span></span>      |
| [<span data-ttu-id="f9621-122">филекост</span><span class="sxs-lookup"><span data-stu-id="f9621-122">FileCost</span></span>](filecost-action.md)                 |                                                                 | <span data-ttu-id="f9621-123">700</span><span class="sxs-lookup"><span data-stu-id="f9621-123">700</span></span>      |
| [<span data-ttu-id="f9621-124">костфинализе</span><span class="sxs-lookup"><span data-stu-id="f9621-124">CostFinalize</span></span>](costfinalize-action.md)         |                                                                 | <span data-ttu-id="f9621-125">800</span><span class="sxs-lookup"><span data-stu-id="f9621-125">800</span></span>      |
| <span data-ttu-id="f9621-126">инсталлдиалог</span><span class="sxs-lookup"><span data-stu-id="f9621-126">InstallDialog</span></span>                                   | <span data-ttu-id="f9621-127">НЕ [ **установлено**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f9621-127">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="f9621-128">900</span><span class="sxs-lookup"><span data-stu-id="f9621-128">900</span></span>      |
| <span data-ttu-id="f9621-129">маинтенанцедиалог</span><span class="sxs-lookup"><span data-stu-id="f9621-129">MaintenanceDialog</span></span>                               | <span data-ttu-id="f9621-130">[**Установлено**](installed.md) И не [ **возобновлять**](resume.md)</span><span class="sxs-lookup"><span data-stu-id="f9621-130">[**Installed**](installed.md) AND NOT [**Resume**](resume.md)</span></span> | <span data-ttu-id="f9621-131">1000</span><span class="sxs-lookup"><span data-stu-id="f9621-131">1000</span></span>     |
| <span data-ttu-id="f9621-132">актиондиалог</span><span class="sxs-lookup"><span data-stu-id="f9621-132">ActionDialog</span></span>                                    |                                                                 | <span data-ttu-id="f9621-133">1100</span><span class="sxs-lookup"><span data-stu-id="f9621-133">1100</span></span>     |
| [<span data-ttu-id="f9621-134">регистерпродукт</span><span class="sxs-lookup"><span data-stu-id="f9621-134">RegisterProduct</span></span>](registerproduct-action.md)   |                                                                 | <span data-ttu-id="f9621-135">1200</span><span class="sxs-lookup"><span data-stu-id="f9621-135">1200</span></span>     |
| [<span data-ttu-id="f9621-136">инсталлвалидате</span><span class="sxs-lookup"><span data-stu-id="f9621-136">InstallValidate</span></span>](installvalidate-action.md)   |                                                                 | <span data-ttu-id="f9621-137">1300</span><span class="sxs-lookup"><span data-stu-id="f9621-137">1300</span></span>     |
| [<span data-ttu-id="f9621-138">инсталлфилес</span><span class="sxs-lookup"><span data-stu-id="f9621-138">InstallFiles</span></span>](installfiles-action.md)         |                                                                 | <span data-ttu-id="f9621-139">1400</span><span class="sxs-lookup"><span data-stu-id="f9621-139">1400</span></span>     |
| <span data-ttu-id="f9621-140">микустомактион</span><span class="sxs-lookup"><span data-stu-id="f9621-140">MyCustomAction</span></span>                                  | <span data-ttu-id="f9621-141">$MyComponent > 2</span><span class="sxs-lookup"><span data-stu-id="f9621-141">$MyComponent > 2</span></span>                                             | <span data-ttu-id="f9621-142">1500</span><span class="sxs-lookup"><span data-stu-id="f9621-142">1500</span></span>     |
| [<span data-ttu-id="f9621-143">Функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="f9621-143">InstallFinalize</span></span>](installfinalize-action.md)   |                                                                 | <span data-ttu-id="f9621-144">1600</span><span class="sxs-lookup"><span data-stu-id="f9621-144">1600</span></span>     |



 

<span data-ttu-id="f9621-145">Следующие действия в этой таблице последовательностей определяются установщиком и являются примерами стандартных действий.</span><span class="sxs-lookup"><span data-stu-id="f9621-145">The following actions in this sequence table are defined by the installer and are examples of standard actions:</span></span>

[<span data-ttu-id="f9621-146">лаунчкондитионс</span><span class="sxs-lookup"><span data-stu-id="f9621-146">LaunchConditions</span></span>](launchconditions-action.md)

 

[<span data-ttu-id="f9621-147">аппсеарч</span><span class="sxs-lookup"><span data-stu-id="f9621-147">AppSearch</span></span>](appsearch-action.md)

 

[<span data-ttu-id="f9621-148">ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="f9621-148">CCPSearch</span></span>](ccpsearch-action.md)

 

[<span data-ttu-id="f9621-149">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="f9621-149">CostInitialize</span></span>](costinitialize-action.md)

 

[<span data-ttu-id="f9621-150">филекост</span><span class="sxs-lookup"><span data-stu-id="f9621-150">FileCost</span></span>](filecost-action.md)

 

[<span data-ttu-id="f9621-151">костфинализе</span><span class="sxs-lookup"><span data-stu-id="f9621-151">CostFinalize</span></span>](costfinalize-action.md)

 

[<span data-ttu-id="f9621-152">регистерпродукт</span><span class="sxs-lookup"><span data-stu-id="f9621-152">RegisterProduct</span></span>](registerproduct-action.md)

 

[<span data-ttu-id="f9621-153">инсталлфилес</span><span class="sxs-lookup"><span data-stu-id="f9621-153">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="f9621-154">инсталлфилес</span><span class="sxs-lookup"><span data-stu-id="f9621-154">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="f9621-155">инсталлвалидате</span><span class="sxs-lookup"><span data-stu-id="f9621-155">InstallValidate</span></span>](installvalidate-action.md)

<span data-ttu-id="f9621-156">Следующие действия были определены автором таблицы и являются примерами [пользовательских действий](custom-actions.md) и должны быть перечислены в [таблице CustomAction](customaction-table.md):</span><span class="sxs-lookup"><span data-stu-id="f9621-156">The following actions were defined by the table's author and are examples of [custom actions](custom-actions.md) and must be listed in the [CustomAction table](customaction-table.md):</span></span>

<span data-ttu-id="f9621-157">микустомконфиг</span><span class="sxs-lookup"><span data-stu-id="f9621-157">MyCustomConfig</span></span>

 

<span data-ttu-id="f9621-158">микустомактион</span><span class="sxs-lookup"><span data-stu-id="f9621-158">MyCustomAction</span></span>

<span data-ttu-id="f9621-159">Остальные записи в поле действие являются внешними ключами в [таблице диалоговых окон](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="f9621-159">The remaining entries in the Action field are foreign keys into the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="f9621-160">Они указывают имена диалоговых окон, которые будут отображаться, если поле условия имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="f9621-160">They specify the names of dialog boxes that will displayed if the condition field evaluates to True.</span></span>

<span data-ttu-id="f9621-161">ккпдиалог</span><span class="sxs-lookup"><span data-stu-id="f9621-161">CCPDialog</span></span>

 

<span data-ttu-id="f9621-162">инсталлдиалог</span><span class="sxs-lookup"><span data-stu-id="f9621-162">InstallDialog</span></span>

 

<span data-ttu-id="f9621-163">маинтенанцедиалог</span><span class="sxs-lookup"><span data-stu-id="f9621-163">MaintenanceDialog</span></span>

 

<span data-ttu-id="f9621-164">актиондиалог</span><span class="sxs-lookup"><span data-stu-id="f9621-164">ActionDialog</span></span>

<span data-ttu-id="f9621-165">Столбец Условие заставляет установщик пропустить действие, если свойство или выражение в этом поле имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="f9621-165">The Condition column causes the installer to skip the action if the property or expression in this field is False.</span></span> <span data-ttu-id="f9621-166">Свойства [**Installed**](installed.md) и [**Resume**](resume.md) являются примерами свойств, которые устанавливаются установщиком.</span><span class="sxs-lookup"><span data-stu-id="f9621-166">The [**Installed**](installed.md) property and the [**RESUME**](resume.md) property are example of properties that are set by the installer.</span></span> <span data-ttu-id="f9621-167">[**Установленное**](installed.md) свойство устанавливается равным true, если продукт уже установлен, а свойство [**Resume**](resume.md) задано при возобновлении приостановленной установки.</span><span class="sxs-lookup"><span data-stu-id="f9621-167">The [**Installed**](installed.md) property is set to true if the product is already installed and the [**RESUME**](resume.md) property is set if resuming a suspended installation.</span></span> <span data-ttu-id="f9621-168">В \_ \_ \_ качестве примера свойств, которые могут быть заданы пользователем при установке приложения, можно задать в командной строке параметры проверки CCP и не CCP.</span><span class="sxs-lookup"><span data-stu-id="f9621-168">The CCP\_TEST and the NOT\_CCP\_SUCCESS properties are examples of properties that can be set at the command line by the user installing the application.</span></span>

<span data-ttu-id="f9621-169">Все действия выполняются последовательно со следующими условными шагами:</span><span class="sxs-lookup"><span data-stu-id="f9621-169">All actions run in sequence with the following conditional steps:</span></span>

-   <span data-ttu-id="f9621-170">Кппсеарч выполняется, только если \_ задано тестирование CCP.</span><span class="sxs-lookup"><span data-stu-id="f9621-170">The CPPSearch is run only if CCP\_TEST is set.</span></span>
-   <span data-ttu-id="f9621-171">Ккпдиалог выполняется, только если \_ \_ установлен параметр "не удалось установить CCP".</span><span class="sxs-lookup"><span data-stu-id="f9621-171">CCPDialog is run only if NOT\_CCP\_SUCCESS is set.</span></span>
-   <span data-ttu-id="f9621-172">Маинтенанцедиалог выполняется, только если этот продукт уже установлен и не является установкой, которая возобновляется после приостановки.</span><span class="sxs-lookup"><span data-stu-id="f9621-172">MaintenanceDialog is run only if this product is already installed and if this is not an installation that is being resume after being suspended.</span></span>
-   <span data-ttu-id="f9621-173">Микустомактион выполняется, только если выражение в столбце Condition имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="f9621-173">MyCustomAction is run only if the expression in the Condition column is True.</span></span> <span data-ttu-id="f9621-174">Выражение $MyComponent > 2 относится к состоянию действия компонента MyComponent.</span><span class="sxs-lookup"><span data-stu-id="f9621-174">The expression $MyComponent > 2 refers to the action state of the component called MyComponent.</span></span> <span data-ttu-id="f9621-175">Это состояние указывает, что Микустомактион следует запускать только в том случае, если установлен параметр MyComponent.</span><span class="sxs-lookup"><span data-stu-id="f9621-175">This condition indicates that MyCustomAction should only be run if MyComponent is set to be installed.</span></span> <span data-ttu-id="f9621-176">Дополнительные сведения о состояниях действий и состояниях выбора см. в описании свойства [**феатуререкуестстате**](session-featurerequeststate.md) , [таблицы функций](feature-table.md)и [действия инсталлфилес](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="f9621-176">For more information on Action states and Selection states, see the [**FeatureRequestState**](session-featurerequeststate.md) property, the [Feature table](feature-table.md), and the [InstallFiles action](installfiles-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9621-177">См. также</span><span class="sxs-lookup"><span data-stu-id="f9621-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9621-178">Использование свойств</span><span class="sxs-lookup"><span data-stu-id="f9621-178">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="f9621-179">Синтаксис условных операторов</span><span class="sxs-lookup"><span data-stu-id="f9621-179">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 



