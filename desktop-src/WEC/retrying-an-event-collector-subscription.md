---
title: Повторная попытка подписки сборщика событий
description: Если проблема возникает с источником событий, связанным с подпиской сборщика событий, можно повторно выполнить подписку после устранения проблемы.
ms.assetid: 8a3570af-bde3-40e5-8129-84ec313d853f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0f29d485d36bb6f623cb67bd3e8598c4bb46b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777732"
---
# <a name="retrying-an-event-collector-subscription"></a>Повторная попытка подписки сборщика событий

Если проблема возникает с источником событий, связанным с подпиской сборщика событий, можно повторно выполнить подписку после устранения проблемы.

> [!Note]
>
> Этот пример можно использовать для повторного выполнения подписки. в командной строке можно ввести следующую команду:
>
> **wecutil RS** *SubscriptionName*

 

Чтобы повторить попытку, потребуется имя подписки. Чтобы вывести список имен текущих подписок на локальном компьютере, можно использовать пример кода C++, показанный в [списке подписок сборщика событий](listing-event-collector-subscriptions.md), или ввести в командной строке следующую команду:

**wecutil ES**

> [!Note]  
> В этом примере показано, как по отдельности повторять каждый источник событий инициированной сборщиком подписки и как повторить попытку, инициированную источником.

 

В следующем примере кода следует процедура повторного выполнения всех источников событий подписки сборщика событий.

**Повторная попытка подписки сборщика событий**

1.  Откройте подписку, указав имя подписки и права доступа в качестве параметров функции [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) . Дополнительные сведения о правах доступа см. в разделе [**константы сборщика событий Windows**](windows-event-collector-constants.md).
2.  Повторите источник события, вызвав функцию **екретрисубскриптион** .
3.  Закройте подписку, вызвав функцию [**екклосе**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .

В следующем примере кода C++ показано, как повторить попытку подписки сборщика событий.


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetStatus(LPCWSTR subscriptionName, 
    LPCWSTR eventSource, 
    EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID statusInfoID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vStatus);


void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwRetVal, dwEventSourceCount;
    EC_HANDLE hSubscription;
    PEC_VARIANT vProperty, vEventSources;
    std::vector<BYTE> buffer, eventSourceBuffer;
    LPCWSTR lpSubname = L"SourceInit";

    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS,
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Determine if the subscription is source initiated or
    // collector initiated.
    dwRetVal = GetProperty(hSubscription,
        EcSubscriptionType,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal){
        goto Cleanup;
    }

    if( vProperty->Type != EcVarTypeNull && vProperty->Type != EcVarTypeUInt32)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if( vProperty->UInt32Val == EcSubscriptionTypeSourceInitiated)
    {
        // Retry the subscription (event source parameter is NULL,
        // so the entire subscription is retried).
        if (!EcRetrySubscription(lpSubname, NULL, 0))
            {
                dwRetVal =  GetLastError();
                goto Cleanup;
            }
        wprintf(L"\nThe subscription was retried.\n");
    }
    else if ( vProperty->UInt32Val == EcSubscriptionTypeCollectorInitiated)
    {
        // Get the event sources array to retry each event source.
        dwRetVal = GetStatus(lpSubname, NULL,
            EcSubscriptionRunTimeStatusEventSources,
            0,
            eventSourceBuffer,
            vEventSources);
        if (ERROR_SUCCESS != dwRetVal){
            goto Cleanup;
        }

        // Ensure that a handle to the event sources array has been obtained.
        if (vEventSources->Type != EcVarTypeNull && 
            vEventSources->Type != (EcVarTypeString | EC_VARIANT_TYPE_ARRAY) )
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }

        dwEventSourceCount = vEventSources->Count;
        
        for (DWORD I = 0; I < dwEventSourceCount ; I++)
        {
            LPCWSTR eventSource = vEventSources->StringArr[I];

            if (!eventSource)
                continue;

            // Retry the event source.
            if (!EcRetrySubscription(lpSubname, eventSource, 0))
            {
                dwRetVal =  GetLastError();
                goto Cleanup;
            }
            
        }
        wprintf(L"\nEach event source was retried.\n");
    }

    Cleanup:
        // Step 5: Close the subscription.
        if(hSubscription)
            EcClose(hSubscription);
        if (dwRetVal != ERROR_SUCCESS)
        {
            FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
                NULL,
                dwRetVal,
                0,
                (LPWSTR) &lpwszBuffer,
                0,
                NULL);
            
            if (!lpwszBuffer)
            {
                wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." \
                    L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
                return;
            }

            wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n" \
                L"Error Message: %s\n", dwRetVal, lpwszBuffer);

            LocalFree(lpwszBuffer);
        }
}

DWORD GetProperty(EC_HANDLE hSubscription,
    EC_SUBSCRIPTION_PROPERTY_ID propID,
    DWORD flags,
    std::vector<BYTE>& buffer,
    PEC_VARIANT& vProperty)
{
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hSubscription)
        return ERROR_INVALID_PARAMETER;

    // Get the value for the specified property. 
    if (!EcGetSubscriptionProperty(hSubscription,
        propID,
        flags, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0], 
        &dwBufferSize))
    {
        dwRetVal = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetSubscriptionProperty(hSubscription,
                propID,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}

// Get the information for the specified EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
DWORD GetStatus(LPCWSTR subscriptionName, 
    LPCWSTR eventSource, 
    EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID statusInfoID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vStatus)
{
    DWORD dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.clear();
    buffer.resize(sizeof(EC_VARIANT));
    
    if ( !EcGetSubscriptionRunTimeStatus( subscriptionName,
        statusInfoID,
        eventSource,
        flags,
        (DWORD) buffer.size(),
        (PEC_VARIANT) &buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if( ERROR_INSUFFICIENT_BUFFER ==  dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);
            if(!EcGetSubscriptionRunTimeStatus( subscriptionName,
                statusInfoID,
                eventSource,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT) &buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if ( ERROR_SUCCESS == dwRetVal)
    {
        vStatus = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vStatus = NULL;
    }

    return dwRetVal;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Список подписок сборщика событий](listing-event-collector-subscriptions.md)
</dt> <dt>

[Справочник по сборщикам событий Windows](windows-event-collector-reference.md)
</dt> </dl>

 

 




