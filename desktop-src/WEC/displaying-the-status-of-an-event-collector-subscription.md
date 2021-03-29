---
title: Отображение состояния подписки сборщика событий
description: Можно отобразить состояние подписки сборщика событий. Состояние включает доступность подписки, последнюю ошибку, возникшую для подписки, время последней ошибки и следующий раз, когда подписка будет повторно выполнена.
ms.assetid: e1c3c3ed-2f7c-433d-a51d-66c2abd2e961
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7c806d72d4945e2e45384b91bc94fbef3ed08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329736"
---
# <a name="displaying-the-status-of-an-event-collector-subscription"></a><span data-ttu-id="54b8d-104">Отображение состояния подписки сборщика событий</span><span class="sxs-lookup"><span data-stu-id="54b8d-104">Displaying the Status of an Event Collector Subscription</span></span>

<span data-ttu-id="54b8d-105">Можно отобразить состояние подписки сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="54b8d-105">You can display the status of an Event Collector subscription.</span></span> <span data-ttu-id="54b8d-106">Состояние включает доступность подписки, последнюю ошибку, возникшую для подписки, время последней ошибки и следующий раз, когда подписка будет повторно выполнена.</span><span class="sxs-lookup"><span data-stu-id="54b8d-106">The status includes the availability of the subscription, the last error that occurred for the subscription, the time of the last error, and the next time the subscription will be retried.</span></span>

> [!Note]
>
> <span data-ttu-id="54b8d-107">С помощью этого примера можно отобразить состояние подписки или ввести в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54b8d-107">You can use this example to display the status of a subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="54b8d-108">**wecutil GR** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="54b8d-108">**wecutil gr** *SubscriptionName*</span></span>

 

<span data-ttu-id="54b8d-109">Вам потребуется имя подписки, чтобы отобразить ее состояние.</span><span class="sxs-lookup"><span data-stu-id="54b8d-109">You will need the name of a subscription to display its status.</span></span> <span data-ttu-id="54b8d-110">Чтобы вывести список имен текущих подписок на локальном компьютере, можно использовать пример C++ в списке [подписок сборщика событий](listing-event-collector-subscriptions.md)или ввести в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54b8d-110">To list the names of current subscriptions on a local computer, you can use the C++ example in shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="54b8d-111">**wecutil ES**</span><span class="sxs-lookup"><span data-stu-id="54b8d-111">**wecutil es**</span></span>

<span data-ttu-id="54b8d-112">Ниже приведен пример процедуры для просмотра состояния подписки сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="54b8d-112">The following example follows a procedure to display the status of an Event Collector subscription:</span></span>

<span data-ttu-id="54b8d-113">**Отображение состояния подписки сборщика событий**</span><span class="sxs-lookup"><span data-stu-id="54b8d-113">**To display the status of an Event Collector subscription**</span></span>

