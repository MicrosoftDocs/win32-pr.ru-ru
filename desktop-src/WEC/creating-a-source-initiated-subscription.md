---
title: Создание подписки, инициированной источником
description: Подписки, инициированные источником, позволяют определить подписку на компьютере сборщика событий, не определяя исходные компьютеры событий, а затем можно настроить несколько удаленных компьютеров источника событий (с помощью параметра групповой политики) для перенаправления событий на компьютер сборщика событий. Прежде чем локальный компьютер сможет подписаться на события, а удаленный компьютер может пересылать события, оба компьютера должны быть настроены для сбора событий и пересылки событий. Дополнительные сведения о настройке компьютеров см. в разделе Настройка инициированной источником подписки.
ms.assetid: 489d3613-177f-4045-a055-2c1577ef2191
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0e6d4aa7c94afcdbe6458c2c23c214d935db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792925"
---
# <a name="creating-a-source-initiated-subscription"></a><span data-ttu-id="98579-105">Создание подписки, инициированной источником</span><span class="sxs-lookup"><span data-stu-id="98579-105">Creating a Source Initiated Subscription</span></span>

<span data-ttu-id="98579-106">Подписки, инициированные источником, позволяют определить подписку на компьютере сборщика событий, не определяя исходные компьютеры событий, а затем можно настроить несколько удаленных компьютеров источника событий (с помощью параметра групповой политики) для перенаправления событий на компьютер сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="98579-106">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="98579-107">Прежде чем локальный компьютер сможет подписаться на события, а удаленный компьютер может пересылать события, оба компьютера должны быть настроены для сбора событий и пересылки событий.</span><span class="sxs-lookup"><span data-stu-id="98579-107">Before a local computer can subscribe to events and a remote computer can forward events, both computers must be set up for event collecting and event forwarding.</span></span> <span data-ttu-id="98579-108">Дополнительные сведения о настройке компьютеров см. в разделе [Настройка инициированной источником подписки](setting-up-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="98579-108">For more information about how to configure the computers, see [Setting up a Source Initiated Subscription](setting-up-a-source-initiated-subscription.md).</span></span>

<span data-ttu-id="98579-109">В следующем примере кода используется последовательность действий для создания исходной инициированной подписки, в которой источники событий находятся в том же домене, что и компьютер сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="98579-109">The following code example follows a series of steps to create a source initiated subscription where the event sources are in the same domain as the event collector computer.</span></span>

<span data-ttu-id="98579-110">**Программное создание подписки, инициированной исходным кодом**</span><span class="sxs-lookup"><span data-stu-id="98579-110">**To programmatically create a source-initiated subscription**</span></span>

1.  <span data-ttu-id="98579-111">Откройте подписку, указав имя подписки и права доступа в качестве параметров функции [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="98579-111">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="98579-112">Дополнительные сведения о правах доступа см. в разделе [**константы сборщика событий Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="98579-112">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="98579-113">Задайте свойства подписки, вызвав функцию [**ексетсубскриптионпроперти**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="98579-113">Set the properties of the subscription by calling the [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) function.</span></span> <span data-ttu-id="98579-114">Дополнительные сведения о свойствах подписки, которые можно задать, см. в разделе Перечисление [**\_ \_ \_ идентификаторов свойств подписки EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="98579-114">For more information about subscription properties that can be set, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="98579-115">Сохраните подписку, вызвав функцию [**ексавесубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="98579-115">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
4.  <span data-ttu-id="98579-116">Закройте подписку, вызвав функцию [**екклосе**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="98579-116">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="98579-117">В следующем примере C++ показано, как создать исходную подписку.</span><span class="sxs-lookup"><span data-stu-id="98579-117">The following C++ example shows how to create a source initiated subscription:</span></span>


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <string>
#include <xstring>
#include <conio.h>
#include <EvColl.h>
#include <vector>
#include <wincred.h>
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "wecapi.lib")

// Track properties of the Subscription.
typedef struct _SUBSCRIPTION_SOURCE_INITIATED
{
    std::wstring Name;
    EC_SUBSCRIPTION_TYPE SubscriptionType;
    std::wstring Description;
    BOOL SubscriptionStatus;
    std::wstring URI;
    EC_SUBSCRIPTION_CONFIGURATION_MODE ConfigMode;
    EC_SUBSCRIPTION_DELIVERY_MODE DeliveryMode;
    DWORD MaxItems;
    DWORD MaxLatencyTime;
    DWORD HeartbeatInerval;
    time_t Expires;
    std::wstring Query;
    BOOL ReadExistingEvents;
    std::wstring TransportName;
    EC_SUBSCRIPTION_CONTENT_FORMAT ContentFormat;
    std::wstring DestinationLog;
    std::wstring AllowedSourceNonDomainComputers;
    std::wstring AllowedSourceDomainComputers;

} SUBSCRIPTION_SOURCE_INITIATED;

// Subscription Information
DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);


void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwRetVal = ERROR_SUCCESS;
    EC_HANDLE hSubscription;
    EC_VARIANT vPropertyValue;
    std::vector<BYTE> buffer;
    PEC_VARIANT vProperty = NULL;
    SUBSCRIPTION_SOURCE_INITIATED sub;

    sub.Name = L"TestSubscription-SourceInitiated";
    sub.SubscriptionType = EcSubscriptionTypeSourceInitiated;
    sub.Description = L"A subscription that collects events that are published in\n" \
        L"the Microsoft-Windows-TaskScheduler/Operational log and forwards them \n" \
        L"to the ForwardedEvents log.";
    sub.URI = L"http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog";
    sub.Query = L"<QueryList>" \
        L"<Query Path=\"Microsoft-Windows-TaskScheduler/Operational\">" \
        L"<Select>*</Select>" \
        L"</Query>" \
        L"</QueryList>";
    sub.DestinationLog = L"ForwardedEvents";
    sub.ConfigMode = EcConfigurationModeCustom;
    sub.MaxItems = 5;
    sub.MaxLatencyTime = 1000;
    sub.HeartbeatInerval = 60000;
    sub.DeliveryMode = EcDeliveryModePush;
    sub.ContentFormat = EcContentFormatRenderedText;
    sub.ReadExistingEvents = true;
    sub.SubscriptionStatus = true;
    sub.TransportName = L"http";

    // This SDDL grants members of the Domain Computers domain group as well
    // as members of the Network Service group (for the local forwarder),
    // the ability to raise events for this subscription.
    sub.AllowedSourceDomainComputers = L"O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)";


    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(sub.Name.c_str(),
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_CREATE_NEW);
    if ( !hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Define the subscription properties.
    // Set the subscription type property (collector initiated).
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.SubscriptionType;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionType,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Description property that contains a description
    // of the subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Description.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionDescription,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    // Set the URI property that specifies the URI of all the event sources.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.URI.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionURI,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Query property that defines the query used by the event
    // source to select events that are forwarded to the event collector.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Query.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionQuery,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Log File property that specifies where the forwarded events
    // will be stored.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.DestinationLog.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionLogFile,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the ConfigurationMode property that specifies the mode in which events 
    // are delivered.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ConfigMode;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionConfigurationMode,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // If the Configuration Mode is Custom, set the DeliveryMode, DeliveryMaxItems,
    // HeartbeatInterval, and DeliveryMaxLatencyTime properties.
    if ( sub.ConfigMode == EcConfigurationModeCustom)
    {
        // Set the DeliveryMode property that defines how events are delivered. 
        // Events can be delivered through either a push or pull model.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.DeliveryMode;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMode,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxItems property that specifies the maximum number of 
        // events that can be batched when forwarded from the event sources.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxItems;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxItems,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the HeartbeatInterval property that defines the time interval, in 
        // seconds, that is observed between the heartbeat messages.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.HeartbeatInerval;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionHeartbeatInterval,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxLatencyTime property that specifies how long, in 
        // seconds, the event source should wait before forwarding events.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxLatencyTime;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxLatencyTime,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // Set the ContentFormat property that specifies the format for the event content.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ContentFormat;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionContentFormat,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the ReadExistingEvents property that is used to enable or disable whether
    // existing events are forwarded.
    vPropertyValue.Type = EcVarTypeBoolean;
    vPropertyValue.BooleanVal = sub.ReadExistingEvents;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionReadExistingEvents,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Enabled property that is used to enable or disable the subscription
    // or to obtain the current status of a subscription.
    vPropertyValue.Type = EcVarTypeBoolean;
    vPropertyValue.BooleanVal = sub.SubscriptionStatus;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionEnabled,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the TransportName property that determines the type of 
    // transport used by the subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.TransportName.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionTransportName,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Required:
    // Set the AllowedSourceDomainComputers property to the specified SDDL.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.AllowedSourceDomainComputers.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionAllowedSourceDomainComputers,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    //----------------------------------------------
    // Step 3: Save the subscription.
    // Save the subscription with the associated properties
    // This will create the subscription and store it in the 
    // subscription repository 
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Close the subscription.
Cleanup:
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
            L" Error Message: %s\n", dwRetVal, lpwszBuffer);

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
        &dwBufferSize) )
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
```



<span data-ttu-id="98579-118">**Проверка правильности работы подписки**</span><span class="sxs-lookup"><span data-stu-id="98579-118">**Validate that the subscription works correctly**</span></span>

1.  <span data-ttu-id="98579-119">На компьютере сборщика событий выполните следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="98579-119">On the event collector computer complete the following procedure:</span></span>

    1.  <span data-ttu-id="98579-120">Выполните следующую команду из командной строки с повышенными привилегиями, чтобы получить состояние выполнения подписки:</span><span class="sxs-lookup"><span data-stu-id="98579-120">Run the following command from an elevated privilege command prompt to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="98579-121">\**wecutil GR\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="98579-121">**wecutil gr** *<subscriptionID>*</span></span>

    2.  <span data-ttu-id="98579-122">Убедитесь, что источник событий подключен.</span><span class="sxs-lookup"><span data-stu-id="98579-122">Verify that the event source has connected.</span></span> <span data-ttu-id="98579-123">Возможно, потребуется подождать, пока интервал обновления, указанный в политике, не пойдет после создания подписки для подключения к источнику событий.</span><span class="sxs-lookup"><span data-stu-id="98579-123">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3.  <span data-ttu-id="98579-124">Выполните следующую команду, чтобы получить сведения о подписке:</span><span class="sxs-lookup"><span data-stu-id="98579-124">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="98579-125">\**wecutil GS\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="98579-125">**wecutil gs** *<subscriptionID>*</span></span>

    4.  <span data-ttu-id="98579-126">Получите значение Деливеримакситемс из сведений о подписке.</span><span class="sxs-lookup"><span data-stu-id="98579-126">Get the DeliveryMaxItems value from the subscription information.</span></span>

2.  <span data-ttu-id="98579-127">На компьютере источника событий создайте события, которые соответствуют запросу, из подписки на события.</span><span class="sxs-lookup"><span data-stu-id="98579-127">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="98579-128">Деливеримакситемс число событий должно быть сгенерировано для перенаправляемых событий.</span><span class="sxs-lookup"><span data-stu-id="98579-128">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3.  <span data-ttu-id="98579-129">На компьютере сборщика событий проверьте, что события были перенаправлены в журнал ForwardedEvents или в журнал, указанный в подписке.</span><span class="sxs-lookup"><span data-stu-id="98579-129">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98579-130">См. также</span><span class="sxs-lookup"><span data-stu-id="98579-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="98579-131">[Настройка компьютеров на пересылку и получение событий](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="98579-131">[Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="98579-132">Настройка исходной подписки, инициированной источником</span><span class="sxs-lookup"><span data-stu-id="98579-132">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)
</dt> <dt>

[<span data-ttu-id="98579-133">Справочник по сборщикам событий Windows</span><span class="sxs-lookup"><span data-stu-id="98579-133">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 