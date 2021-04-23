---
description: В таблице Админексекутесекуенце перечислены действия, выполняемые установщиком при вызове действия администратора верхнего уровня. См. раздел таблицы процедур установки, использование таблицы последовательности и подробный пример таблицы последовательности.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Импорт Админексекутесекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810738"
---
# <a name="importing-the-adminexecutesequence"></a><span data-ttu-id="aaa55-104">Импорт Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="aaa55-104">Importing the AdminExecuteSequence</span></span>

<span data-ttu-id="aaa55-105">В [таблице админексекутесекуенце](adminexecutesequence-table.md) перечислены действия, выполняемые установщиком при вызове [действия администратора](admin-action.md)верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="aaa55-105">The [AdminExecuteSequence table](adminexecutesequence-table.md) lists actions that the installer executes when it calls the top-level [ADMIN action](admin-action.md).</span></span> <span data-ttu-id="aaa55-106">См. раздел [таблицы процедур установки](installation-procedure-tables-group.md), [Использование таблицы последовательности](using-a-sequence-table.md)и [подробный пример таблицы последовательности](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="aaa55-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="aaa55-107">Если в разделе [импортируется пустая база данных](importing-a-blank-database.md) , которая использовалась uisample.msi из пакета SDK для установщик Windows, таблицы последовательности в копии MNP2000.msi уже содержат предлагаемые последовательности действий, описанные в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="aaa55-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="aaa55-108">Изменения этих последовательностей не требуются для создания образца установочного пакета Notepad.</span><span class="sxs-lookup"><span data-stu-id="aaa55-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="aaa55-109">Используйте редактор базы данных, чтобы открыть MNP2000.msi и ввести в таблицу Админексекутесекуенце следующие данные.</span><span class="sxs-lookup"><span data-stu-id="aaa55-109">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="aaa55-110">Таблица Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="aaa55-110">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)



| <span data-ttu-id="aaa55-111">Действие</span><span class="sxs-lookup"><span data-stu-id="aaa55-111">Action</span></span>              | <span data-ttu-id="aaa55-112">Условие</span><span class="sxs-lookup"><span data-stu-id="aaa55-112">Condition</span></span> | <span data-ttu-id="aaa55-113">Последовательность</span><span class="sxs-lookup"><span data-stu-id="aaa55-113">Sequence</span></span> |
|---------------------|-----------|----------|
| <span data-ttu-id="aaa55-114">костфинализе</span><span class="sxs-lookup"><span data-stu-id="aaa55-114">CostFinalize</span></span>        |           | <span data-ttu-id="aaa55-115">1000</span><span class="sxs-lookup"><span data-stu-id="aaa55-115">1000</span></span>     |
| <span data-ttu-id="aaa55-116">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="aaa55-116">CostInitialize</span></span>      |           | <span data-ttu-id="aaa55-117">800</span><span class="sxs-lookup"><span data-stu-id="aaa55-117">800</span></span>      |
| <span data-ttu-id="aaa55-118">филекост</span><span class="sxs-lookup"><span data-stu-id="aaa55-118">FileCost</span></span>            |           | <span data-ttu-id="aaa55-119">900</span><span class="sxs-lookup"><span data-stu-id="aaa55-119">900</span></span>      |
| <span data-ttu-id="aaa55-120">инсталладминпаккаже</span><span class="sxs-lookup"><span data-stu-id="aaa55-120">InstallAdminPackage</span></span> |           | <span data-ttu-id="aaa55-121">3900</span><span class="sxs-lookup"><span data-stu-id="aaa55-121">3900</span></span>     |
| <span data-ttu-id="aaa55-122">инсталлфилес</span><span class="sxs-lookup"><span data-stu-id="aaa55-122">InstallFiles</span></span>        |           | <span data-ttu-id="aaa55-123">4000</span><span class="sxs-lookup"><span data-stu-id="aaa55-123">4000</span></span>     |
| <span data-ttu-id="aaa55-124">Функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="aaa55-124">InstallFinalize</span></span>     |           | <span data-ttu-id="aaa55-125">6600</span><span class="sxs-lookup"><span data-stu-id="aaa55-125">6600</span></span>     |
| <span data-ttu-id="aaa55-126">инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="aaa55-126">InstallInitialize</span></span>   |           | <span data-ttu-id="aaa55-127">1500</span><span class="sxs-lookup"><span data-stu-id="aaa55-127">1500</span></span>     |
| <span data-ttu-id="aaa55-128">инсталлвалидате</span><span class="sxs-lookup"><span data-stu-id="aaa55-128">InstallValidate</span></span>     |           | <span data-ttu-id="aaa55-129">1400</span><span class="sxs-lookup"><span data-stu-id="aaa55-129">1400</span></span>     |



 

[<span data-ttu-id="aaa55-130">Продолжить</span><span class="sxs-lookup"><span data-stu-id="aaa55-130">Continue</span></span>](importing-the-adminuisequence.md)

 

 



