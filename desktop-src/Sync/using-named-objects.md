---
description: В следующем примере показано использование имен объектов путем создания и открытия именованного мьютекса.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Использование именованных объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349e3e26f661ca988bc5c5ebbc7b3c6ea622956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663406"
---
# <a name="using-named-objects"></a><span data-ttu-id="b6424-103">Использование именованных объектов</span><span class="sxs-lookup"><span data-stu-id="b6424-103">Using Named Objects</span></span>

<span data-ttu-id="b6424-104">В следующем примере показано использование [имен объектов](object-names.md) путем создания и открытия именованного мьютекса.</span><span class="sxs-lookup"><span data-stu-id="b6424-104">The following example illustrates the use of [object names](object-names.md) by creating and opening a named mutex.</span></span>

## <a name="first-process"></a><span data-ttu-id="b6424-105">Первый процесс</span><span class="sxs-lookup"><span data-stu-id="b6424-105">First Process</span></span>

<span data-ttu-id="b6424-106">Первый процесс использует функцию [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) для создания объекта Mutex.</span><span class="sxs-lookup"><span data-stu-id="b6424-106">The first process uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create the mutex object.</span></span> <span data-ttu-id="b6424-107">Обратите внимание, что эта функция может выполняться, даже если существует объект с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="b6424-107">Note that this function succeeds even if there is an existing object with the same name.</span></span>


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



## <a name="second-process"></a><span data-ttu-id="b6424-108">Второй процесс</span><span class="sxs-lookup"><span data-stu-id="b6424-108">Second Process</span></span>

<span data-ttu-id="b6424-109">Второй процесс использует функцию [**опенмутекс**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) для открытия маркера существующего мьютекса.</span><span class="sxs-lookup"><span data-stu-id="b6424-109">The second process uses the [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) function to open a handle to the existing mutex.</span></span> <span data-ttu-id="b6424-110">Эта функция завершается ошибкой, если объект мьютекса с указанным именем не существует.</span><span class="sxs-lookup"><span data-stu-id="b6424-110">This function fails if a mutex object with the specified name does not exist.</span></span> <span data-ttu-id="b6424-111">Параметр доступа запрашивает полный доступ к объекту Mutex, который необходим для использования маркера в любой из функций ожидания.</span><span class="sxs-lookup"><span data-stu-id="b6424-111">The access parameter requests full access to the mutex object, which is necessary for the handle to be used in any of the wait functions.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b6424-112">См. также</span><span class="sxs-lookup"><span data-stu-id="b6424-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6424-113">Имена объектов</span><span class="sxs-lookup"><span data-stu-id="b6424-113">Object Names</span></span>](object-names.md)
</dt> <dt>

[<span data-ttu-id="b6424-114">Использование объектов Mutex</span><span class="sxs-lookup"><span data-stu-id="b6424-114">Using Mutex Objects</span></span>](using-mutex-objects.md)
</dt> </dl>

 

 
