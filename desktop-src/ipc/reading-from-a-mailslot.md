---
description: Чтение из слота сообщений. Процесс, создающий почтовый слот, может считывать сообщения из него с помощью обработчика слота при вызове функции ReadFile.
ms.assetid: e193dca9-3b77-4e41-be6d-90992e1a8fe3
title: Чтение из слота сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35458f90ca381689275417e0e525c2d5a31ac9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692119"
---
# <a name="reading-from-a-mailslot"></a><span data-ttu-id="7ad0d-104">Чтение из слота сообщений</span><span class="sxs-lookup"><span data-stu-id="7ad0d-104">Reading from a Mailslot</span></span>

<span data-ttu-id="7ad0d-105">Процесс, создающий почтовый слот, может считывать сообщения из него с помощью обработчика слота при вызове функции [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) .</span><span class="sxs-lookup"><span data-stu-id="7ad0d-105">The process that creates a mailslot can read messages from it by using the mailslot handle in a call to the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function.</span></span> <span data-ttu-id="7ad0d-106">В следующем примере вызывается функция [**жетмаилслотинфо**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) для определения наличия сообщений в почтовом слоте.</span><span class="sxs-lookup"><span data-stu-id="7ad0d-106">The following example calls the [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) function to determine whether there are messages in the mailslot.</span></span> <span data-ttu-id="7ad0d-107">Если сообщения ожидают, каждое из них отображается вместе с количеством оставшихся сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ad0d-107">If messages are waiting, each is displayed along with the number of messages remaining to be read.</span></span>

<span data-ttu-id="7ad0d-108">Почтовый слот существует до вызова функции [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) для всех открытых дескрипторов сервера или до момента выхода всех серверных процессов, владеющих дескриптором слота.</span><span class="sxs-lookup"><span data-stu-id="7ad0d-108">A mailslot exists until the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function is called for all open server handles or until all server processes that own a mailslot handle exit.</span></span> <span data-ttu-id="7ad0d-109">В обоих случаях все непрочитанные сообщения удаляются из слота, все дескрипторы клиента в почтовый слот закрываются, а сам почтовый слот удаляется из памяти.</span><span class="sxs-lookup"><span data-stu-id="7ad0d-109">In both cases, any unread messages are deleted from the mailslot, all client handles to the mailslot are closed, and the mailslot itself is deleted from memory.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL ReadSlot() 
{ 
    DWORD cbMessage, cMessage, cbRead; 
    BOOL fResult; 
    LPTSTR lpszBuffer; 
    TCHAR achID[80]; 
    DWORD cAllMessages; 
    HANDLE hEvent;
    OVERLAPPED ov;
 
    cbMessage = cMessage = cbRead = 0; 

    hEvent = CreateEvent(NULL, FALSE, FALSE, TEXT("ExampleSlot"));
    if( NULL == hEvent )
        return FALSE;
    ov.Offset = 0;
    ov.OffsetHigh = 0;
    ov.hEvent = hEvent;
 
    fResult = GetMailslotInfo( hSlot, // mailslot handle 
        (LPDWORD) NULL,               // no maximum message size 
        &cbMessage,                   // size of next message 
        &cMessage,                    // number of messages 
        (LPDWORD) NULL);              // no read time-out 
 
    if (!fResult) 
    { 
        printf("GetMailslotInfo failed with %d.\n", GetLastError()); 
        return FALSE; 
    } 
 
    if (cbMessage == MAILSLOT_NO_MESSAGE) 
    { 
        printf("Waiting for a message...\n"); 
        return TRUE; 
    } 
 
    cAllMessages = cMessage; 
 
    while (cMessage != 0)  // retrieve all messages
    { 
        // Create a message-number string. 
 
        StringCchPrintf((LPTSTR) achID, 
            80,
            TEXT("\nMessage #%d of %d\n"), 
            cAllMessages - cMessage + 1, 
            cAllMessages); 

        // Allocate memory for the message. 
 
        lpszBuffer = (LPTSTR) GlobalAlloc(GPTR, 
            lstrlen((LPTSTR) achID)*sizeof(TCHAR) + cbMessage); 
        if( NULL == lpszBuffer )
            return FALSE;
        lpszBuffer[0] = '\0'; 
 
        fResult = ReadFile(hSlot, 
            lpszBuffer, 
            cbMessage, 
            &cbRead, 
            &ov); 
 
        if (!fResult) 
        { 
            printf("ReadFile failed with %d.\n", GetLastError()); 
            GlobalFree((HGLOBAL) lpszBuffer); 
            return FALSE; 
        } 
 
        // Concatenate the message and the message-number string. 
 
        StringCbCat(lpszBuffer, 
                    lstrlen((LPTSTR) achID)*sizeof(TCHAR)+cbMessage, 
                    (LPTSTR) achID); 
 
        // Display the message. 
 
        _tprintf(TEXT("Contents of the mailslot: %s\n"), lpszBuffer); 
 
        GlobalFree((HGLOBAL) lpszBuffer); 
 
        fResult = GetMailslotInfo(hSlot,  // mailslot handle 
            (LPDWORD) NULL,               // no maximum message size 
            &cbMessage,                   // size of next message 
            &cMessage,                    // number of messages 
            (LPDWORD) NULL);              // no read time-out 
 
        if (!fResult) 
        { 
            printf("GetMailslotInfo failed (%d)\n", GetLastError());
            return FALSE; 
        } 
    } 
    CloseHandle(hEvent);
    return TRUE; 
}

BOOL WINAPI MakeSlot(LPCTSTR lpszSlotName) 
{ 
    hSlot = CreateMailslot(lpszSlotName, 
        0,                             // no maximum message size 
        MAILSLOT_WAIT_FOREVER,         // no time-out for operations 
        (LPSECURITY_ATTRIBUTES) NULL); // default security
 
    if (hSlot == INVALID_HANDLE_VALUE) 
    { 
        printf("CreateMailslot failed with %d\n", GetLastError());
        return FALSE; 
    } 
    return TRUE; 
}

void main()
{
   MakeSlot(SlotName);

   while(TRUE)
   {
      ReadSlot();
      Sleep(3000);
   }
}
```



<span data-ttu-id="7ad0d-110">Ниже приведены выходные данные, которые отображаются при выполнении этого примера с клиентом слота, отображаемым при [записи в почтовый слот](writing-to-a-mailslot.md).</span><span class="sxs-lookup"><span data-stu-id="7ad0d-110">The following is the output that is displayed when this example is run with the mailslot client shown in [Writing to a Mailslot](writing-to-a-mailslot.md).</span></span>

``` syntax
Waiting for a message...
Waiting for a message...
Contents of the mailslot: Message one for mailslot.
Message #1 of 2

Contents of the mailslot: Message two for mailslot.
Message #2 of 2

Waiting for a message...
Contents of the mailslot: Message three for mailslot.
Message #1 of 1

Waiting for a message...
Waiting for a message...
Waiting for a message...
^C
```

 

 
