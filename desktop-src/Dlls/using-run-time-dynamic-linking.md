---
description: Одну и ту же библиотеку DLL можно использовать в динамической компоновке во время загрузки и во время выполнения.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Использование Run-Time динамической компоновки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d6ca65c510433350b81a282d8bf7a3a3825ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683194"
---
# <a name="using-run-time-dynamic-linking"></a><span data-ttu-id="aec51-103">Использование Run-Time динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="aec51-103">Using Run-Time Dynamic Linking</span></span>

<span data-ttu-id="aec51-104">Одну и ту же библиотеку DLL можно использовать в динамической компоновке во время загрузки и во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="aec51-104">You can use the same DLL in both load-time and run-time dynamic linking.</span></span> <span data-ttu-id="aec51-105">В следующем примере функция [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) используется для получения маркера библиотеки DLL мипутс (см. раздел [создание простой библиотеки Dynamic-Link](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="aec51-105">The following example uses the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to get a handle to the Myputs DLL (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span> <span data-ttu-id="aec51-106">Если **LoadLibrary** выполняется, программа использует возвращенный маркер в функции [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения адреса функции мипутс библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="aec51-106">If **LoadLibrary** succeeds, the program uses the returned handle in the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to get the address of the DLL's myPuts function.</span></span> <span data-ttu-id="aec51-107">После вызова функции DLL программа вызывает функцию [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) для выгрузки библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="aec51-107">After calling the DLL function, the program calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function to unload the DLL.</span></span>

<span data-ttu-id="aec51-108">Поскольку программа использует динамическую компоновку во время выполнения, нет необходимости связывать модуль с библиотекой импорта для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="aec51-108">Because the program uses run-time dynamic linking, it is not necessary to link the module with an import library for the DLL.</span></span>

<span data-ttu-id="aec51-109">Этот пример иллюстрирует важное различие между динамической компоновкой во время выполнения и временем загрузки.</span><span class="sxs-lookup"><span data-stu-id="aec51-109">This example illustrates an important difference between run-time and load-time dynamic linking.</span></span> <span data-ttu-id="aec51-110">Если библиотека DLL недоступна, приложение, использующее динамическую компоновку во время загрузки, должно просто завершиться.</span><span class="sxs-lookup"><span data-stu-id="aec51-110">If the DLL is not available, the application using load-time dynamic linking must simply terminate.</span></span> <span data-ttu-id="aec51-111">Однако пример динамической компоновки времени выполнения может реагировать на ошибку.</span><span class="sxs-lookup"><span data-stu-id="aec51-111">The run-time dynamic linking example, however, can respond to the error.</span></span>


```C++
// A simple program that uses LoadLibrary and 
// GetProcAddress to access myPuts from Myputs.dll. 
 
#include <windows.h> 
#include <stdio.h> 
 
typedef int (__cdecl *MYPROC)(LPWSTR); 
 
int main( void ) 
{ 
    HINSTANCE hinstLib; 
    MYPROC ProcAdd; 
    BOOL fFreeResult, fRunTimeLinkSuccess = FALSE; 
 
    // Get a handle to the DLL module.
 
    hinstLib = LoadLibrary(TEXT("MyPuts.dll")); 
 
    // If the handle is valid, try to get the function address.
 
    if (hinstLib != NULL) 
    { 
        ProcAdd = (MYPROC) GetProcAddress(hinstLib, "myPuts"); 
 
        // If the function address is valid, call the function.
 
        if (NULL != ProcAdd) 
        {
            fRunTimeLinkSuccess = TRUE;
            (ProcAdd) (L"Message sent to the DLL function\n"); 
        }
        // Free the DLL module.
 
        fFreeResult = FreeLibrary(hinstLib); 
    } 

    // If unable to call the DLL function, use an alternative.
    if (! fRunTimeLinkSuccess) 
        printf("Message printed from executable\n"); 

    return 0;

}
```



## <a name="related-topics"></a><span data-ttu-id="aec51-112">См. также</span><span class="sxs-lookup"><span data-stu-id="aec51-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec51-113">Динамическая компоновка во время выполнения</span><span class="sxs-lookup"><span data-stu-id="aec51-113">Run-Time Dynamic Linking</span></span>](run-time-dynamic-linking.md)
</dt> </dl>

 

 
