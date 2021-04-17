---
description: В таблице Админуисекуенце перечислены действия, которые установщик вызывает при выполнении действия администратора верхнего уровня, а на уровне внутреннего пользовательского интерфейса — полный пользовательский интерфейс или ограниченный пользовательский интерфейс.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Импорт Админуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650968"
---
# <a name="importing-the-adminuisequence"></a><span data-ttu-id="ce293-103">Импорт Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="ce293-103">Importing the AdminUISequence</span></span>

<span data-ttu-id="ce293-104">В [таблице админуисекуенце](adminuisequence-table.md) перечислены действия, которые установщик вызывает при выполнении [действия администратора](admin-action.md) верхнего уровня, а на уровне внутреннего ПОЛЬЗОВАТЕЛЬСКОГО интерфейса — полный пользовательский интерфейс или ограниченный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ce293-104">The [AdminUISequence table](adminuisequence-table.md) lists actions that the installer calls when it executes the top-level [ADMIN action](admin-action.md) and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="ce293-105">Установщик пропускает действия в этой таблице, если на уровне пользовательского интерфейса задан базовый пользовательский интерфейс или нет пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ce293-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="ce293-106">См. раздел [Пользовательский интерфейс](user-interface.md) и [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ce293-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="ce293-107">См. раздел [таблицы процедур установки](installation-procedure-tables-group.md), [Использование таблицы последовательности](using-a-sequence-table.md)и [подробный пример таблицы последовательности](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="ce293-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="ce293-108">Если в разделе [импортируется пустая база данных](importing-a-blank-database.md) , которая использовалась uisample.msi из пакета SDK для установщик Windows, таблицы последовательности в копии MNP2000.msi уже содержат предлагаемые последовательности действий, описанные в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ce293-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="ce293-109">Для установки образца Notepad не нужно вносить изменения в эти последовательности.</span><span class="sxs-lookup"><span data-stu-id="ce293-109">No changes to these sequences should be necessary to install the Notepad sample.</span></span>

<span data-ttu-id="ce293-110">Используйте редактор базы данных, чтобы открыть MNP2000.msi и ввести в таблицу Админексекутесекуенце следующие данные.</span><span class="sxs-lookup"><span data-stu-id="ce293-110">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="ce293-111">Таблица Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="ce293-111">AdminUISequence Table</span></span>](adminuisequence-table.md)



| <span data-ttu-id="ce293-112">Действие</span><span class="sxs-lookup"><span data-stu-id="ce293-112">Action</span></span>          | <span data-ttu-id="ce293-113">Условие</span><span class="sxs-lookup"><span data-stu-id="ce293-113">Condition</span></span> | <span data-ttu-id="ce293-114">Последовательность</span><span class="sxs-lookup"><span data-stu-id="ce293-114">Sequence</span></span> |
|-----------------|-----------|----------|
| <span data-ttu-id="ce293-115">админвелкомедлг</span><span class="sxs-lookup"><span data-stu-id="ce293-115">AdminWelcomeDlg</span></span> |           | <span data-ttu-id="ce293-116">1230</span><span class="sxs-lookup"><span data-stu-id="ce293-116">1230</span></span>     |
| <span data-ttu-id="ce293-117">костфинализе</span><span class="sxs-lookup"><span data-stu-id="ce293-117">CostFinalize</span></span>    |           | <span data-ttu-id="ce293-118">1000</span><span class="sxs-lookup"><span data-stu-id="ce293-118">1000</span></span>     |
| <span data-ttu-id="ce293-119">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="ce293-119">CostInitialize</span></span>  |           | <span data-ttu-id="ce293-120">800</span><span class="sxs-lookup"><span data-stu-id="ce293-120">800</span></span>      |
| <span data-ttu-id="ce293-121">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="ce293-121">ExecuteAction</span></span>   |           | <span data-ttu-id="ce293-122">1300</span><span class="sxs-lookup"><span data-stu-id="ce293-122">1300</span></span>     |
| <span data-ttu-id="ce293-123">екситдлг</span><span class="sxs-lookup"><span data-stu-id="ce293-123">ExitDlg</span></span>         |           | <span data-ttu-id="ce293-124">-1</span><span class="sxs-lookup"><span data-stu-id="ce293-124">-1</span></span>       |
| <span data-ttu-id="ce293-125">фаталеррордлг</span><span class="sxs-lookup"><span data-stu-id="ce293-125">FatalErrorDlg</span></span>   |           | <span data-ttu-id="ce293-126">–3</span><span class="sxs-lookup"><span data-stu-id="ce293-126">-3</span></span>       |
| <span data-ttu-id="ce293-127">филекост</span><span class="sxs-lookup"><span data-stu-id="ce293-127">FileCost</span></span>        |           | <span data-ttu-id="ce293-128">900</span><span class="sxs-lookup"><span data-stu-id="ce293-128">900</span></span>      |
| <span data-ttu-id="ce293-129">препаредлг</span><span class="sxs-lookup"><span data-stu-id="ce293-129">PrepareDlg</span></span>      |           | <span data-ttu-id="ce293-130">140</span><span class="sxs-lookup"><span data-stu-id="ce293-130">140</span></span>      |
| <span data-ttu-id="ce293-131">прогрессдлг</span><span class="sxs-lookup"><span data-stu-id="ce293-131">ProgressDlg</span></span>     |           | <span data-ttu-id="ce293-132">1280</span><span class="sxs-lookup"><span data-stu-id="ce293-132">1280</span></span>     |
| <span data-ttu-id="ce293-133">усерекситдлг</span><span class="sxs-lookup"><span data-stu-id="ce293-133">UserExitDlg</span></span>     |           | <span data-ttu-id="ce293-134">-2</span><span class="sxs-lookup"><span data-stu-id="ce293-134">-2</span></span>       |



 

[<span data-ttu-id="ce293-135">Продолжить</span><span class="sxs-lookup"><span data-stu-id="ce293-135">Continue</span></span>](importing-the-advtexecutesequence.md)

 

 



