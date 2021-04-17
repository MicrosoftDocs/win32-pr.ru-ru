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
# <a name="creating-a-mailslot"></a>Создание слота сообщений

Маилслотс поддерживаются тремя специализированными функциями: [**креатемаилслот**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**жетмаилслотинфо**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)и [**сетмаилслотинфо**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo). Эти функции используются сервером слота.

В следующем примере кода функция [**креатемаилслот**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) используется для получения маркера в почтовый слот с именем "Sample \_ почтовый слот". Пример кода в [записи в почтовый слот](writing-to-a-mailslot.md) показывает, как клиентское приложение может выполнять запись в этот почтовый слот.


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



Чтобы создать почтовый слот, который может наследоваться дочерними процессами, приложение должно изменить структуру [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , переданную в качестве последнего параметра [**креатемаилслот**](/windows/desktop/api/Winbase/nf-winbase-createmailslota). Для этого приложение устанавливает для элемента **бинхерисандле** этой структуры **значение true** (значение по умолчанию — **false**).

 

 
