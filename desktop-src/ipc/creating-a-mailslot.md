---
description: 'Как создать маилслотс. Маилслотс поддерживаются тремя специализированными функциями: Креатемаилслот, Жетмаилслотинфо и Сетмаилслотинфо. Эти функции используются сервером слота.'
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: Создание слота сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4cfbcf990162347d1e45da01c815002f39299e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684426"
---
# <a name="creating-a-mailslot"></a><span data-ttu-id="b1aa9-105">Создание слота сообщений</span><span class="sxs-lookup"><span data-stu-id="b1aa9-105">Creating a Mailslot</span></span>

<span data-ttu-id="b1aa9-106">Маилслотс поддерживаются тремя специализированными функциями: [**креатемаилслот**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**жетмаилслотинфо**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)и [**сетмаилслотинфо**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo).</span><span class="sxs-lookup"><span data-stu-id="b1aa9-106">Mailslots are supported by three specialized functions: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo), and [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo).</span></span> <span data-ttu-id="b1aa9-107">Эти функции используются сервером слота.</span><span class="sxs-lookup"><span data-stu-id="b1aa9-107">These functions are used by the mailslot server.</span></span>

<span data-ttu-id="b1aa9-108">В следующем примере кода функция [**креатемаилслот**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) используется для получения маркера в почтовый слот с именем "Sample \_ почтовый слот".</span><span class="sxs-lookup"><span data-stu-id="b1aa9-108">The following code sample uses the [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) function to retrieve the handle to a mailslot named "sample\_mailslot".</span></span> <span data-ttu-id="b1aa9-109">Пример кода в [записи в почтовый слот](writing-to-a-mailslot.md) показывает, как клиентское приложение может выполнять запись в этот почтовый слот.</span><span class="sxs-lookup"><span data-stu-id="b1aa9-109">The code sample in [Writing to a Mailslot](writing-to-a-mailslot.md) shows how client application can write to this mailslot.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

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
    else printf("Mailslot created successfully.\n"); 
    return TRUE; 
}

void main()
{ 
   MakeSlot(SlotName);
}
```



<span data-ttu-id="b1aa9-110">Чтобы создать почтовый слот, который может наследоваться дочерними процессами, приложение должно изменить структуру [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , переданную в качестве последнего параметра [**креатемаилслот**](/windows/desktop/api/Winbase/nf-winbase-createmailslota).</span><span class="sxs-lookup"><span data-stu-id="b1aa9-110">To create a mailslot that can be inherited by child processes, an application should change the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure passed as the last parameter of [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota).</span></span> <span data-ttu-id="b1aa9-111">Для этого приложение устанавливает для элемента **бинхерисандле** этой структуры **значение true** (значение по умолчанию — **false**).</span><span class="sxs-lookup"><span data-stu-id="b1aa9-111">To do this, the application sets the **bInheritHandle** member of this structure to **TRUE** (the default setting is **FALSE**).</span></span>

 

 
