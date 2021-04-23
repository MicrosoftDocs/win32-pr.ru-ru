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
# <a name="writing-to-a-mailslot"></a><span data-ttu-id="5f4e6-104">Запись в почтовый слот</span><span class="sxs-lookup"><span data-stu-id="5f4e6-104">Writing to a Mailslot</span></span>

<span data-ttu-id="5f4e6-105">Запись в почтовый слот аналогична записи в файл стандартного диска.</span><span class="sxs-lookup"><span data-stu-id="5f4e6-105">Writing to a mailslot is similar to writing to a standard disk file.</span></span> <span data-ttu-id="5f4e6-106">В следующем коде функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)и [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) используются для помещения короткого сообщения в почтовый слот.</span><span class="sxs-lookup"><span data-stu-id="5f4e6-106">The following code uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) functions to put a short message in a mailslot.</span></span> <span data-ttu-id="5f4e6-107">Сообщение передается на сервер слота с именем "образец \_ слота сообщений" на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5f4e6-107">The message is broadcast to the mailslot server named "sample\_mailslot" on the local computer.</span></span> <span data-ttu-id="5f4e6-108">Код работает в соответствии с предположением о том, что сервер слота уже создан.</span><span class="sxs-lookup"><span data-stu-id="5f4e6-108">The code operates under the assumption that the mailslot server was already created.</span></span>


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



<span data-ttu-id="5f4e6-109">Ниже приведены выходные данные, которые отображаются при запуске этого примера с сервером слота, показанным при [чтении из слота сообщений](reading-from-a-mailslot.md).</span><span class="sxs-lookup"><span data-stu-id="5f4e6-109">The following is the output that is displayed when this example is run with the mailslot server shown in [Reading from a Mailslot](reading-from-a-mailslot.md).</span></span>

``` syntax
Slot written to successfully.
Slot written to successfully.
Slot written to successfully.
```

 

 
