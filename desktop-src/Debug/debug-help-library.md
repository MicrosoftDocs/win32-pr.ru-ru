---
description: В этом обзоре описывается набор функций, предоставляемый отладочной библиотекой справки DbgHelp. Он содержит набор подпрограмм поддержки отладки, позволяющих работать с исполняемыми образами в переносимом исполняемом формате (PE).
ms.assetid: 71a5513d-bb89-4556-9266-57e7f92acf09
title: Отладка библиотеки справки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bccf284c0d22d3e9193b14255a24796b93a36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072351"
---
# <a name="debug-help-library"></a><span data-ttu-id="35f1f-104">Отладка библиотеки справки</span><span class="sxs-lookup"><span data-stu-id="35f1f-104">Debug Help Library</span></span>

<span data-ttu-id="35f1f-105">В этом обзоре описывается набор функций, предоставляемый отладочной библиотекой справки DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="35f1f-105">This overview describes the function set provided by the debug help library, DbgHelp.</span></span> <span data-ttu-id="35f1f-106">Он содержит набор подпрограмм поддержки отладки, позволяющих работать с исполняемыми образами в переносимом исполняемом формате (PE).</span><span class="sxs-lookup"><span data-stu-id="35f1f-106">It contains a set of debugging support routines that allow you to work with executable images in the portable executable (PE) format.</span></span>

<span data-ttu-id="35f1f-107">Документация по DbgHelp выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="35f1f-107">The DbgHelp documentation is as follows:</span></span>

- [<span data-ttu-id="35f1f-108">О DbgHelp</span><span class="sxs-lookup"><span data-stu-id="35f1f-108">About DbgHelp</span></span>](about-dbghelp.md)
- [<span data-ttu-id="35f1f-109">Использование DbgHelp</span><span class="sxs-lookup"><span data-stu-id="35f1f-109">Using DbgHelp</span></span>](using-dbghelp.md)
- [<span data-ttu-id="35f1f-110">Справочник по DbgHelp</span><span class="sxs-lookup"><span data-stu-id="35f1f-110">DbgHelp Reference</span></span>](dbghelp-reference.md)

<span data-ttu-id="35f1f-111">Чтобы получить последнюю версию DbgHelp.dll, перейдите на страницу [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) и скачайте средства отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="35f1f-111">To obtain the latest version of DbgHelp.dll, go to [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) and download Debugging Tools for Windows.</span></span>

<span data-ttu-id="35f1f-112">Чтобы получить описание формата PE, скачайте спецификацию по следующему адресу: [https://www.microsoft.com/whdc/system/platform/firmware/PECOFF.mspx](https://www.microsoft.com/whdc/system/platform/firmware/PECOFF.mspx) .</span><span class="sxs-lookup"><span data-stu-id="35f1f-112">For a description of the PE format, download the specification from the following location: [https://www.microsoft.com/whdc/system/platform/firmware/PECOFF.mspx](https://www.microsoft.com/whdc/system/platform/firmware/PECOFF.mspx).</span></span>

<span data-ttu-id="35f1f-113">Сведения о просмотре сведений, найденных в PDB-файлах, см. в разделе [SDK для доступа к интерфейсу отладки](/visualstudio/debugger/debug-interface-access/debug-interface-access-sdk?view=vs-2015).</span><span class="sxs-lookup"><span data-stu-id="35f1f-113">For information on how to browse information found in .pdb files, see the [Debug Interface Access SDK](/visualstudio/debugger/debug-interface-access/debug-interface-access-sdk?view=vs-2015).</span></span>
