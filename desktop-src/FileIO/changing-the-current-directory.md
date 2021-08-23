---
description: Приложение может изменить текущий каталог, вызвав функцию Сеткуррентдиректори.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Изменение текущего каталога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf742c872bab7d37e115afa815fff961d2f975bfbd3db75ff61a5e992d64a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632114"
---
# <a name="changing-the-current-directory"></a>Изменение текущего каталога

Каталог в конце активного пути называется текущим каталогом; это каталог, в котором запущено активное приложение, если оно не было явно изменено. Приложение может определить, какой каталог является текущим, вызвав функцию [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) . Иногда необходимо использовать функцию [**жетфуллпаснаме**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) , чтобы убедиться, что буква диска включена, если это требуется приложению.

> [!Note]  
> Хотя каждый процесс может иметь только один текущий каталог, если приложение переключает тома с помощью функции [**сеткуррентдиректори**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) , система запоминает последний текущий путь для каждого тома (буква диска). Это поведение будет проявляться только при указании буквы диска без полного пути при изменении текущей точки ссылки на другой том. Это относится к операциям get или Set.

 

Приложение может изменить текущий каталог, вызвав функцию [**сеткуррентдиректори**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) .

В следующем примере демонстрируется использование [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) и [**сеткуррентдиректори**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH
 
void _tmain(int argc, TCHAR **argv) 
{ 
   TCHAR Buffer[BUFSIZE];
   DWORD dwRet;

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }

   dwRet = GetCurrentDirectory(BUFSIZE, Buffer);

   if( dwRet == 0 )
   {
      printf("GetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   if(dwRet > BUFSIZE)
   {
      printf("Buffer too small; need %d characters\n", dwRet);
      return;
   }

   if( !SetCurrentDirectory(argv[1]))
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Set current directory to %s\n"), argv[1]);

   if( !SetCurrentDirectory(Buffer) )
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Restored previous directory (%s)\n"), Buffer);
}
```



 

 



