---
description: В таблице Адвтексекутесекуенце перечислены действия, которые установщик вызывает при выполнении действия объявления верхнего уровня. См. раздел таблицы процедур установки, использование таблицы последовательности и подробный пример таблицы последовательности.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Импорт Адвтексекутесекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815448"
---
# <a name="importing-the-advtexecutesequence"></a><span data-ttu-id="61370-104">Импорт Адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="61370-104">Importing the AdvtExecuteSequence</span></span>

<span data-ttu-id="61370-105">В [таблице адвтексекутесекуенце](advtexecutesequence-table.md) перечислены действия, которые установщик вызывает при выполнении [действия объявления](advertise-action.md)верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="61370-105">The [AdvtExecuteSequence table](advtexecutesequence-table.md) lists actions the installer calls when it executes the top-level [ADVERTISE action](advertise-action.md).</span></span> <span data-ttu-id="61370-106">См. раздел [таблицы процедур установки](installation-procedure-tables-group.md), [Использование таблицы последовательности](using-a-sequence-table.md)и [подробный пример таблицы последовательности](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="61370-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="61370-107">Если в разделе [импортируется пустая база данных](importing-a-blank-database.md) , которая использовалась uisample.msi из пакета SDK для установщик Windows, таблицы последовательности в копии MNP2000.msi уже содержат предлагаемые последовательности действий, описанные в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="61370-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence table](using-a-sequence-table.md).</span></span> <span data-ttu-id="61370-108">Изменения этих последовательностей не требуются для создания образца установочного пакета Notepad.</span><span class="sxs-lookup"><span data-stu-id="61370-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="61370-109">Используйте редактор базы данных, чтобы открыть MNP2000.msi и ввести в [таблицу адвтексекутесекуенце](advtexecutesequence-table.md)следующие данные.</span><span class="sxs-lookup"><span data-stu-id="61370-109">Use your database editor to open MNP2000.msi and enter the following data into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

[<span data-ttu-id="61370-110">Таблица Адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="61370-110">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)



| <span data-ttu-id="61370-111">Действие</span><span class="sxs-lookup"><span data-stu-id="61370-111">Action</span></span>                | <span data-ttu-id="61370-112">Условие</span><span class="sxs-lookup"><span data-stu-id="61370-112">Condition</span></span> | <span data-ttu-id="61370-113">Последовательность</span><span class="sxs-lookup"><span data-stu-id="61370-113">Sequence</span></span> |
|-----------------------|-----------|----------|
| <span data-ttu-id="61370-114">костфинализе</span><span class="sxs-lookup"><span data-stu-id="61370-114">CostFinalize</span></span>          |           | <span data-ttu-id="61370-115">1000</span><span class="sxs-lookup"><span data-stu-id="61370-115">1000</span></span>     |
| <span data-ttu-id="61370-116">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="61370-116">CostInitialize</span></span>        |           | <span data-ttu-id="61370-117">800</span><span class="sxs-lookup"><span data-stu-id="61370-117">800</span></span>      |
| <span data-ttu-id="61370-118">креатешорткутс</span><span class="sxs-lookup"><span data-stu-id="61370-118">CreateShortcuts</span></span>       |           | <span data-ttu-id="61370-119">4500</span><span class="sxs-lookup"><span data-stu-id="61370-119">4500</span></span>     |
| <span data-ttu-id="61370-120">Функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="61370-120">InstallFinalize</span></span>       |           | <span data-ttu-id="61370-121">6600</span><span class="sxs-lookup"><span data-stu-id="61370-121">6600</span></span>     |
| <span data-ttu-id="61370-122">инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="61370-122">InstallInitialize</span></span>     |           | <span data-ttu-id="61370-123">1500</span><span class="sxs-lookup"><span data-stu-id="61370-123">1500</span></span>     |
| <span data-ttu-id="61370-124">инсталлвалидате</span><span class="sxs-lookup"><span data-stu-id="61370-124">InstallValidate</span></span>       |           | <span data-ttu-id="61370-125">1400</span><span class="sxs-lookup"><span data-stu-id="61370-125">1400</span></span>     |
| <span data-ttu-id="61370-126">публишкомпонентс</span><span class="sxs-lookup"><span data-stu-id="61370-126">PublishComponents</span></span>     |           | <span data-ttu-id="61370-127">6200</span><span class="sxs-lookup"><span data-stu-id="61370-127">6200</span></span>     |
| <span data-ttu-id="61370-128">публишфеатурес</span><span class="sxs-lookup"><span data-stu-id="61370-128">PublishFeatures</span></span>       |           | <span data-ttu-id="61370-129">6300</span><span class="sxs-lookup"><span data-stu-id="61370-129">6300</span></span>     |
| <span data-ttu-id="61370-130">публишпродукт</span><span class="sxs-lookup"><span data-stu-id="61370-130">PublishProduct</span></span>        |           | <span data-ttu-id="61370-131">6400</span><span class="sxs-lookup"><span data-stu-id="61370-131">6400</span></span>     |
| <span data-ttu-id="61370-132">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="61370-132">RegisterClassInfo</span></span>     |           | <span data-ttu-id="61370-133">4600</span><span class="sxs-lookup"><span data-stu-id="61370-133">4600</span></span>     |
| <span data-ttu-id="61370-134">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="61370-134">RegisterExtensionInfo</span></span> |           | <span data-ttu-id="61370-135">4700</span><span class="sxs-lookup"><span data-stu-id="61370-135">4700</span></span>     |
| <span data-ttu-id="61370-136">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="61370-136">RegisterMIMEInfo</span></span>      |           | <span data-ttu-id="61370-137">4900</span><span class="sxs-lookup"><span data-stu-id="61370-137">4900</span></span>     |
| <span data-ttu-id="61370-138">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="61370-138">RegisterProgIdInfo</span></span>    |           | <span data-ttu-id="61370-139">4800</span><span class="sxs-lookup"><span data-stu-id="61370-139">4800</span></span>     |



 

<span data-ttu-id="61370-140">[Таблица адвтуисекуенце](advtuisequence-table.md) не используется установщиком.</span><span class="sxs-lookup"><span data-stu-id="61370-140">The [AdvtUISequence table](advtuisequence-table.md) is not used by the installer.</span></span> <span data-ttu-id="61370-141">Эта таблица не должна существовать или оставаться пустой в базе данных установки.</span><span class="sxs-lookup"><span data-stu-id="61370-141">This table should not exist or be left empty in the installation database.</span></span>

[<span data-ttu-id="61370-142">Продолжить</span><span class="sxs-lookup"><span data-stu-id="61370-142">Continue</span></span>](adding-summary-information.md)

 

 



