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
# <a name="deleting-an-event-collector-subscription"></a><span data-ttu-id="adfdc-103">Удаление подписки сборщика событий</span><span class="sxs-lookup"><span data-stu-id="adfdc-103">Deleting an Event Collector Subscription</span></span>

<span data-ttu-id="adfdc-104">Вы можете удалить подписку сборщика событий с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="adfdc-104">You can delete an Event Collector subscription from a local computer.</span></span> <span data-ttu-id="adfdc-105">Необходимо указать имя подписки, прежде чем ее можно будет удалить.</span><span class="sxs-lookup"><span data-stu-id="adfdc-105">You must know the name of the subscription before you can delete it.</span></span> <span data-ttu-id="adfdc-106">Дополнительные сведения о том, как вывести список текущих подписок на локальном компьютере, см. в разделе список [подписок сборщика событий](listing-event-collector-subscriptions.md)или введите в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="adfdc-106">For more information about how to list the current subscriptions on a local computer, see [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or type the following command at the command prompt:</span></span>

<span data-ttu-id="adfdc-107">**wecutil ES**</span><span class="sxs-lookup"><span data-stu-id="adfdc-107">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="adfdc-108">С помощью этого примера можно удалить подписку сборщика событий или ввести в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="adfdc-108">You can use this example to delete an Event Collector subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="adfdc-109">**wecutil DS** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="adfdc-109">**wecutil ds** *SubscriptionName*</span></span>

 

<span data-ttu-id="adfdc-110">После получения имени подписки сборщика событий для удаления можно указать имя подписки в качестве параметра для [**екделетесубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span><span class="sxs-lookup"><span data-stu-id="adfdc-110">After you retrieve the name of the Event Collector subscription to delete, you can provide the name of the subscription as a parameter to [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span></span>

<span data-ttu-id="adfdc-111">В следующем примере кода C++ показано, как удалить подписку сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="adfdc-111">The following C++ code example shows how to delete an Event Collector subscription.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="adfdc-112">См. также</span><span class="sxs-lookup"><span data-stu-id="adfdc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adfdc-113">Список подписок сборщика событий</span><span class="sxs-lookup"><span data-stu-id="adfdc-113">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="adfdc-114">Справочник по сборщикам событий Windows</span><span class="sxs-lookup"><span data-stu-id="adfdc-114">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




