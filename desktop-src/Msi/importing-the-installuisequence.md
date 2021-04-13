---
description: Последовательность пользовательского интерфейса импортируется в образец базы данных.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Импорт Инсталлуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265416"
---
# <a name="importing-the-installuisequence"></a><span data-ttu-id="6ab89-103">Импорт Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="6ab89-103">Importing the InstallUISequence</span></span>

<span data-ttu-id="6ab89-104">В [таблице инсталлуисекуенце](installuisequence-table.md) перечислены действия, выполняемые при выполнении [действия по установке](install-action.md) верхнего уровня, а для внутреннего уровня ПОЛЬЗОВАТЕЛЬСКОГО интерфейса — полный пользовательский интерфейс или сокращенный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6ab89-104">The [InstallUISequence table](installuisequence-table.md) lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="6ab89-105">Установщик пропускает действия в этой таблице, если для уровня пользовательского интерфейса задан базовый пользовательский интерфейс или нет пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6ab89-105">The installer skips the actions in this table if the user interface level is set to basic UI or to no UI.</span></span> <span data-ttu-id="6ab89-106">См. раздел [Пользовательский интерфейс](user-interface.md) и [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="6ab89-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="6ab89-107">См. раздел [таблицы процедур установки](installation-procedure-tables-group.md), [Использование таблицы последовательности](using-a-sequence-table.md)и [подробный пример таблицы последовательности](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="6ab89-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="6ab89-108">Если в разделе [импортируется пустая база данных](importing-a-blank-database.md) , которая использовалась uisample.msi из пакета SDK для установщик Windows, таблицы последовательности в копии MNP2000.msi уже содержат предлагаемые последовательности действий, описанные в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6ab89-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="6ab89-109">Для создания установочного пакета блокнота нет необходимости вносить изменения в эти последовательности.</span><span class="sxs-lookup"><span data-stu-id="6ab89-109">No changes to these sequences should be necessary to author the Notepad installation package.</span></span>

<span data-ttu-id="6ab89-110">Используйте редактор базы данных, чтобы открыть MNP2000.msi и ввести в таблицу Инсталлуисекуенце следующие данные.</span><span class="sxs-lookup"><span data-stu-id="6ab89-110">Use your database editor to open MNP2000.msi and enter the following data into the InstallUISequence table.</span></span>

[<span data-ttu-id="6ab89-111">Таблица Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="6ab89-111">InstallUISequence Table</span></span>](installuisequence-table.md)



| <span data-ttu-id="6ab89-112">Действие</span><span class="sxs-lookup"><span data-stu-id="6ab89-112">Action</span></span>                | <span data-ttu-id="6ab89-113">Условие</span><span class="sxs-lookup"><span data-stu-id="6ab89-113">Condition</span></span>                                    | <span data-ttu-id="6ab89-114">Последовательность</span><span class="sxs-lookup"><span data-stu-id="6ab89-114">Sequence</span></span> |
|-----------------------|----------------------------------------------|----------|
| <span data-ttu-id="6ab89-115">аппсеарч</span><span class="sxs-lookup"><span data-stu-id="6ab89-115">AppSearch</span></span>             |                                              | <span data-ttu-id="6ab89-116">400</span><span class="sxs-lookup"><span data-stu-id="6ab89-116">400</span></span>      |
| <span data-ttu-id="6ab89-117">ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="6ab89-117">CCPSearch</span></span>             | <span data-ttu-id="6ab89-118">НЕ установлено</span><span class="sxs-lookup"><span data-stu-id="6ab89-118">NOT Installed</span></span>                                | <span data-ttu-id="6ab89-119">500</span><span class="sxs-lookup"><span data-stu-id="6ab89-119">500</span></span>      |
| <span data-ttu-id="6ab89-120">костфинализе</span><span class="sxs-lookup"><span data-stu-id="6ab89-120">CostFinalize</span></span>          |                                              | <span data-ttu-id="6ab89-121">1000</span><span class="sxs-lookup"><span data-stu-id="6ab89-121">1000</span></span>     |
| <span data-ttu-id="6ab89-122">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="6ab89-122">CostInitialize</span></span>        |                                              | <span data-ttu-id="6ab89-123">800</span><span class="sxs-lookup"><span data-stu-id="6ab89-123">800</span></span>      |
| <span data-ttu-id="6ab89-124">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="6ab89-124">ExecuteAction</span></span>         |                                              | <span data-ttu-id="6ab89-125">1300</span><span class="sxs-lookup"><span data-stu-id="6ab89-125">1300</span></span>     |
| <span data-ttu-id="6ab89-126">екситдлг</span><span class="sxs-lookup"><span data-stu-id="6ab89-126">ExitDlg</span></span>               |                                              | <span data-ttu-id="6ab89-127">-1</span><span class="sxs-lookup"><span data-stu-id="6ab89-127">-1</span></span>       |
| <span data-ttu-id="6ab89-128">фаталеррордлг</span><span class="sxs-lookup"><span data-stu-id="6ab89-128">FatalErrorDlg</span></span>         |                                              | <span data-ttu-id="6ab89-129">–3</span><span class="sxs-lookup"><span data-stu-id="6ab89-129">-3</span></span>       |
| <span data-ttu-id="6ab89-130">филекост</span><span class="sxs-lookup"><span data-stu-id="6ab89-130">FileCost</span></span>              |                                              | <span data-ttu-id="6ab89-131">900</span><span class="sxs-lookup"><span data-stu-id="6ab89-131">900</span></span>      |
| <span data-ttu-id="6ab89-132">лаунчкондитионс</span><span class="sxs-lookup"><span data-stu-id="6ab89-132">LaunchConditions</span></span>      |                                              | <span data-ttu-id="6ab89-133">100</span><span class="sxs-lookup"><span data-stu-id="6ab89-133">100</span></span>      |
| <span data-ttu-id="6ab89-134">маинтенанцевелкомедлг</span><span class="sxs-lookup"><span data-stu-id="6ab89-134">MaintenanceWelcomeDlg</span></span> | <span data-ttu-id="6ab89-135">Установлено, не возобновлено и не выбрано</span><span class="sxs-lookup"><span data-stu-id="6ab89-135">Installed AND NOT RESUME AND NOT Preselected</span></span> | <span data-ttu-id="6ab89-136">1250</span><span class="sxs-lookup"><span data-stu-id="6ab89-136">1250</span></span>     |
| <span data-ttu-id="6ab89-137">препаредлг</span><span class="sxs-lookup"><span data-stu-id="6ab89-137">PrepareDlg</span></span>            |                                              | <span data-ttu-id="6ab89-138">140</span><span class="sxs-lookup"><span data-stu-id="6ab89-138">140</span></span>      |
| <span data-ttu-id="6ab89-139">прогрессдлг</span><span class="sxs-lookup"><span data-stu-id="6ab89-139">ProgressDlg</span></span>           |                                              | <span data-ttu-id="6ab89-140">1280</span><span class="sxs-lookup"><span data-stu-id="6ab89-140">1280</span></span>     |
| <span data-ttu-id="6ab89-141">ресумедлг</span><span class="sxs-lookup"><span data-stu-id="6ab89-141">ResumeDlg</span></span>             | <span data-ttu-id="6ab89-142">Установленные и (возобновление или предустановленный)</span><span class="sxs-lookup"><span data-stu-id="6ab89-142">Installed AND (RESUME OR Preselected)</span></span>        | <span data-ttu-id="6ab89-143">1240</span><span class="sxs-lookup"><span data-stu-id="6ab89-143">1240</span></span>     |
| <span data-ttu-id="6ab89-144">рмккпсеарч</span><span class="sxs-lookup"><span data-stu-id="6ab89-144">RMCCPSearch</span></span>           | <span data-ttu-id="6ab89-145">НЕ установлено</span><span class="sxs-lookup"><span data-stu-id="6ab89-145">NOT Installed</span></span>                                | <span data-ttu-id="6ab89-146">600</span><span class="sxs-lookup"><span data-stu-id="6ab89-146">600</span></span>      |
| <span data-ttu-id="6ab89-147">усерекситдлг</span><span class="sxs-lookup"><span data-stu-id="6ab89-147">UserExitDlg</span></span>           |                                              | <span data-ttu-id="6ab89-148">-2</span><span class="sxs-lookup"><span data-stu-id="6ab89-148">-2</span></span>       |
| <span data-ttu-id="6ab89-149">велкомедлг</span><span class="sxs-lookup"><span data-stu-id="6ab89-149">WelcomeDlg</span></span>            | <span data-ttu-id="6ab89-150">НЕ установлено</span><span class="sxs-lookup"><span data-stu-id="6ab89-150">NOT Installed</span></span>                                | <span data-ttu-id="6ab89-151">1230</span><span class="sxs-lookup"><span data-stu-id="6ab89-151">1230</span></span>     |
| <span data-ttu-id="6ab89-152">мигратефеатурестатес</span><span class="sxs-lookup"><span data-stu-id="6ab89-152">MigrateFeatureStates</span></span>  |                                              | <span data-ttu-id="6ab89-153">1200</span><span class="sxs-lookup"><span data-stu-id="6ab89-153">1200</span></span>     |
| <span data-ttu-id="6ab89-154">финдрелатедпродуктс</span><span class="sxs-lookup"><span data-stu-id="6ab89-154">FindRelatedProducts</span></span>   |                                              | <span data-ttu-id="6ab89-155">200</span><span class="sxs-lookup"><span data-stu-id="6ab89-155">200</span></span>      |



 

[<span data-ttu-id="6ab89-156">Продолжить</span><span class="sxs-lookup"><span data-stu-id="6ab89-156">Continue</span></span>](importing-the-adminexecutesequence.md)

 

 



