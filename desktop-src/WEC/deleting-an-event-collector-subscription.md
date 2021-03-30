---
title: Удаление подписки сборщика событий
description: Вы можете удалить подписку сборщика событий с локального компьютера.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cec036625bbb94e33e71af0f1d9808ad9252a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775668"
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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Список подписок сборщика событий](listing-event-collector-subscriptions.md)
</dt> <dt>

[Справочник по сборщикам событий Windows](windows-event-collector-reference.md)
</dt> </dl>

 

 




