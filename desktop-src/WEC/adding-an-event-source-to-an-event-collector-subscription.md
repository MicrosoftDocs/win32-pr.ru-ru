---
title: Добавление источника событий к подписке, инициированной сборщиком
description: Чтобы получить перенаправленное событие из подписки на события, можно создать подписку, инициированную сборщиком на локальном компьютере.
ms.assetid: f0100938-1702-4ef7-b20e-a0e8df224d18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c639b496a00f56a38a0f9f8e72b9d099e58c17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070153"
---
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a><span data-ttu-id="7a6c6-103">Добавление источника событий к подписке, инициированной сборщиком</span><span class="sxs-lookup"><span data-stu-id="7a6c6-103">Adding an Event Source to a Collector Initiated Subscription</span></span>

<span data-ttu-id="7a6c6-104">Чтобы получить перенаправленное событие из подписки на события, можно создать подписку, инициированную сборщиком на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7a6c6-104">To receive a forwarded event from an event subscription, you can create a collector-initiated subscription on the local computer.</span></span> <span data-ttu-id="7a6c6-105">Дополнительные сведения о создании подписки, инициированной сборщиком, см. в примере кода C++, приведенном в разделе [Создание подписки сборщика событий](creating-an-event-collector-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="7a6c6-105">For more information about how to create a collector initiated subscription, see the C++ code example shown in [Creating an Event Collector Subscription](creating-an-event-collector-subscription.md).</span></span>

<span data-ttu-id="7a6c6-106">После создания подписки, инициированной сборщиком, можно добавить источники событий в подписку.</span><span class="sxs-lookup"><span data-stu-id="7a6c6-106">After a collector-initiated subscription has been created, you can add event sources to the subscription.</span></span> <span data-ttu-id="7a6c6-107">Необходимо добавить по крайней мере один источник событий в подписку для получения событий.</span><span class="sxs-lookup"><span data-stu-id="7a6c6-107">You must add at least one event source to a subscription to collect events.</span></span>

> [!Note]
>
> <span data-ttu-id="7a6c6-108">С помощью этого примера кода можно добавить источник события в подписку. в командной строке можно ввести следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7a6c6-108">You can use this code example to add an event source to a subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="7a6c6-109">**wecutil SS** *SubscriptionName*  \* */ЕСА: \* \* \* евентсаурцеаддресс* **/АЕС/ЕСЕ**</span><span class="sxs-lookup"><span data-stu-id="7a6c6-109">**wecutil ss** *SubscriptionName* \**/esa:\*\*\*EventSourceAddress* **/aes /ese**</span></span>
>
> <span data-ttu-id="7a6c6-110">*Евентсаурцеаддресс* может иметь значение localhost для локального компьютера или полное доменное имя удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="7a6c6-110">*EventSourceAddress* can be either localhost for the local computer or a fully qualified domain name for a remote computer.</span></span>

 

