---
description: На странице защиты предоставляется оповещение одного снимка о доступе к странице памяти.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Создание страниц защиты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10768da75090a28ffecd5302d88dbc142ae9c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673308"
---
# <a name="creating-guard-pages"></a>Создание страниц защиты

На странице защиты предоставляется оповещение одного снимка о доступе к странице памяти. Это может быть полезно для приложения, которое должно отслеживать рост больших динамических структур данных. Например, существуют операционные системы, которые используют защищенные страницы для реализации автоматической проверки стека.

Чтобы создать охранную страницу, задайте для страницы модификатор защиты страницы **\_ охранных** страниц. Это значение можно указать вместе с другими модификаторами защиты страницы в функциях [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**виртуалаллоцекс**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)и [**виртуалпротектекс**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) . Модификатор **Page \_ Guard** можно использовать с любыми другими модификаторами защиты страницы, за исключением **страницы без \_ доступа**.

Если программа пытается получить доступ к адресу на странице защиты, система вызывает исключение **\_ \_ \_ нарушения страницы состояния** (0x80000001). Система также очищает модификатор Application **\_ Guard** , удаляя состояние страницы защиты страницы памяти. Система не будет прерывать следующую попытку доступа к странице памяти с исключением **\_ \_ \_ нарушения страницы состояния защиты** .

Если исключение страницы защиты возникает во время выполнения системной службы, служба завершается сбоем и обычно возвращает индикатор состояния сбоя. Так как система также удаляет состояние страницы защиты соответствующей страницы памяти, следующий вызов той же системной службы не будет выполнен из-за исключения **\_ \_ \_ нарушения страницы состояния** (если, конечно, кто-то воссоздает страницу защиты).

В следующей краткой программе демонстрируется поведение защиты страниц безопасности.


```C++
/* A program to demonstrate the use of guard pages of memory. Allocate
   a page of memory as a guard page, then try to access the page. That
   will fail, but doing so releases the lock on the guard page, so the
   next access works correctly.

   The output will look like this. The actual address may vary.

   This computer has a page size of 4096.
   Committed 4096 bytes at address 0x00520000
   Cannot lock at 00520000, error = 0x80000001
   2nd Lock Achieved at 00520000

   This sample does not show how to use the guard page fault to
   "grow" a dynamic array, such as a stack. */

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <tchar.h>

int main()
{
  LPVOID lpvAddr;               // address of the test memory
  DWORD dwPageSize;             // amount of memory to allocate.
  BOOL bLocked;                 // address of the guarded memory
  SYSTEM_INFO sSysInfo;         // useful information about the system

  GetSystemInfo(&sSysInfo);     // initialize the structure

  _tprintf(TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

  dwPageSize = sSysInfo.dwPageSize;

  // Try to allocate the memory.

  lpvAddr = VirtualAlloc(NULL, dwPageSize,
                         MEM_RESERVE | MEM_COMMIT,
                         PAGE_READONLY | PAGE_GUARD);

  if(lpvAddr == NULL) {
    _tprintf(TEXT("VirtualAlloc failed. Error: %ld\n"),
             GetLastError());
    return 1;

  } else {
    _ftprintf(stderr, TEXT("Committed %lu bytes at address 0x%lp\n"),
              dwPageSize, lpvAddr);
  }

  // Try to lock the committed memory. This fails the first time 
  // because of the guard page.

  bLocked = VirtualLock(lpvAddr, dwPageSize);
  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot lock at %lp, error = 0x%lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("Lock Achieved at %lp\n"), lpvAddr);
  }

  // Try to lock the committed memory again. This succeeds the second
  // time because the guard page status was removed by the first 
  // access attempt.

  bLocked = VirtualLock(lpvAddr, dwPageSize);

  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot get 2nd lock at %lp, error = %lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("2nd Lock Achieved at %lp\n"), lpvAddr);
  }

  return 0;
}
```



Первая попытка заблокировать блок памяти завершается ошибкой, что вызывает **исключение \_ \_ \_ нарушения страницы состояния** . Вторая предпринята успешно, так как защита страниц защиты блока памяти была отключена первой попытки.

 

 
