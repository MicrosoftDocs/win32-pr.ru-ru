---
description: Действие Патчфилес запрашивает таблицу исправлений, чтобы определить, какие исправления должны быть применены. Действие Патчфилес также выполняет обновление файлов по байтам.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Действие Патчфилес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909831"
---
# <a name="patchfiles-action"></a><span data-ttu-id="b0e71-104">Действие Патчфилес</span><span class="sxs-lookup"><span data-stu-id="b0e71-104">PatchFiles Action</span></span>

<span data-ttu-id="b0e71-105">Действие Патчфилес запрашивает [таблицу исправлений](patch-table.md) , чтобы определить, какие исправления должны быть применены.</span><span class="sxs-lookup"><span data-stu-id="b0e71-105">The PatchFiles action queries the [Patch table](patch-table.md) to determine which patches are to be applied.</span></span> <span data-ttu-id="b0e71-106">Действие Патчфилес также выполняет обновление файлов по байтам.</span><span class="sxs-lookup"><span data-stu-id="b0e71-106">The PatchFiles action also performs the byte-wise patching of the files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b0e71-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="b0e71-107">Sequence Restrictions</span></span>

<span data-ttu-id="b0e71-108">Если файл, который должен быть исправлен, не установлен, действие Патчфилес должно следовать после [действия инсталлфилес](installfiles-action.md) , устанавливающего файл.</span><span class="sxs-lookup"><span data-stu-id="b0e71-108">If the file that is to be patched is not installed, the PatchFiles action must come after the [InstallFiles action](installfiles-action.md) that installs the file.</span></span> <span data-ttu-id="b0e71-109">Ранее установленные файлы могут быть исправлены в любой точке последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="b0e71-109">Previously installed files may be patched at any point in the action sequence.</span></span> <span data-ttu-id="b0e71-110">[Действие дупликатефилес](duplicatefiles-action.md) должно следовать после действия патчфилес, чтобы предотвратить дублирование неисправленной версии файла.</span><span class="sxs-lookup"><span data-stu-id="b0e71-110">The [DuplicateFiles Action](duplicatefiles-action.md) must come after the PatchFiles action to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b0e71-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="b0e71-111">ActionData Messages</span></span>



| <span data-ttu-id="b0e71-112">Поле</span><span class="sxs-lookup"><span data-stu-id="b0e71-112">Field</span></span> | <span data-ttu-id="b0e71-113">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="b0e71-113">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="b0e71-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b0e71-114">\[1\]</span></span> | <span data-ttu-id="b0e71-115">Идентификатор исправленного файла.</span><span class="sxs-lookup"><span data-stu-id="b0e71-115">Identifier of patched file.</span></span>                   |
| <span data-ttu-id="b0e71-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="b0e71-116">\[2\]</span></span> | <span data-ttu-id="b0e71-117">Идентификатор каталога, содержащего исправленный файл.</span><span class="sxs-lookup"><span data-stu-id="b0e71-117">Identifier of directory holding patched file.</span></span> |
| <span data-ttu-id="b0e71-118">\[3\]</span><span class="sxs-lookup"><span data-stu-id="b0e71-118">\[3\]</span></span> | <span data-ttu-id="b0e71-119">Размер исправления в байтах.</span><span class="sxs-lookup"><span data-stu-id="b0e71-119">Size of patch in bytes.</span></span>                       |



 

 

 



