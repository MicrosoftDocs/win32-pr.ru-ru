---
title: Определение расположения общей папки
description: В следующем примере показано, как вызвать функцию Внетжетуниверсалнаме, чтобы определить расположение общей папки на перенаправленном диске.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a881d452c6aa9eac5eea85d4ef0e9ddce83524f001294d2a6d6d6307f5ff1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566897"
---
# <a name="determining-the-location-of-a-share"></a>Определение расположения общей папки

В следующем примере показано, как вызвать функцию [**внетжетуниверсалнаме**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) , чтобы определить расположение общей папки на перенаправленном диске.

Сначала в примере кода вызывается функция **внетжетуниверсалнаме** , указывающая уровень сведений о [**универсальном \_ имени \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) для получения указателя на строку имени в формате UNC для ресурса. Затем пример вызывает **внетжетуниверсалнаме** во второй раз, указывая уровень информации об [**удаленном \_ имени \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) для получения двух дополнительных строк сведений о сетевом подключении. Если вызовы выполнены успешно, в примере выводится расположение общей папки.

Чтобы протестировать следующий пример кода, выполните следующие действия.

1.  Назовите пример кода Жетуни. cpp.
2.  Добавьте пример в консольное приложение с именем Жетуни.
3.  Свяжите библиотеки shell32. lib, MPR. lib и NetApi32. lib со списком библиотек в компиляторе.
4.  В командной строке перейдите в каталог Жетуни.
5.  Скомпилируйте Жетуни. cpp.
6.  Запустите файл GetUni.exe, за которым следует буква диска и двоеточие, например:

    **Жетуни H:\\**


```C++
#define  STRICT
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")

#define BUFFSIZE = 1000

void main( int argc, char *argv[] )
{
  DWORD cbBuff = 1000;    // Size of Buffer
  TCHAR szBuff[1000];    // Buffer to receive information
  REMOTE_NAME_INFO  * prni = (REMOTE_NAME_INFO *)   &szBuff;
  UNIVERSAL_NAME_INFO * puni = (UNIVERSAL_NAME_INFO *) &szBuff;
  DWORD res;

  if((argc < 2) | (lstrcmp(argv[1], "/?") == 0))
  {
    printf("Syntax:  GetUni DrivePathAndFilename\n"
         "Example: GetUni U:\\WINNT\\SYSTEM32\\WSOCK32.DLL\n");
    return;
  }
  
  // Call WNetGetUniversalName with the UNIVERSAL_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using UNIVERSAL_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1],
         UNIVERSAL_NAME_INFO_LEVEL, // The structure is written to this block of memory. 
         (LPVOID) &szBuff, 
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print the location of the share, 
    //  using the pointer to UNIVERSAL_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n\n", res); 
   
  else
    _tprintf(TEXT("Universal Name: \t%s\n\n"), puni->lpUniversalName); 
    
  //
  // Call WNetGetUniversalName with the REMOTE_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using REMOTE_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1], 
         REMOTE_NAME_INFO_LEVEL, 
         (LPVOID) &szBuff,    //Structure is written to this block of memory
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print
    //  the location of the share, using 
    //  the pointer to REMOTE_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n", res); 
  else
    _tprintf(TEXT("Universal Name: \t%s\nConnection Name:\t%s\nRemaining Path: \t%s\n"),
          prni->lpUniversalName, 
          prni->lpConnectionName, 
          prni->lpRemainingPath);
  return;
}
```



 

 