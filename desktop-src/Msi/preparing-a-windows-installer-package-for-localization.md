---
description: Следуйте этим рекомендациям, чтобы упростить локализацию пакетов установщик Windows.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Подготовка пакета установщик Windows для локализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650476"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a><span data-ttu-id="f62e5-103">Подготовка пакета установщик Windows для локализации</span><span class="sxs-lookup"><span data-stu-id="f62e5-103">Preparing a Windows Installer Package for Localization</span></span>

<span data-ttu-id="f62e5-104">Локализация пакета установщик Windows на несколько языков может значительно облегчить выполнение следующих действий.</span><span class="sxs-lookup"><span data-stu-id="f62e5-104">Localization of a Windows Installer package into multiple languages can be greatly facilitated by doing the following:</span></span>

-   <span data-ttu-id="f62e5-105">Создайте базовую базу данных установки с нейтральной кодовой страницей.</span><span class="sxs-lookup"><span data-stu-id="f62e5-105">Author a base installation database that is code page neutral.</span></span> <span data-ttu-id="f62e5-106">См. раздел [Создание базы данных с нейтральной кодовой страницей](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="f62e5-106">See [Creating a database with a neutral code page](creating-a-database-with-a-neutral-code-page.md).</span></span> <span data-ttu-id="f62e5-107">Затем можно установить кодовую страницу локализованной базы данных, импортировав таблицу с ненейтральной кодовой страницей в основную базу данных.</span><span class="sxs-lookup"><span data-stu-id="f62e5-107">The code page of the localized database can then be set by importing a text archive table with a non-neutral code page into the base database.</span></span> <span data-ttu-id="f62e5-108">См. раздел [Настройка кодовой страницы базы данных](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="f62e5-108">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="f62e5-109">Упорядочите файлы, которые требуют локализации, в отдельные компоненты и устанавливайте эти файлы в отдельные каталоги.</span><span class="sxs-lookup"><span data-stu-id="f62e5-109">Organize files requiring localization into separate components and install these files into separate directories.</span></span> <span data-ttu-id="f62e5-110">Это гарантирует, что два локализованных пакета никогда не устанавливают файлы с одинаковыми именами в один каталог.</span><span class="sxs-lookup"><span data-stu-id="f62e5-110">This ensures that two localized packages never install identically named files into the same directory.</span></span>

<span data-ttu-id="f62e5-111">Например, приложение мирового типа, использующее следующие ресурсы, может иметь три компонента.</span><span class="sxs-lookup"><span data-stu-id="f62e5-111">For example, a worldwide application using the following resources may have three components.</span></span>



| <span data-ttu-id="f62e5-112">Компонент</span><span class="sxs-lookup"><span data-stu-id="f62e5-112">Component</span></span> | <span data-ttu-id="f62e5-113">Ресурс</span><span class="sxs-lookup"><span data-stu-id="f62e5-113">Resource</span></span>                   |
|-----------|----------------------------|
| <span data-ttu-id="f62e5-114">РЕАЛЬНОГО</span><span class="sxs-lookup"><span data-stu-id="f62e5-114">WORLD</span></span>     | <span data-ttu-id="f62e5-115">worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="f62e5-115">worldwide.exe</span></span>              |
| <span data-ttu-id="f62e5-116">РЕАЛЬНОГО</span><span class="sxs-lookup"><span data-stu-id="f62e5-116">WORLD</span></span>     | <span data-ttu-id="f62e5-117">записи реестра для всех стран</span><span class="sxs-lookup"><span data-stu-id="f62e5-117">worldwide registry entries</span></span> |
| <span data-ttu-id="f62e5-118">РЕАЛЬНОГО</span><span class="sxs-lookup"><span data-stu-id="f62e5-118">WORLD</span></span>     | <span data-ttu-id="f62e5-119">международные сочетания</span><span class="sxs-lookup"><span data-stu-id="f62e5-119">worldwide shortcut</span></span>         |
| <span data-ttu-id="f62e5-120">ENG</span><span class="sxs-lookup"><span data-stu-id="f62e5-120">ENG</span></span>       | <span data-ttu-id="f62e5-121">engui.dll</span><span class="sxs-lookup"><span data-stu-id="f62e5-121">engui.dll</span></span>                  |
| <span data-ttu-id="f62e5-122">ENG</span><span class="sxs-lookup"><span data-stu-id="f62e5-122">ENG</span></span>       | <span data-ttu-id="f62e5-123">readMe.txt</span><span class="sxs-lookup"><span data-stu-id="f62e5-123">readme.txt</span></span>                 |
| <span data-ttu-id="f62e5-124">FRA</span><span class="sxs-lookup"><span data-stu-id="f62e5-124">FRA</span></span>       | <span data-ttu-id="f62e5-125">fraui.dll</span><span class="sxs-lookup"><span data-stu-id="f62e5-125">fraui.dll</span></span>                  |
| <span data-ttu-id="f62e5-126">FRA</span><span class="sxs-lookup"><span data-stu-id="f62e5-126">FRA</span></span>       | <span data-ttu-id="f62e5-127">readMe.txt</span><span class="sxs-lookup"><span data-stu-id="f62e5-127">readme.txt</span></span>                 |



 

<span data-ttu-id="f62e5-128">Файлы, которые необходимо локализовать, можно установить в следующие каталоги:</span><span class="sxs-lookup"><span data-stu-id="f62e5-128">The files that need to be localized may be installed into the following directory locations:</span></span>

-   <span data-ttu-id="f62e5-129">\[ProgramFilesFolder \] \\ World \\worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="f62e5-129">\[ProgramFilesFolder\]\\World\\worldwide.exe</span></span>
-   <span data-ttu-id="f62e5-130">\[\] \\ \\ Английскийengui.dll ProgramFilesFolder \\ World</span><span class="sxs-lookup"><span data-stu-id="f62e5-130">\[ProgramFilesFolder\]\\World\\English\\engui.dll</span></span>
-   <span data-ttu-id="f62e5-131">\[\] \\ \\ Английскийreadme.txt ProgramFilesFolder \\ World</span><span class="sxs-lookup"><span data-stu-id="f62e5-131">\[ProgramFilesFolder\]\\World\\English\\readme.txt</span></span>
-   <span data-ttu-id="f62e5-132">\[ProgramFilesFolder \] \\ мира на \\ французском языке \\fraui.dll</span><span class="sxs-lookup"><span data-stu-id="f62e5-132">\[ProgramFilesFolder\]\\World\\French\\fraui.dll</span></span>
-   <span data-ttu-id="f62e5-133">\[ProgramFilesFolder \] \\ мира на \\ французском языке \\readme.txt</span><span class="sxs-lookup"><span data-stu-id="f62e5-133">\[ProgramFilesFolder\]\\World\\French\\readme.txt</span></span>

 

 



