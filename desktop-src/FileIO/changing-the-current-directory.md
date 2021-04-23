---
description: Приложение может изменить текущий каталог, вызвав функцию Сеткуррентдиректори.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Изменение текущего каталога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e507d206bcd988a7c00f557bde2b8a0ad39c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684635"
---
# <a name="changing-the-current-directory"></a><span data-ttu-id="26b41-103">Изменение текущего каталога</span><span class="sxs-lookup"><span data-stu-id="26b41-103">Changing the Current Directory</span></span>

<span data-ttu-id="26b41-104">Каталог в конце активного пути называется текущим каталогом; это каталог, в котором запущено активное приложение, если оно не было явно изменено.</span><span class="sxs-lookup"><span data-stu-id="26b41-104">The directory at the end of the active path is called the current directory; it is the directory in which the active application started, unless it has been explicitly changed.</span></span> <span data-ttu-id="26b41-105">Приложение может определить, какой каталог является текущим, вызвав функцию [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="26b41-105">An application can determine which directory is current by calling the [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) function.</span></span> <span data-ttu-id="26b41-106">Иногда необходимо использовать функцию [**жетфуллпаснаме**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) , чтобы убедиться, что буква диска включена, если это требуется приложению.</span><span class="sxs-lookup"><span data-stu-id="26b41-106">It is sometimes necessary to use the [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) function to ensure the drive letter is included if the application requires it.</span></span>

> [!Note]  
> <span data-ttu-id="26b41-107">Хотя каждый процесс может иметь только один текущий каталог, если приложение переключает тома с помощью функции [**сеткуррентдиректори**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) , система запоминает последний текущий путь для каждого тома (буква диска).</span><span class="sxs-lookup"><span data-stu-id="26b41-107">Although each process can have only one current directory, if the application switches volumes by using the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function, the system remembers the last current path for each volume (drive letter).</span></span> <span data-ttu-id="26b41-108">Это поведение будет проявляться только при указании буквы диска без полного пути при изменении текущей точки ссылки на другой том.</span><span class="sxs-lookup"><span data-stu-id="26b41-108">This behavior will manifest itself only when specifying a drive letter without a fully qualified path when changing the current directory point of reference to a different volume.</span></span> <span data-ttu-id="26b41-109">Это относится к операциям get или Set.</span><span class="sxs-lookup"><span data-stu-id="26b41-109">This applies to either Get or Set operations.</span></span>

 

<span data-ttu-id="26b41-110">Приложение может изменить текущий каталог, вызвав функцию [**сеткуррентдиректори**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="26b41-110">An application can change the current directory by calling the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function.</span></span>

<span data-ttu-id="26b41-111">В следующем примере демонстрируется использование [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) и [**сеткуррентдиректори**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span><span class="sxs-lookup"><span data-stu-id="26b41-111">The following example demonstrates the use of [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) and [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span></span>


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



 

 



