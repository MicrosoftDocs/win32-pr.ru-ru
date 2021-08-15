---
description: В следующем примере показано использование имен объектов путем создания и открытия именованного мьютекса.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Использование именованных объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e31d21af713a28d5bee501349e818327750cba15a961ebd0f6a5295be91e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765133"
---
# <a name="using-named-objects"></a>Использование именованных объектов

В следующем примере показано использование [имен объектов](object-names.md) путем создания и открытия именованного мьютекса.

## <a name="first-process"></a>Первый процесс

Первый процесс использует функцию [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) для создания объекта Mutex. Обратите внимание, что эта функция может выполняться, даже если существует объект с таким же именем.


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>

// This process creates the mutex object.

int main(void)
{
    HANDLE hMutex; 

    hMutex = CreateMutex( 
        NULL,                        // default security descriptor
        FALSE,                       // mutex not owned
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("CreateMutex error: %d\n", GetLastError() ); 
    else 
        if ( GetLastError() == ERROR_ALREADY_EXISTS ) 
            printf("CreateMutex opened an existing mutex\n"); 
        else printf("CreateMutex created a new mutex.\n");

    // Keep this process around until the second process is run
    _getch();

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="second-process"></a>Второй процесс

Второй процесс использует функцию [**опенмутекс**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) для открытия маркера существующего мьютекса. Эта функция завершается ошибкой, если объект мьютекса с указанным именем не существует. Параметр доступа запрашивает полный доступ к объекту Mutex, который необходим для использования маркера в любой из функций ожидания.


```C++
#include <windows.h>
#include <stdio.h>

// This process opens a handle to a mutex created by another process.

int main(void)
{
    HANDLE hMutex; 

    hMutex = OpenMutex( 
        MUTEX_ALL_ACCESS,            // request full access
        FALSE,                       // handle not inheritable
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("OpenMutex error: %d\n", GetLastError() );
    else printf("OpenMutex successfully opened the mutex.\n");

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Имена объектов](object-names.md)
</dt> <dt>

[Использование объектов Mutex](using-mutex-objects.md)
</dt> </dl>

 

 
