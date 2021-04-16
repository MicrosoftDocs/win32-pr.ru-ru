---
description: Подготовка ресурсов для приложения MUI поддерживает модели Win32 PE и не Win32 PE.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Подготовка ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684241"
---
# <a name="preparing-resources"></a><span data-ttu-id="b1008-103">Подготовка ресурсов</span><span class="sxs-lookup"><span data-stu-id="b1008-103">Preparing Resources</span></span>

<span data-ttu-id="b1008-104">Подготовка ресурсов для приложения MUI поддерживает модели Win32 PE и не Win32 PE.</span><span class="sxs-lookup"><span data-stu-id="b1008-104">Resource preparation for a MUI application supports both Win32 PE and non-Win32 PE models.</span></span> <span data-ttu-id="b1008-105">Ресурсы Win32 PE предоставляются в файлах на основе PE, таких как DLL, exe или sys-файлы.</span><span class="sxs-lookup"><span data-stu-id="b1008-105">Win32 PE resources are provided in PE-based files, such as .dll, .exe, or .sys files.</span></span> <span data-ttu-id="b1008-106">Ресурсы PE, отличные от Win32, предоставляются в настраиваемом модуле по своему выбору.</span><span class="sxs-lookup"><span data-stu-id="b1008-106">Non-Win32 PE resources are furnished in a customized module of your choosing.</span></span>

> [!Note]  
> <span data-ttu-id="b1008-107">Настоятельно рекомендуется использовать ресурсы Win32 PE для приложений Win32 MUI, так как эти ресурсы полностью поддерживаются технологией ресурсов MUI.</span><span class="sxs-lookup"><span data-stu-id="b1008-107">It is highly recommended for you to use Win32 PE resources for Win32 MUI applications, as these resources are completely supported by the MUI resource technology.</span></span> <span data-ttu-id="b1008-108">Файлы ресурсов, не относящиеся к Win32 PE, можно найти, вызвав функцию [**жетфилемуипас**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) , как описано в разделе [Поиск ресурсов PE, отличных от Win32](locating-non-win32-pe-resources.md), но приложение должно предоставить собственные функции для поиска и загрузки необходимых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1008-108">Non-Win32 PE resource files can be located by calling the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function as described in [Locating Non-Win32 PE Resources](locating-non-win32-pe-resources.md), but the application must provide its own functionality to find and load the required resources.</span></span>

 

<span data-ttu-id="b1008-109">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="b1008-109">This section contains the following topics:</span></span>

-   [<span data-ttu-id="b1008-110">Создание файла ресурсов базового языка</span><span class="sxs-lookup"><span data-stu-id="b1008-110">Creating the Base Language Resource File</span></span>](creating-the-base-language-resource-file.md)
-   [<span data-ttu-id="b1008-111">Использование перенаправления строк реестра</span><span class="sxs-lookup"><span data-stu-id="b1008-111">Using Registry String Redirection</span></span>](using-registry-string-redirection.md)
-   [<span data-ttu-id="b1008-112">Подготовка файла конфигурации ресурса</span><span class="sxs-lookup"><span data-stu-id="b1008-112">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)

 

 



