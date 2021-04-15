---
title: Сведения о версии
description: В этом разделе обсуждаются функции сведений о версии.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- ресурсы, сведения о версии
- сведения о версии
- добавление сведений о версии
- конфликты файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412857"
---
# <a name="about-version-information"></a><span data-ttu-id="60d6f-107">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="60d6f-107">About Version Information</span></span>

<span data-ttu-id="60d6f-108">Функции сведений о версии можно использовать для определения места установки файла и выявления конфликтов с установленными в настоящий момент файлами.</span><span class="sxs-lookup"><span data-stu-id="60d6f-108">You can use the version information functions to determine where a file should be installed and identify conflicts with currently installed files.</span></span> <span data-ttu-id="60d6f-109">Эти функции позволяют избежать следующих проблем:</span><span class="sxs-lookup"><span data-stu-id="60d6f-109">These functions enable you to avoid the following problems:</span></span>

-   <span data-ttu-id="60d6f-110">Установка старых версий компонентов более новых версий</span><span class="sxs-lookup"><span data-stu-id="60d6f-110">installing older versions of components over newer versions</span></span>
-   <span data-ttu-id="60d6f-111">изменение языка в системе на разных языках без уведомления</span><span class="sxs-lookup"><span data-stu-id="60d6f-111">changing the language in a mixed-language system without notification</span></span>
-   <span data-ttu-id="60d6f-112">Установка нескольких копий библиотеки в разных каталогах</span><span class="sxs-lookup"><span data-stu-id="60d6f-112">installing multiple copies of a library in different directories</span></span>
-   <span data-ttu-id="60d6f-113">копирование файлов в сетевые каталоги, совместно используемые несколькими пользователями</span><span class="sxs-lookup"><span data-stu-id="60d6f-113">copying files to network directories shared by multiple users</span></span>

<span data-ttu-id="60d6f-114">Функции сведений о версии позволяют приложениям запрашивать сведения о файле в ресурсе версии и представлять их в четком формате.</span><span class="sxs-lookup"><span data-stu-id="60d6f-114">The version information functions enable applications to query a version resource for file information and present the information in a clear format.</span></span> <span data-ttu-id="60d6f-115">Эти сведения включают назначение файла, автора, номер версии и т. д.</span><span class="sxs-lookup"><span data-stu-id="60d6f-115">This information includes the file's purpose, author, version number, and so on.</span></span>

<span data-ttu-id="60d6f-116">Сведения о версии можно добавлять в любые файлы, которые могут иметь ресурсы Windows, такие как DLL, исполняемые файлы или файлы шрифтов FON.</span><span class="sxs-lookup"><span data-stu-id="60d6f-116">You can add version information to any files that can have Windows resources, such as DLLs, executable files, or .fon font files.</span></span> <span data-ttu-id="60d6f-117">Чтобы добавить сведения, создайте [ресурс versionInfo](/windows/desktop/menurc/versioninfo-resource) и используйте компилятор ресурсов для компиляции ресурса.</span><span class="sxs-lookup"><span data-stu-id="60d6f-117">To add the information, create a [VERSIONINFO Resource](/windows/desktop/menurc/versioninfo-resource) and use the resource compiler to compile the resource.</span></span>

 

 