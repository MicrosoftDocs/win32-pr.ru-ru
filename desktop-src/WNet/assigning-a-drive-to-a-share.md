---
title: Назначение диска общему ресурсу
description: В следующем примере показано, как подключить букву диска к удаленному общему серверу с помощью вызова функции WNetAddConnection2. Пример информирует пользователя о том, был ли вызов успешным.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cb4c930250f74cc549d9b5a31f121b92abad0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413305"
---
# <a name="assigning-a-drive-to-a-share"></a><span data-ttu-id="94e0f-104">Назначение диска общему ресурсу</span><span class="sxs-lookup"><span data-stu-id="94e0f-104">Assigning a Drive to a Share</span></span>

<span data-ttu-id="94e0f-105">В следующем примере показано, как подключить букву диска к удаленному общему серверу с помощью вызова функции [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) .</span><span class="sxs-lookup"><span data-stu-id="94e0f-105">The following example demonstrates how to connect a drive letter to a remote server share with a call to the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function.</span></span> <span data-ttu-id="94e0f-106">Пример информирует пользователя о том, был ли вызов успешным.</span><span class="sxs-lookup"><span data-stu-id="94e0f-106">The sample informs the user whether or not the call was successful.</span></span>

<span data-ttu-id="94e0f-107">Чтобы протестировать следующий пример кода, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="94e0f-107">To test the following code sample, perform the following steps:</span></span>

1.  <span data-ttu-id="94e0f-108">Измените следующие строки на допустимые строки:</span><span class="sxs-lookup"><span data-stu-id="94e0f-108">Change the following lines to valid strings:</span></span>

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  <span data-ttu-id="94e0f-109">Добавьте файл в консольное приложение с именем AddConn2.</span><span class="sxs-lookup"><span data-stu-id="94e0f-109">Add the file to a console application called AddConn2.</span></span>
3.  <span data-ttu-id="94e0f-110">Свяжите библиотеку MPR. LIB в список библиотек в компиляторе.</span><span class="sxs-lookup"><span data-stu-id="94e0f-110">Link the library MPR.LIB to the compiler list of libraries.</span></span>
4.  <span data-ttu-id="94e0f-111">Скомпилируйте и запустите программу AddConn2.EXE.</span><span class="sxs-lookup"><span data-stu-id="94e0f-111">Compile and run the program AddConn2.EXE.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>
#pragma comment(lib, "mpr.lib")

void main()
{
NETRESOURCE nr;
DWORD res;
TCHAR szUserName[32] = "MyUserName",
    szPassword[32] = "MyPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
//
// Assign values to the NETRESOURCE structure.
//
nr.dwType = RESOURCETYPE_ANY;
nr.lpLocalName = szLocalName;
nr.lpRemoteName = szRemoteName;
nr.lpProvider = NULL;
//
// Call the WNetAddConnection2 function to assign
//   a drive letter to the share.
//
res = WNetAddConnection2(&nr, szPassword, szUserName, FALSE);
//
// If the call succeeds, inform the user; otherwise,
//  print the error.
//
if(res == NO_ERROR)
  printf("Connection added \n", szRemoteName);
else
  printf("Error: %ld\n", res);
  return;
}
```



 

 