---
description: Обратите внимание, что нельзя указать порядок, в котором установщик регистрирует или отменяет регистрацию библиотек DLL с помощью действий Селфрегмодулес и Селфунрегмодулес.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Указание порядка самостоятельной регистрации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497787"
---
# <a name="specifying-the-order-of-self-registration"></a><span data-ttu-id="e5478-103">Указание порядка самостоятельной регистрации</span><span class="sxs-lookup"><span data-stu-id="e5478-103">Specifying the Order of Self Registration</span></span>

<span data-ttu-id="e5478-104">Обратите внимание, что нельзя указать порядок, в котором установщик регистрирует или отменяет регистрацию библиотек DLL с помощью действий [селфрегмодулес](selfregmodules-action.md) и [селфунрегмодулес](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e5478-104">Note that you cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="e5478-105">Эти действия регистрируют все модули, перечисленные в [таблице селфрег](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5478-105">These actions register all the modules listed in the [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="e5478-106">Установщик не выполняет самостоятельную регистрацию exe-файлов.</span><span class="sxs-lookup"><span data-stu-id="e5478-106">The installer does not self-register .exe files.</span></span>

<span data-ttu-id="e5478-107">Чтобы указать порядок, в котором установщик регистрирует или отменяет регистрацию модулей, необходимо использовать два [настраиваемых действия](custom-actions.md) для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="e5478-107">To specify the order in which the installer registers or unregisters modules, you must use two [custom actions](custom-actions.md) for each module.</span></span> <span data-ttu-id="e5478-108">Одно настраиваемое действие для DllRegisterServer и второе для DllUnregisterServer.</span><span class="sxs-lookup"><span data-stu-id="e5478-108">One custom action for DllRegisterServer and a second for DllUnregisterServer.</span></span> <span data-ttu-id="e5478-109">Эти настраиваемые действия должны быть созданы в [таблице инсталлексекутесекуенце](installexecutesequence-table.md) в точке последовательности везде, где будет зарегистрирована или отменена регистрация библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="e5478-109">These custom actions must then be authored in the [InstallExecuteSequence table](installexecutesequence-table.md) at the point in the sequence wherever the DLL is to be registered or unregistered.</span></span>

<span data-ttu-id="e5478-110">В следующем примере показано, как создать базу данных, чтобы запланировать самостоятельную регистрацию библиотеки DLL в определенной точке последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="e5478-110">The following example illustrates how to author the database to schedule the self-registration of a DLL at a particular point in the action sequence.</span></span>

<span data-ttu-id="e5478-111">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e5478-111">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="e5478-112">Файл</span><span class="sxs-lookup"><span data-stu-id="e5478-112">File</span></span>  | <span data-ttu-id="e5478-113">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="e5478-113">Component\_</span></span> | <span data-ttu-id="e5478-114">FileName</span><span class="sxs-lookup"><span data-stu-id="e5478-114">FileName</span></span>  | <span data-ttu-id="e5478-115">Последовательность</span><span class="sxs-lookup"><span data-stu-id="e5478-115">Sequence</span></span> |
|-------|-------------|-----------|----------|
| <span data-ttu-id="e5478-116">myDll</span><span class="sxs-lookup"><span data-stu-id="e5478-116">mydll</span></span> | <span data-ttu-id="e5478-117">myComponent</span><span class="sxs-lookup"><span data-stu-id="e5478-117">myComponent</span></span> | <span data-ttu-id="e5478-118">Mydll.dll</span><span class="sxs-lookup"><span data-stu-id="e5478-118">Mydll.dll</span></span> | <span data-ttu-id="e5478-119">13</span><span class="sxs-lookup"><span data-stu-id="e5478-119">13</span></span>       |



 

<span data-ttu-id="e5478-120">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e5478-120">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="e5478-121">Компонент</span><span class="sxs-lookup"><span data-stu-id="e5478-121">Component</span></span>   | <span data-ttu-id="e5478-122">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e5478-122">ComponentId</span></span> | <span data-ttu-id="e5478-123">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="e5478-123">Directory\_</span></span> | <span data-ttu-id="e5478-124">Путь</span><span class="sxs-lookup"><span data-stu-id="e5478-124">KeyPath</span></span> |
|-------------|-------------|-------------|---------|
| <span data-ttu-id="e5478-125">myComponent</span><span class="sxs-lookup"><span data-stu-id="e5478-125">myComponent</span></span> | <span data-ttu-id="e5478-126">{*a GUID*}</span><span class="sxs-lookup"><span data-stu-id="e5478-126">{*a GUID*}</span></span>  | <span data-ttu-id="e5478-127">myFolder</span><span class="sxs-lookup"><span data-stu-id="e5478-127">myFolder</span></span>    | <span data-ttu-id="e5478-128">myDll</span><span class="sxs-lookup"><span data-stu-id="e5478-128">mydll</span></span>   |



 

[<span data-ttu-id="e5478-129">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="e5478-129">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="e5478-130">Каталог</span><span class="sxs-lookup"><span data-stu-id="e5478-130">Directory</span></span> | <span data-ttu-id="e5478-131">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="e5478-131">Directory\_Parent</span></span> | <span data-ttu-id="e5478-132">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="e5478-132">DefaultDir</span></span>          |
|-----------|-------------------|---------------------|
| <span data-ttu-id="e5478-133">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="e5478-133">TARGETDIR</span></span> |                   | <span data-ttu-id="e5478-134">SourceDir</span><span class="sxs-lookup"><span data-stu-id="e5478-134">SourceDir</span></span>           |
| <span data-ttu-id="e5478-135">myFolder</span><span class="sxs-lookup"><span data-stu-id="e5478-135">myFolder</span></span>  | <span data-ttu-id="e5478-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="e5478-136">TARGETDIR</span></span>         | <span data-ttu-id="e5478-137">myFolder \| мою папку</span><span class="sxs-lookup"><span data-stu-id="e5478-137">myFolder\|My Folder</span></span> |



 

[<span data-ttu-id="e5478-138">Таблица CustomAction</span><span class="sxs-lookup"><span data-stu-id="e5478-138">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="e5478-139">Действие</span><span class="sxs-lookup"><span data-stu-id="e5478-139">Action</span></span>     | <span data-ttu-id="e5478-140">Тип</span><span class="sxs-lookup"><span data-stu-id="e5478-140">Type</span></span> | <span data-ttu-id="e5478-141">Источник</span><span class="sxs-lookup"><span data-stu-id="e5478-141">Source</span></span>   | <span data-ttu-id="e5478-142">Назначение</span><span class="sxs-lookup"><span data-stu-id="e5478-142">Target</span></span>                                     |
|------------|------|----------|--------------------------------------------|
| <span data-ttu-id="e5478-143">мидллрег</span><span class="sxs-lookup"><span data-stu-id="e5478-143">mydllREG</span></span>   | <span data-ttu-id="e5478-144">3170</span><span class="sxs-lookup"><span data-stu-id="e5478-144">3170</span></span> | <span data-ttu-id="e5478-145">myFolder</span><span class="sxs-lookup"><span data-stu-id="e5478-145">myFolder</span></span> | <span data-ttu-id="e5478-146">" \[ Системфолдер \] msiexec"/y " \[ \# myDll \] "</span><span class="sxs-lookup"><span data-stu-id="e5478-146">"\[SystemFolder\]msiexec" /y "\[\#mydll\]"</span></span> |
| <span data-ttu-id="e5478-147">мидллунрег</span><span class="sxs-lookup"><span data-stu-id="e5478-147">mydllUNREG</span></span> | <span data-ttu-id="e5478-148">3170</span><span class="sxs-lookup"><span data-stu-id="e5478-148">3170</span></span> | <span data-ttu-id="e5478-149">myFolder</span><span class="sxs-lookup"><span data-stu-id="e5478-149">myFolder</span></span> | <span data-ttu-id="e5478-150">" \[ Системфолдер \] msiexec"/z " \[ \# myDll \] "</span><span class="sxs-lookup"><span data-stu-id="e5478-150">"\[SystemFolder\]msiexec" /z "\[\#mydll\]"</span></span> |



 

<span data-ttu-id="e5478-151">[Таблица инсталлексекутесекуенце](installexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e5478-151">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="e5478-152">Действие</span><span class="sxs-lookup"><span data-stu-id="e5478-152">Action</span></span>           | <span data-ttu-id="e5478-153">Условие</span><span class="sxs-lookup"><span data-stu-id="e5478-153">Condition</span></span>         | <span data-ttu-id="e5478-154">Последовательность</span><span class="sxs-lookup"><span data-stu-id="e5478-154">Sequence</span></span> |
|------------------|-------------------|----------|
| <span data-ttu-id="e5478-155">селфунрегмодулес</span><span class="sxs-lookup"><span data-stu-id="e5478-155">SelfUnregModules</span></span> |                   | <span data-ttu-id="e5478-156">2200</span><span class="sxs-lookup"><span data-stu-id="e5478-156">2200</span></span>     |
| <span data-ttu-id="e5478-157">мидллунрег</span><span class="sxs-lookup"><span data-stu-id="e5478-157">mydllUNREG</span></span>       | <span data-ttu-id="e5478-158">$myComponent = 2</span><span class="sxs-lookup"><span data-stu-id="e5478-158">$myComponent=2</span></span>    | <span data-ttu-id="e5478-159">2201</span><span class="sxs-lookup"><span data-stu-id="e5478-159">2201</span></span>     |
| <span data-ttu-id="e5478-160">ремовефилес</span><span class="sxs-lookup"><span data-stu-id="e5478-160">RemoveFiles</span></span>      |                   | <span data-ttu-id="e5478-161">3500</span><span class="sxs-lookup"><span data-stu-id="e5478-161">3500</span></span>     |
| <span data-ttu-id="e5478-162">инсталлфилес</span><span class="sxs-lookup"><span data-stu-id="e5478-162">InstallFiles</span></span>     |                   | <span data-ttu-id="e5478-163">4000</span><span class="sxs-lookup"><span data-stu-id="e5478-163">4000</span></span>     |
| <span data-ttu-id="e5478-164">селфрегмодулес</span><span class="sxs-lookup"><span data-stu-id="e5478-164">SelfRegModules</span></span>   |                   | <span data-ttu-id="e5478-165">6500</span><span class="sxs-lookup"><span data-stu-id="e5478-165">6500</span></span>     |
| <span data-ttu-id="e5478-166">мидллрег</span><span class="sxs-lookup"><span data-stu-id="e5478-166">mydllREG</span></span>         | <span data-ttu-id="e5478-167">$myComponent>2</span><span class="sxs-lookup"><span data-stu-id="e5478-167">$myComponent>2</span></span> | <span data-ttu-id="e5478-168">6501</span><span class="sxs-lookup"><span data-stu-id="e5478-168">6501</span></span>     |



 

 

 



