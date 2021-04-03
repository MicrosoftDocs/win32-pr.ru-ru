---
title: Определение расположения общей папки
description: В следующем примере показано, как вызвать функцию Внетжетуниверсалнаме, чтобы определить расположение общей папки на перенаправленном диске.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987716"
---
# <a name="determining-the-location-of-a-share"></a><span data-ttu-id="67c42-103">Определение расположения общей папки</span><span class="sxs-lookup"><span data-stu-id="67c42-103">Determining the Location of a Share</span></span>

<span data-ttu-id="67c42-104">В следующем примере показано, как вызвать функцию [**внетжетуниверсалнаме**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) , чтобы определить расположение общей папки на перенаправленном диске.</span><span class="sxs-lookup"><span data-stu-id="67c42-104">The following example demonstrates how to call the [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) function to determine the location of a share on a redirected drive.</span></span>

<span data-ttu-id="67c42-105">Сначала в примере кода вызывается функция **внетжетуниверсалнаме** , указывающая уровень сведений о [**универсальном \_ имени \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) для получения указателя на строку имени в формате UNC для ресурса.</span><span class="sxs-lookup"><span data-stu-id="67c42-105">First the code sample calls the **WNetGetUniversalName** function, specifying the [**UNIVERSAL\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) information level to retrieve a pointer to a Universal Naming Convention (UNC) name string for the resource.</span></span> <span data-ttu-id="67c42-106">Затем пример вызывает **внетжетуниверсалнаме** во второй раз, указывая уровень информации об [**удаленном \_ имени \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) для получения двух дополнительных строк сведений о сетевом подключении.</span><span class="sxs-lookup"><span data-stu-id="67c42-106">Then the sample calls **WNetGetUniversalName** a second time, specifying the [**REMOTE\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) information level to retrieve two additional network connection information strings.</span></span> <span data-ttu-id="67c42-107">Если вызовы выполнены успешно, в примере выводится расположение общей папки.</span><span class="sxs-lookup"><span data-stu-id="67c42-107">If the calls are successful, the sample prints the location of the share.</span></span>

<span data-ttu-id="67c42-108">Чтобы протестировать следующий пример кода, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="67c42-108">To test the following code sample, perform the following steps:</span></span>

1.  <span data-ttu-id="67c42-109">Назовите пример кода Жетуни. cpp.</span><span class="sxs-lookup"><span data-stu-id="67c42-109">Name the code sample GetUni.cpp.</span></span>
2.  <span data-ttu-id="67c42-110">Добавьте пример в консольное приложение с именем Жетуни.</span><span class="sxs-lookup"><span data-stu-id="67c42-110">Add the sample to a console application called GetUni.</span></span>
3.  <span data-ttu-id="67c42-111">Свяжите библиотеки shell32. lib, MPR. lib и NetApi32. lib со списком библиотек в компиляторе.</span><span class="sxs-lookup"><span data-stu-id="67c42-111">Link the libraries Shell32.lib, Mpr.lib, and NetApi32.lib to the compiler list of libraries.</span></span>
4.  <span data-ttu-id="67c42-112">В командной строке перейдите в каталог Жетуни.</span><span class="sxs-lookup"><span data-stu-id="67c42-112">From the command prompt, change to the GetUni directory.</span></span>
5.  <span data-ttu-id="67c42-113">Скомпилируйте Жетуни. cpp.</span><span class="sxs-lookup"><span data-stu-id="67c42-113">Compile GetUni.cpp.</span></span>
6.  <span data-ttu-id="67c42-114">Запустите файл GetUni.exe, за которым следует буква диска и двоеточие, например:</span><span class="sxs-lookup"><span data-stu-id="67c42-114">Run the file GetUni.exe followed by a drive letter and colon, like this:</span></span>

    <span data-ttu-id="67c42-115">**Жетуни H:\\**</span><span class="sxs-lookup"><span data-stu-id="67c42-115">**GetUni H:\\**</span></span>


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



 

 