<span data-ttu-id="7a6c6-111">Дополнительные сведения о добавлении источников событий к исходной инициированной подписке см. в разделе [Настройка инициированной источником подписки](setting-up-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="7a6c6-111">For more information about how to add event sources to a source initiated subscription, see [Setting up a Source Initiated Subscription](setting-up-a-source-initiated-subscription.md).</span></span>

<span data-ttu-id="7a6c6-112">В этом примере для добавления источника событий в подписку, инициированную сборщиком, следует выполнить ряд действий.</span><span class="sxs-lookup"><span data-stu-id="7a6c6-112">This example follows a series of steps to add an event source to a collector initiated subscription.</span></span>

<span data-ttu-id="7a6c6-113">**Добавление источника событий к подписке, инициированной сборщиком**</span><span class="sxs-lookup"><span data-stu-id="7a6c6-113">**To add an event source to a collector initiated subscription**</span></span>

1.  <span data-ttu-id="7a6c6-114">Откройте существующую подписку, указав имя подписки и права доступа в качестве параметров функции [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="7a6c6-114">Open the existing subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="7a6c6-115">Дополнительные сведения о правах доступа см. в разделе [**константы сборщика событий Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7a6c6-115">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="7a6c6-116">Получите массив источников событий подписки, вызвав функцию [**екжетсубскриптионпроперти**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="7a6c6-116">Get the event sources array of the subscription by calling the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) function.</span></span> <span data-ttu-id="7a6c6-117">Дополнительные сведения о свойствах подписки, которые можно получить, см. в разделе Перечисление [**\_ \_ \_ идентификаторов свойств подписки EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="7a6c6-117">For more information about subscription properties that can be retrieved, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="7a6c6-118">Добавьте новый источник событий в массив источников событий подписки, вызвав функцию [**еЦинсертобжектаррайелемент**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) .</span><span class="sxs-lookup"><span data-stu-id="7a6c6-118">Add a new event source to the event sources array of the subscription by calling the [**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) function.</span></span>
4.  <span data-ttu-id="7a6c6-119">Задайте свойства источника события, вызвав функцию [**ексетобжектаррайпроперти**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) .</span><span class="sxs-lookup"><span data-stu-id="7a6c6-119">Set the event source properties by calling the [**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) function.</span></span> <span data-ttu-id="7a6c6-120">Свойство **ексубскриптионевентсаурцеаддресс** либо устанавливается в адрес локального компьютера (localhost), либо в полное доменное имя удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="7a6c6-120">The **EcSubscriptionEventSourceAddress** property is either set to an address for the local computer (Localhost) or to a fully qualified domain name for a remote computer.</span></span> <span data-ttu-id="7a6c6-121">Дополнительные сведения о свойствах источника событий, которые можно задать, см. в разделе Перечисление **\_ \_ \_ идентификаторов свойств подписки EC** .</span><span class="sxs-lookup"><span data-stu-id="7a6c6-121">For more information about event source properties that can be set, see the **EC\_SUBSCRIPTION\_PROPERTY\_ID** enumeration.</span></span>
5.  <span data-ttu-id="7a6c6-122">Сохраните подписку, вызвав функцию [**ексавесубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="7a6c6-122">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
6.  <span data-ttu-id="7a6c6-123">Закройте подписку, вызвав функцию [**екклосе**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="7a6c6-123">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="7a6c6-124">В следующем примере кода C++ показано, как добавить источник события в подписку, инициированную сборщиком:</span><span class="sxs-lookup"><span data-stu-id="7a6c6-124">The following C++ code example shows how to add an event source to a collector initiated subscription:</span></span>


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);

void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    std::wstring eventSourceUserName;
    std::wstring eventSourcePassword;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vEventSource = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_VARIANT vProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription( lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to add a new event 
    // source to the subscription.
    dwRetVal = GetProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vEventSource);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained. 
    if (vEventSource->Type != EcVarTypeNull  && 
        vEventSource->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vEventSource->Type == EcVarTypeNull)? NULL: 
        vEventSource->PropertyHandleVal;
    if(!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }
    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Add a new event source to the event source array.
    if (!EcInsertObjectArrayElement(hArray,
        dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vProperty.Type = EcVarTypeString;
    vProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the credentials.
    wcout << "Enter credentials used to connect to the event source " <<
        eventSource << ". " << endl <<
        "Enter user name: " << endl;
    wcin >> eventSourceUserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && eventSourcePassword.length() < 512)
    {eventSourcePassword.append(1, c);}

    // Set the EventSourceUserName property that specifies the user
    // that can retrieve events from the event source.
    if (eventSourceUserName.length() > 0)
    {
        vProperty.Type = EcVarTypeString;
        vProperty.StringVal = eventSourceUserName.c_str();
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourceUserName,
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the EventSourcePassword property that defines the password
        // for the previously-defined user.
        vProperty.StringVal = (eventSourcePassword.length() > 0) ? 
            eventSourcePassword.c_str() : L"";
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourcePassword, 
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // When you have finished using the credentials,
    // erase them.
    eventSourceUserName.erase();
    eventSourcePassword.erase();


    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vProperty.Type = EcVarTypeBoolean;
    vProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 5: Save the subscription to enable the event source.
    if (!EcSaveSubscription(hSubscription, NULL))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 6: Close the subscription.
Cleanup:
    if (hArray)
        EcClose(hArray);
    if (hSubscription)
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u\n  Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }
        wprintf(L"\nFailed to Perform Operation. Error Code: %u\n Error Message: %s\n", dwRetVal, lpwszBuffer);
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
                &dwBufferSize) )
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



## <a name="related-topics"></a><span data-ttu-id="7a6c6-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7a6c6-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7a6c6-126">[Настройка компьютеров на пересылку и получение событий](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="7a6c6-126">[Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="7a6c6-127">Создание подписки сборщика событий</span><span class="sxs-lookup"><span data-stu-id="7a6c6-127">Creating an Event Collector Subscription</span></span>](creating-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="7a6c6-128">Справочник по сборщикам событий Windows</span><span class="sxs-lookup"><span data-stu-id="7a6c6-128">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 