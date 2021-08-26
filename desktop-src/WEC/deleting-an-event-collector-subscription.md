---
title: Удаление подписки сборщика событий
description: Вы можете удалить подписку сборщика событий с локального компьютера.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9edf2f9dda2b6393ab147d5f58ff8f889952eaeb7f31f82080558697f117f3c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006094"
---
# <a name="deleting-an-event-collector-subscription"></a>Удаление подписки сборщика событий

Вы можете удалить подписку сборщика событий с локального компьютера. Необходимо указать имя подписки, прежде чем ее можно будет удалить. Дополнительные сведения о том, как вывести список текущих подписок на локальном компьютере, см. в разделе список [подписок сборщика событий](listing-event-collector-subscriptions.md)или введите в командной строке следующую команду:

**wecutil ES**

> [!Note]
>
> С помощью этого примера можно удалить подписку сборщика событий или ввести в командной строке следующую команду:
>
> **wecutil DS** *SubscriptionName*

 

После получения имени подписки сборщика событий для удаления можно указать имя подписки в качестве параметра для [**екделетесубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).

В следующем примере кода C++ показано, как удалить подписку сборщика событий.


```C++
#include <windows.h>
#include <EvColl.h>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    DWORD dwRetVal;
    LPWSTR lpSubname = L"MyTestSubscription";

    // Delete the specified Event Collector subscription.
    if (!EcDeleteSubscription(lpSubname, 0))
    {
        dwRetVal = GetLastError();
        LPVOID lpwszBuffer;

        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);

        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." 
                L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n"
            L"Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Список подписок сборщика событий](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows Справочник по сборщикам событий](windows-event-collector-reference.md)
</dt> </dl>

 

 




