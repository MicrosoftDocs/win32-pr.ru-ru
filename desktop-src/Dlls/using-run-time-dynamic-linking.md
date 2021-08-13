---
description: Одну и ту же библиотеку DLL можно использовать в динамической компоновке во время загрузки и во время выполнения.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Использование Run-Time динамической компоновки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c13cc66a34f0fd5938fcdada027b30223ebff0abe6e9ce459d60f93a6546f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255984"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Динамическая компоновка во время выполнения](run-time-dynamic-linking.md)
</dt> </dl>

 

 