1.  <span data-ttu-id="54b8d-114">Откройте подписку, указав имя подписки и права доступа в качестве параметров функции [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="54b8d-114">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="54b8d-115">Дополнительные сведения о правах доступа см. в разделе [**константы сборщика событий Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="54b8d-115">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="54b8d-116">Получите состояние подписки, вызвав функцию [**екжетсубскриптионрунтиместатус**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) (не указывайте источник события при вызове функции).</span><span class="sxs-lookup"><span data-stu-id="54b8d-116">Get the status of the subscription by calling the [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) function (do not specify an event source when calling the function).</span></span>
3.  <span data-ttu-id="54b8d-117">Получите массив источников событий подписки, вызвав функцию [**екжетсубскриптионрунтиместатус**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) и передав флаг ексубскриптионрунтиместатусевентсаурцес.</span><span class="sxs-lookup"><span data-stu-id="54b8d-117">Get the event sources array of the subscription by calling the [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) function and passing in the EcSubscriptionRunTimeStatusEventSources flag.</span></span>
4.  <span data-ttu-id="54b8d-118">Получите сведения о состоянии для каждого источника события, вызвав функцию [**екжетсубскриптионрунтиместатус**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) и передав имя источника события.</span><span class="sxs-lookup"><span data-stu-id="54b8d-118">Get the status information for each event source by calling the [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) function and passing in the event source name.</span></span> <span data-ttu-id="54b8d-119">Дополнительные сведения о состоянии, которое можно получить, см. в разделе Перечисление [**\_ \_ \_ \_ \_ ИД сведений о состоянии среды выполнения подписки EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id) .</span><span class="sxs-lookup"><span data-stu-id="54b8d-119">For more information about the status information that can be retrieved, see the [**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_INFO\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id) enumeration.</span></span>
5.  <span data-ttu-id="54b8d-120">Печать сведений о состоянии подписки.</span><span class="sxs-lookup"><span data-stu-id="54b8d-120">Print the status information for the subscription.</span></span>
6.  <span data-ttu-id="54b8d-121">Закройте подписку, вызвав функцию [**екклосе**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="54b8d-121">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="54b8d-122">В следующем примере кода C++ показано, как отобразить состояние подписки сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="54b8d-122">The following C++ code example shows how to display the status of an Event Collector subscription.</span></span>


```C++
#include <iostream>
using namespace std;
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Track Runtime Status
typedef struct _RUNTIME_STATUS
{
    std::wstring ActiveStatus;
    DWORD LastError;
    std::wstring LastErrorMessage;
    std::wstring NextRetryTime;

} RUNTIME_STATUS;

// Subscription Information

DWORD GetStatus(LPCWSTR subscriptionName, 
    LPCWSTR eventSource, 
    EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID statusInfoID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vStatus);

std::wstring ConvertEcDateTime( ULONGLONG code );



void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwEventSourceCount, dwRetVal = ERROR_SUCCESS;
    std::vector<BYTE> buffer;
    std::vector<BYTE> eventSourceBuffer;
    std::vector<BYTE>::iterator sourceNameIterator;
    PEC_VARIANT vStatus, vEventSources;
    EC_HANDLE hSubscription;
    LPCWSTR lpSubname = L"TestSubscription";
    RUNTIME_STATUS runtimeStatus;
    std::wstring eventSource;

    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(lpSubname, 
        EC_READ_ACCESS, 
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the status values for the entire subscription.
    dwRetVal = GetStatus(lpSubname, NULL, 
        EcSubscriptionRunTimeStatusActive,
        0,
        buffer,
        vStatus);
    if (ERROR_SUCCESS != dwRetVal) {
        goto Cleanup;
    }
    wprintf(L"\nEvent Subscription: %s\n",  lpSubname);
    
    // Convert the status value to text.
    switch (vStatus->UInt32Val)
    {
        case EcRuntimeStatusActiveStatusActive:
            runtimeStatus.ActiveStatus = L"Active";
            break;
        case EcRuntimeStatusActiveStatusDisabled:
            runtimeStatus.ActiveStatus = L"Disabled";
            break;
        case EcRuntimeStatusActiveStatusInactive:
            runtimeStatus.ActiveStatus = L"Inactive";
            break;
        case EcRuntimeStatusActiveStatusTrying:
            runtimeStatus.ActiveStatus = L"Trying";
            break;
        default:
            runtimeStatus.ActiveStatus = L"Unknown Status";
        break;
    }
    wprintf(L"Runtime Status: %s\n", runtimeStatus.ActiveStatus.c_str());
    
    dwRetVal = GetStatus(lpSubname, NULL, 
        EcSubscriptionRunTimeStatusLastError,
        0,
        buffer,
        vStatus);
    if (ERROR_SUCCESS != dwRetVal) {
        goto Cleanup;
    }
    wprintf(L"Last Error: %u\n", vStatus->UInt32Val);
        
    

    // Step 2: Get the event sources array to query for event source status.
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
    
    // Step 3: Get the status of each event source.
    for (DWORD I = 0; I < dwEventSourceCount ; I++)
    {
        eventSource = vEventSources->StringArr[I];

        // Get the status of the subscription event source.
        dwRetVal = GetStatus(lpSubname, 
            eventSource.c_str(),
            EcSubscriptionRunTimeStatusActive, 
            0, 
            buffer, 
            vStatus);
        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }
        if (vStatus->Type != EcVarTypeUInt32)
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }

        // Convert the status value to text.
        switch (vStatus->UInt32Val)
        {
            case EcRuntimeStatusActiveStatusActive:
                runtimeStatus.ActiveStatus = L"Active";
                break;
            case EcRuntimeStatusActiveStatusDisabled:
                runtimeStatus.ActiveStatus = L"Disabled";
                break;
            case EcRuntimeStatusActiveStatusInactive:
                runtimeStatus.ActiveStatus = L"Inactive";
                break;
            case EcRuntimeStatusActiveStatusTrying:
                runtimeStatus.ActiveStatus = L"Trying";
                break;
            default:
                runtimeStatus.ActiveStatus = L"Unknown Status";
            break;
        }

        // Get the last error that occurred for the subscription.
        dwRetVal = GetStatus(lpSubname, 
            eventSource.c_str(), 
            EcSubscriptionRunTimeStatusLastError, 
            0, 
            buffer, 
            vStatus);
        if(ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }
        if (vStatus->Type != EcVarTypeUInt32)
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }
        
        runtimeStatus.LastError = vStatus->UInt32Val;

        // Get the error message for the last error.
        dwRetVal = GetStatus(lpSubname, 
            eventSource.c_str(), 
            EcSubscriptionRunTimeStatusLastErrorMessage, 
            0, 
            buffer, 
            vStatus);

        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }
        if (vStatus->Type != EcVarTypeNull && vStatus->Type != EcVarTypeString)
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }
          
        if (vStatus->Type != EcVarTypeNull)
        {
            runtimeStatus.LastErrorMessage = vStatus->StringVal;
        }
        else
        {
            runtimeStatus.LastErrorMessage = L"";
        }

        // Get the time when the subscription will be retried.
        dwRetVal = GetStatus( lpSubname, 
            eventSource.c_str(), 
            EcSubscriptionRunTimeStatusNextRetryTime, 
            0, 
            buffer, 
            vStatus);

        if( ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }
         
        if (vStatus->Type != EcVarTypeNull && vStatus->Type != EcVarTypeDateTime)
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }
          
        if( vStatus->Type != EcVarTypeNull)
        {
            runtimeStatus.NextRetryTime = ConvertEcDateTime(vStatus->DateTimeVal);
        }
        else
        {
            runtimeStatus.NextRetryTime = L"";
        }

        // Step 4: Print the status information.
        wprintf(L"\nEventSource[%u]\n",  I);
        wprintf(L"    Address: %s\n", eventSource.c_str());
        wprintf(L"    Runtime Status: %s\n", runtimeStatus.ActiveStatus.c_str());
        wprintf(L"    Last Error: %u\n", runtimeStatus.LastError);
         
        if( 0 != runtimeStatus.LastError )
        {
            wprintf(L"    Last Error Message: %s\n", runtimeStatus.LastErrorMessage.c_str());
        }
        else
        {
            wprintf(L"    Last Error Message: No Error\n");
        }
         
        wprintf(L"    Next Retry Time: %s\n", runtimeStatus.NextRetryTime.c_str());
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

std::wstring ConvertEcDateTime( ULONGLONG code )
{
    FILETIME ft;
    SYSTEMTIME utcTime;
    SYSTEMTIME localTime; 
    std::wstring timeString;
    std::vector<WCHAR> buffer(30);

    timeString = L"Error- Failed to Convert Date Time to String";

    ft.dwHighDateTime = (DWORD)((code >> 32) & 0xFFFFFFFF);
    ft.dwLowDateTime = (DWORD)(code & 0xFFFFFFFF);

    if( !FileTimeToSystemTime( &ft, &utcTime) )
    {
        return timeString;
    }

    if(!SystemTimeToTzSpecificLocalTime(NULL, &utcTime, &localTime))
    {
        return timeString;
    }

    HRESULT hr = StringCchPrintfW((LPWSTR) &buffer[0], 
        buffer.size(), 
        L"%4.4hd-%2.2hd-%2.2hdT%2.2hd:%2.2hd:%2.2hd.%3.3hdZ",
        localTime.wYear,
        localTime.wMonth,
        localTime.wDay,
        localTime.wHour,
        localTime.wMinute,
        localTime.wSecond,
        localTime.wMilliseconds);

    if (FAILED(hr)) 
    {
        return timeString;
    }

    timeString = (LPWSTR) &buffer[0];

    return timeString;
}
```



## <a name="related-topics"></a><span data-ttu-id="54b8d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="54b8d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54b8d-124">Список подписок сборщика событий</span><span class="sxs-lookup"><span data-stu-id="54b8d-124">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="54b8d-125">Справочник по сборщикам событий Windows</span><span class="sxs-lookup"><span data-stu-id="54b8d-125">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




