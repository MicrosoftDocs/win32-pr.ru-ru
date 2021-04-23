---
description: Загрузка языковых ресурсов
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Загрузка языковых ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6917f03e773a470288fb4c9577812e0b38868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350305"
---
# <a name="loading-language-resources"></a><span data-ttu-id="69760-103">Загрузка языковых ресурсов</span><span class="sxs-lookup"><span data-stu-id="69760-103">Loading Language Resources</span></span>

<span data-ttu-id="69760-104">Приложение загружает все языковые ресурсы пользовательского интерфейса, кроме определенных перенаправленных строк реестра, используя вызовы стандартных функций загрузки ресурсов, например [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa)и [**лоадимаже**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span><span class="sxs-lookup"><span data-stu-id="69760-104">Your application loads all user interface language resources, other than certain redirected registry strings, using calls to standard resource loading functions, for example, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), and [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span></span> <span data-ttu-id="69760-105">Многие функции загрузки ресурсов были изменены для автоматической загрузки ресурсов из файлов ресурсов, зависящих от языка, которые обрабатывают ресурсы так, как если бы они содержались в LN-файле.</span><span class="sxs-lookup"><span data-stu-id="69760-105">Many resource loading functions have been modified to load resources from language-specific resource files automatically, treating resources as if they are contained in the LN file.</span></span> <span data-ttu-id="69760-106">В следующем примере показано использование **лоадстринг** для загрузки языковых строк для приложения, которое соответствует системным параметрам языка.</span><span class="sxs-lookup"><span data-stu-id="69760-106">The following example illustrates the use of **LoadString** to load language strings for an application that follows system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="69760-107">См. также</span><span class="sxs-lookup"><span data-stu-id="69760-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69760-108">Поиск ресурсов Win32 PE</span><span class="sxs-lookup"><span data-stu-id="69760-108">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> </dl>

 

 
