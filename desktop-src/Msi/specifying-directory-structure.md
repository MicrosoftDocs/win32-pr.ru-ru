---
description: Установщик сохраняет сведения о структуре каталогов установки в таблице Directory.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Указание структуры каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897677"
---
# <a name="specifying-directory-structure"></a><span data-ttu-id="a38cb-103">Указание структуры каталогов</span><span class="sxs-lookup"><span data-stu-id="a38cb-103">Specifying Directory Structure</span></span>

<span data-ttu-id="a38cb-104">Установщик сохраняет сведения о структуре каталогов установки в [таблице Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="a38cb-104">The installer keeps information about the installation directory structure in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="a38cb-105">См. раздел [группа основных таблиц](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="a38cb-105">See the [Core Tables Group](core-tables-group.md).</span></span> <span data-ttu-id="a38cb-106">В этом разделе вы добавите сведения о структуре каталогов для примера "Блокнот" в пустую базу данных, созданную при [импорте пустой базы данных](importing-a-blank-database.md).</span><span class="sxs-lookup"><span data-stu-id="a38cb-106">In this section you add directory structure information for the Notepad sample to the empty database you created in [Importing a Blank Database](importing-a-blank-database.md).</span></span> <span data-ttu-id="a38cb-107">Используйте редактор базы данных Orca, поставляемый вместе с пакетом SDK, или другой редактор, чтобы открыть таблицу Directory в MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="a38cb-107">Use the database editor Orca that is provided with the SDK, or another editor, to open the Directory Table in MNP2000.msi.</span></span> <span data-ttu-id="a38cb-108">Используйте редактор для ввода следующих данных в таблицу пустого каталога.</span><span class="sxs-lookup"><span data-stu-id="a38cb-108">Use the editor to enter the following data into the blank Directory table.</span></span>

[<span data-ttu-id="a38cb-109">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="a38cb-109">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="a38cb-110">Каталог</span><span class="sxs-lookup"><span data-stu-id="a38cb-110">Directory</span></span>                                        | <span data-ttu-id="a38cb-111">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="a38cb-111">Directory\_Parent</span></span>                                | <span data-ttu-id="a38cb-112">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="a38cb-112">DefaultDir</span></span>        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [<span data-ttu-id="a38cb-113">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="a38cb-113">**TARGETDIR**</span></span>](targetdir.md)                   |                                                  | <span data-ttu-id="a38cb-114">SourceDir</span><span class="sxs-lookup"><span data-stu-id="a38cb-114">SourceDir</span></span>         |
| [<span data-ttu-id="a38cb-115">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="a38cb-115">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | [<span data-ttu-id="a38cb-116">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="a38cb-116">**TARGETDIR**</span></span>](targetdir.md)                   | <span data-ttu-id="a38cb-117">.</span><span class="sxs-lookup"><span data-stu-id="a38cb-117">.</span></span>                 |
| <span data-ttu-id="a38cb-118">артсдир</span><span class="sxs-lookup"><span data-stu-id="a38cb-118">ARTSDIR</span></span>                                          | <span data-ttu-id="a38cb-119">нотепаддир</span><span class="sxs-lookup"><span data-stu-id="a38cb-119">NOTEPADDIR</span></span>                                       | <span data-ttu-id="a38cb-120">Искусство: события</span><span class="sxs-lookup"><span data-stu-id="a38cb-120">Arts:Events</span></span>       |
| <span data-ttu-id="a38cb-121">холдир</span><span class="sxs-lookup"><span data-stu-id="a38cb-121">HOLDIR</span></span>                                           | <span data-ttu-id="a38cb-122">мондир</span><span class="sxs-lookup"><span data-stu-id="a38cb-122">MONDIR</span></span>                                           | <span data-ttu-id="a38cb-123">.: Праздники</span><span class="sxs-lookup"><span data-stu-id="a38cb-123">.:Holidays</span></span>        |
| <span data-ttu-id="a38cb-124">менудир</span><span class="sxs-lookup"><span data-stu-id="a38cb-124">MENUDIR</span></span>                                          | <span data-ttu-id="a38cb-125">нотепаддир</span><span class="sxs-lookup"><span data-stu-id="a38cb-125">NOTEPADDIR</span></span>                                       | <span data-ttu-id="a38cb-126">Меню</span><span class="sxs-lookup"><span data-stu-id="a38cb-126">Menu</span></span>              |
| <span data-ttu-id="a38cb-127">мондир</span><span class="sxs-lookup"><span data-stu-id="a38cb-127">MONDIR</span></span>                                           | <span data-ttu-id="a38cb-128">нотепаддир</span><span class="sxs-lookup"><span data-stu-id="a38cb-128">NOTEPADDIR</span></span>                                       | <span data-ttu-id="a38cb-129">Frame</span><span class="sxs-lookup"><span data-stu-id="a38cb-129">Gate</span></span>              |
| <span data-ttu-id="a38cb-130">нотепаддир</span><span class="sxs-lookup"><span data-stu-id="a38cb-130">NOTEPADDIR</span></span>                                       | [<span data-ttu-id="a38cb-131">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="a38cb-131">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | <span data-ttu-id="a38cb-132">Красный \_ парк: Блокнот</span><span class="sxs-lookup"><span data-stu-id="a38cb-132">Red\_Park:Notepad</span></span> |
| <span data-ttu-id="a38cb-133">спортдир</span><span class="sxs-lookup"><span data-stu-id="a38cb-133">SPORTDIR</span></span>                                         | <span data-ttu-id="a38cb-134">нотепаддир</span><span class="sxs-lookup"><span data-stu-id="a38cb-134">NOTEPADDIR</span></span>                                       | <span data-ttu-id="a38cb-135">Спорт: события</span><span class="sxs-lookup"><span data-stu-id="a38cb-135">Sports:Events</span></span>     |



 

<span data-ttu-id="a38cb-136">Ввод этих данных в таблицу Directory задает структуры исходного и целевого каталогов.</span><span class="sxs-lookup"><span data-stu-id="a38cb-136">Entering this data into the Directory table specifies the source and target directory structures.</span></span> <span data-ttu-id="a38cb-137">См. [таблицу Directory](directory-table.md) и разделы [таблицы каталогов](using-the-directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a38cb-137">See the [Directory Table](directory-table.md) and [Using the Directory Table](using-the-directory-table.md) topics.</span></span> <span data-ttu-id="a38cb-138">Обратите внимание, что свойство [**targetDir**](targetdir.md) должно быть именем одного корня в таблице Directory каждой установки.</span><span class="sxs-lookup"><span data-stu-id="a38cb-138">Note that the [**TARGETDIR**](targetdir.md) property must be the name of one root in the Directory table of every installation.</span></span>

[<span data-ttu-id="a38cb-139">Продолжить</span><span class="sxs-lookup"><span data-stu-id="a38cb-139">Continue</span></span>](specifying-components.md)

 

 



