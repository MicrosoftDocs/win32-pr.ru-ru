---
title: Назначение диска общему ресурсу
description: В следующем примере показано, как подключить букву диска к удаленному общему серверу с помощью вызова функции WNetAddConnection2. Пример информирует пользователя о том, был ли вызов успешным.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37095f085b3124cfaa049de4bf61ae830c94191c94c5993f7532920b122b63d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053382"
---
# <a name="assigning-a-drive-to-a-share"></a>Назначение диска общему ресурсу

В следующем примере показано, как подключить букву диска к удаленному общему серверу с помощью вызова функции [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) . Пример информирует пользователя о том, был ли вызов успешным.

Чтобы протестировать следующий пример кода, выполните следующие действия.

1.  Измените следующие строки на допустимые строки:

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  Добавьте файл в консольное приложение с именем AddConn2.
3.  Свяжите библиотеку MPR. LIB в список библиотек в компиляторе.
4.  Скомпилируйте и запустите программу AddConn2.EXE.


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



 

 