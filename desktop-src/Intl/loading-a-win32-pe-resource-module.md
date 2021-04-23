---
description: В этом разделе описывается, как приложение загружает модуль ресурсов Win32 PE в Windows Vista и более поздней версии или более ранней версии операционной системы. Для освобождения модуля ресурсов включены вызовы.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Загрузка модуля ресурсов Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c4c1906a4fc09dc39b805e8ad5a875d96fae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664677"
---
# <a name="loading-a-win32-pe-resource-module"></a><span data-ttu-id="590c2-104">Загрузка модуля ресурсов Win32 PE</span><span class="sxs-lookup"><span data-stu-id="590c2-104">Loading a Win32 PE Resource Module</span></span>

<span data-ttu-id="590c2-105">В этом разделе описывается, как приложение загружает модуль ресурсов Win32 PE в Windows Vista и более поздней версии или более ранней версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="590c2-105">This topic describes how the application loads a Win32 PE resource module on either Windows Vista and later or on an earlier operating system.</span></span> <span data-ttu-id="590c2-106">Для освобождения модуля ресурсов включены вызовы.</span><span class="sxs-lookup"><span data-stu-id="590c2-106">Calls are included for releasing the resource module.</span></span>

## <a name="load-the-resource-module-on-windows-vista-and-later"></a><span data-ttu-id="590c2-107">Загрузка модуля ресурсов в Windows Vista и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="590c2-107">Load the Resource Module on Windows Vista and Later</span></span>

<span data-ttu-id="590c2-108">В Windows Vista и более поздних версиях приложение загружает модуль ресурсов с помощью вызова [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="590c2-108">On Windows Vista and later, the application loads the resource module using a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span> <span data-ttu-id="590c2-109">Рекомендуемая операция — вызвать эту функцию с обоими указанными флагами.</span><span class="sxs-lookup"><span data-stu-id="590c2-109">The recommended operation is to call this function with both flags specified.</span></span> <span data-ttu-id="590c2-110">Ниже приведен пример кода приложения, который загружает модуль на основе системных параметров языка.</span><span class="sxs-lookup"><span data-stu-id="590c2-110">The following is an example of application code that loads a module based on system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="590c2-111">Загрузка модуля ресурсов в операционных системах, предшествующих Windows Vista</span><span class="sxs-lookup"><span data-stu-id="590c2-111">Load the Resource Module on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="590c2-112">В операционных системах, предшествующих Windows Vista, приложение загружает модуль ресурсов на основе параметра языка, совместимого с целевой операционной системой, а также с Windows Vista и более поздними версиями.</span><span class="sxs-lookup"><span data-stu-id="590c2-112">On pre-Windows Vista operating systems, the application loads a resource module based on a language setting that is compatible with the target operating system, as well as Windows Vista and later.</span></span> <span data-ttu-id="590c2-113">Для этого типа загрузки модуля приложение должно вызывать функции многоязыкового интерфейса пользователя [**лоадмуилибрари**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) и [**фримуилибрари**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span><span class="sxs-lookup"><span data-stu-id="590c2-113">For this type of module loading, the application must call the MUI functions [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span></span>


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="590c2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="590c2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="590c2-115">Поиск ресурсов Win32 PE</span><span class="sxs-lookup"><span data-stu-id="590c2-115">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> <dt>

[<span data-ttu-id="590c2-116">MUI: пример параметров Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="590c2-116">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="590c2-117">MUI: образец параметров Application-Specific (до Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="590c2-117">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
