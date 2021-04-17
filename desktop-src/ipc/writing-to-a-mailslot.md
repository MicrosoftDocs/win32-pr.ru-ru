---
description: Запись в почтовый слот. Запись в почтовый слот аналогична записи в файл стандартного диска.
ms.assetid: a69ba953-cd5c-487f-b9e0-dbd6c44b88b8
title: Запись в почтовый слот
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568727f7a83d46925f3e681f3dec4906903ca8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693523"
---
# <a name="writing-to-a-mailslot"></a>Запись в почтовый слот

Запись в почтовый слот аналогична записи в файл стандартного диска. В следующем коде функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)и [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) используются для помещения короткого сообщения в почтовый слот. Сообщение передается на сервер слота с именем "образец \_ слота сообщений" на локальном компьютере. Код работает в соответствии с предположением о том, что сервер слота уже создан.


```C++
#include <windows.h>
#include <stdio.h>

LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WriteSlot(HANDLE hSlot, LPCTSTR lpszMessage)
{
   BOOL fResult; 
   DWORD cbWritten; 
 
   fResult = WriteFile(hSlot, 
     lpszMessage, 
     (DWORD) (lstrlen(lpszMessage)+1)*sizeof(TCHAR),  
     &cbWritten, 
     (LPOVERLAPPED) NULL); 
 
   if (!fResult) 
   { 
      printf("WriteFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   printf("Slot written to successfully.\n"); 

   return TRUE;
}

int main()
{ 
   HANDLE hFile; 

   hFile = CreateFile(SlotName, 
     GENERIC_WRITE, 
     FILE_SHARE_READ,
     (LPSECURITY_ATTRIBUTES) NULL, 
     OPEN_EXISTING, 
     FILE_ATTRIBUTE_NORMAL, 
     (HANDLE) NULL); 
 
   if (hFile == INVALID_HANDLE_VALUE) 
   { 
      printf("CreateFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   WriteSlot(hFile, TEXT("Message one for mailslot."));
   WriteSlot(hFile, TEXT("Message two for mailslot."));

   Sleep(5000);

   WriteSlot(hFile, TEXT("Message three for mailslot."));
 
   CloseHandle(hFile); 
 
   return TRUE;
}
```



Ниже приведены выходные данные, которые отображаются при запуске этого примера с сервером слота, показанным при [чтении из слота сообщений](reading-from-a-mailslot.md).

``` syntax
Slot written to successfully.
Slot written to successfully.
Slot written to successfully.
```

 

 
