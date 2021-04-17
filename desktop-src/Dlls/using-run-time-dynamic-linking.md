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
# <a name="using-run-time-dynamic-linking"></a>Использование Run-Time динамической компоновки

Одну и ту же библиотеку DLL можно использовать в динамической компоновке во время загрузки и во время выполнения. В следующем примере функция [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) используется для получения маркера библиотеки DLL мипутс (см. раздел [создание простой библиотеки Dynamic-Link](creating-a-simple-dynamic-link-library.md)). Если **LoadLibrary** выполняется, программа использует возвращенный маркер в функции [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения адреса функции мипутс библиотеки DLL. После вызова функции DLL программа вызывает функцию [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) для выгрузки библиотеки DLL.

Поскольку программа использует динамическую компоновку во время выполнения, нет необходимости связывать модуль с библиотекой импорта для библиотеки DLL.

Этот пример иллюстрирует важное различие между динамической компоновкой во время выполнения и временем загрузки. Если библиотека DLL недоступна, приложение, использующее динамическую компоновку во время загрузки, должно просто завершиться. Однако пример динамической компоновки времени выполнения может реагировать на ошибку.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Динамическая компоновка во время выполнения](run-time-dynamic-linking.md)
</dt> </dl>

 

 
