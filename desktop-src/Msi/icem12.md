---
description: ICEM12 проверяет, что в таблице Модулесекуенце стандартные действия имеют порядковые номера, а пользовательские действия имеют значения Басеактион и After.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080398"
---
# <a name="icem12"></a><span data-ttu-id="2948a-103">ICEM12</span><span class="sxs-lookup"><span data-stu-id="2948a-103">ICEM12</span></span>

<span data-ttu-id="2948a-104">ICEM12 проверяет, что в таблице Модулесекуенце стандартные действия имеют порядковые номера, а пользовательские действия имеют значения Басеактион и After.</span><span class="sxs-lookup"><span data-stu-id="2948a-104">ICEM12 verifies that in a ModuleSequence table, standard actions have sequence numbers and custom actions have BaseAction and After values.</span></span>

<span data-ttu-id="2948a-105">Этот ИЦЕМ доступен в файле Мержемод. CUB, который входит в состав пакета SDK для установщик Windows 2,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="2948a-105">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="2948a-106">Дополнительные сведения см. в разделе [Windows SDK компонентов для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2948a-106">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="2948a-107">Результат</span><span class="sxs-lookup"><span data-stu-id="2948a-107">Result</span></span>

<span data-ttu-id="2948a-108">ICEM12 отправляет сообщение об ошибке в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="2948a-108">ICEM12 posts an error in the following cases:</span></span>

-   <span data-ttu-id="2948a-109">Он находит, что модуль содержит [стандартное действие](standard-actions.md) без порядкового номера.</span><span class="sxs-lookup"><span data-stu-id="2948a-109">It finds the module contains a [standard action](standard-actions.md) without a sequence number.</span></span>
-   <span data-ttu-id="2948a-110">Он обнаруживает, что стандартное действие имеет значения, указанные в полях Басеактион или After [таблицы модулеадминуисекуенце](moduleadminuisequence-table.md), [модулеадминексекутесекуенце таблицы](moduleadminexecutesequence-table.md), таблицы [модулеадвтексекутесекуенце](moduleadvtexecutesequence-table.md), [таблицы ModuleInstallUISequence](moduleinstalluisequence-table.md)или [таблицы ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2948a-110">It finds that a standard action has values entered in the BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>
-   <span data-ttu-id="2948a-111">Он находит, что модуль содержит [настраиваемое действие](custom-actions.md) , не указывая значения в полях Sequence, Басеактион или After [таблицы модулеадминуисекуенце таблица](moduleadminuisequence-table.md), [Таблица модулеадминексекутесекуенце таблицы](moduleadminexecutesequence-table.md), [Таблица модулеадвтексекутесекуенце](moduleadvtexecutesequence-table.md), таблица [ModuleInstallUISequence](moduleinstalluisequence-table.md)или [Таблица ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2948a-111">It finds the module contains a [custom action](custom-actions.md) without any values entered into the Sequence, BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>

<span data-ttu-id="2948a-112">ICEM12 отправляет предупреждение, если обнаруживает пользовательское действие с указанным порядковым номером, но не имеет значения в полях Басеактион и After.</span><span class="sxs-lookup"><span data-stu-id="2948a-112">ICEM12 posts a warning if it finds a custom action that has a Sequence number specified, but no value in the BaseAction or After fields.</span></span>

<span data-ttu-id="2948a-113">Обратите внимание, что все действия, найденные в [таблице CustomAction](customaction-table.md) , считаются пользовательскими действиями.</span><span class="sxs-lookup"><span data-stu-id="2948a-113">Note that all actions found in the [CustomAction table](customaction-table.md) are considered custom actions.</span></span> <span data-ttu-id="2948a-114">Все остальные действия считаются стандартными действиями.</span><span class="sxs-lookup"><span data-stu-id="2948a-114">All other action are considered standard actions.</span></span>

## <a name="example"></a><span data-ttu-id="2948a-115">Пример</span><span class="sxs-lookup"><span data-stu-id="2948a-115">Example</span></span>

<span data-ttu-id="2948a-116">ICEM12 отправляет следующие сообщения об ошибках и предупреждения для модуля, содержащего записи базы данных, показанные ниже:</span><span class="sxs-lookup"><span data-stu-id="2948a-116">ICEM12 posts the following error and warning messages for a module that contains the database entries shown below:</span></span>

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[<span data-ttu-id="2948a-117">CustomAction</span><span class="sxs-lookup"><span data-stu-id="2948a-117">CustomAction</span></span>](customaction-table.md)



| <span data-ttu-id="2948a-118">Действие</span><span class="sxs-lookup"><span data-stu-id="2948a-118">Action</span></span>  | <span data-ttu-id="2948a-119">Тип</span><span class="sxs-lookup"><span data-stu-id="2948a-119">Type</span></span> | <span data-ttu-id="2948a-120">Источник</span><span class="sxs-lookup"><span data-stu-id="2948a-120">Source</span></span>  | <span data-ttu-id="2948a-121">Назначение</span><span class="sxs-lookup"><span data-stu-id="2948a-121">Target</span></span>  |
|---------|------|---------|---------|
| <span data-ttu-id="2948a-122">Action1 превышают</span><span class="sxs-lookup"><span data-stu-id="2948a-122">Action1</span></span> | <span data-ttu-id="2948a-123">30</span><span class="sxs-lookup"><span data-stu-id="2948a-123">30</span></span>   | <span data-ttu-id="2948a-124">Источник1</span><span class="sxs-lookup"><span data-stu-id="2948a-124">source1</span></span> | <span data-ttu-id="2948a-125">Target1</span><span class="sxs-lookup"><span data-stu-id="2948a-125">target1</span></span> |
| <span data-ttu-id="2948a-126">Action3</span><span class="sxs-lookup"><span data-stu-id="2948a-126">Action3</span></span> | <span data-ttu-id="2948a-127">30</span><span class="sxs-lookup"><span data-stu-id="2948a-127">30</span></span>   | <span data-ttu-id="2948a-128">source3</span><span class="sxs-lookup"><span data-stu-id="2948a-128">source3</span></span> | <span data-ttu-id="2948a-129">target3</span><span class="sxs-lookup"><span data-stu-id="2948a-129">target3</span></span> |



 

[<span data-ttu-id="2948a-130">модулеадминексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="2948a-130">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)



| <span data-ttu-id="2948a-131">Действие</span><span class="sxs-lookup"><span data-stu-id="2948a-131">Action</span></span>  | <span data-ttu-id="2948a-132">Последовательность</span><span class="sxs-lookup"><span data-stu-id="2948a-132">Sequence</span></span> | <span data-ttu-id="2948a-133">басеактион</span><span class="sxs-lookup"><span data-stu-id="2948a-133">BaseAction</span></span> | <span data-ttu-id="2948a-134">После</span><span class="sxs-lookup"><span data-stu-id="2948a-134">After</span></span> | <span data-ttu-id="2948a-135">Условие</span><span class="sxs-lookup"><span data-stu-id="2948a-135">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="2948a-136">Action2</span><span class="sxs-lookup"><span data-stu-id="2948a-136">Action2</span></span> |          | <span data-ttu-id="2948a-137">Action1 превышают</span><span class="sxs-lookup"><span data-stu-id="2948a-137">Action1</span></span>    | <span data-ttu-id="2948a-138">1</span><span class="sxs-lookup"><span data-stu-id="2948a-138">1</span></span>     | <span data-ttu-id="2948a-139">true</span><span class="sxs-lookup"><span data-stu-id="2948a-139">true</span></span>      |
| <span data-ttu-id="2948a-140">Action3</span><span class="sxs-lookup"><span data-stu-id="2948a-140">Action3</span></span> |          |            |       | <span data-ttu-id="2948a-141">true</span><span class="sxs-lookup"><span data-stu-id="2948a-141">true</span></span>      |



 

[<span data-ttu-id="2948a-142">модулеинсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="2948a-142">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="2948a-143">Действие</span><span class="sxs-lookup"><span data-stu-id="2948a-143">Action</span></span>  | <span data-ttu-id="2948a-144">Последовательность</span><span class="sxs-lookup"><span data-stu-id="2948a-144">Sequence</span></span> | <span data-ttu-id="2948a-145">басеактион</span><span class="sxs-lookup"><span data-stu-id="2948a-145">BaseAction</span></span> | <span data-ttu-id="2948a-146">После</span><span class="sxs-lookup"><span data-stu-id="2948a-146">After</span></span> | <span data-ttu-id="2948a-147">Условие</span><span class="sxs-lookup"><span data-stu-id="2948a-147">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="2948a-148">Action1 превышают</span><span class="sxs-lookup"><span data-stu-id="2948a-148">Action1</span></span> | <span data-ttu-id="2948a-149">1</span><span class="sxs-lookup"><span data-stu-id="2948a-149">1</span></span>        |            |       | <span data-ttu-id="2948a-150">true</span><span class="sxs-lookup"><span data-stu-id="2948a-150">true</span></span>      |



 

<span data-ttu-id="2948a-151">Чтобы устранить эти ошибки, попробуйте выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2948a-151">To fix these errors try the following:</span></span>

-   <span data-ttu-id="2948a-152">Удалите порядковый номер для настраиваемого действия Action1 превышают и используйте вместо него поля Басеактион и After.</span><span class="sxs-lookup"><span data-stu-id="2948a-152">Remove the sequence number for the custom action Action1 and use the BaseAction and After fields instead.</span></span>
-   <span data-ttu-id="2948a-153">Введите значения в поля Sequence, Басеактион или After для настраиваемого действия Action3.</span><span class="sxs-lookup"><span data-stu-id="2948a-153">Enter values into the Sequence, BaseAction, or After fields for the custom action Action3.</span></span> <span data-ttu-id="2948a-154">Оставьте поля Басеактион и After пустыми для стандартного действия Action2.</span><span class="sxs-lookup"><span data-stu-id="2948a-154">Leave the BaseAction and After fields empty for standard action Action2.</span></span>
-   <span data-ttu-id="2948a-155">Не оставляйте поле последовательности пустым для стандартного действия Action2.</span><span class="sxs-lookup"><span data-stu-id="2948a-155">Do not leave the Sequence field empty for standard action Action2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2948a-156">См. также</span><span class="sxs-lookup"><span data-stu-id="2948a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2948a-157">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="2948a-157">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



