---
description: В следующем примере кода показан обработчик событий для событий Address и Phone Device. Код для каждого события показывает, как создать интерфейс события и как получить данные события.
ms.assetid: 236d4e7f-865f-4b26-8da6-c86476588c47
title: Телефонные и адресные события, связанные с устройством
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cf4c45eb7c7b933a36814f8eba8cd5cc39d8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543471"
---
# <a name="phone-and-address-device-specific-events"></a><span data-ttu-id="4ac7f-104">Телефонные и адресные события, связанные с устройством</span><span class="sxs-lookup"><span data-stu-id="4ac7f-104">Phone and Address Device-specific Events</span></span>

<span data-ttu-id="4ac7f-105">В следующем примере кода показан обработчик событий для событий Address и Phone Device.</span><span class="sxs-lookup"><span data-stu-id="4ac7f-105">The following code example illustrates an event handler for address and phone device events.</span></span> <span data-ttu-id="4ac7f-106">Код для каждого события показывает, как создать интерфейс события и как получить данные события.</span><span class="sxs-lookup"><span data-stu-id="4ac7f-106">The code for each event shows how to create the event interface and how to retrieve the event data.</span></span>

``` syntax
HRESULT STDMETHODCALLTYPE CMyEventNotification::Event(
   TAPI_EVENT TapiEvent,
   IDispatch * pEvent
)
{
    HRESULT hr = S_OK;
    //...
    switch (TapiEvent) 
    {
        case TE_ADDRESSDEVSPECIFIC:
        {
            ITAddressDeviceSpecificEvent* pITADSEvent = NULL;

            hr = pEvent->QueryInterface( 
                               IID_ITAddressDeviceSpecificEvent,
                               (void **)(&pITADSEvent) );
            // If (hr != S_OK) process the error here...

            // Retrieve data received from the TSP.
            long lParam1=0;
            hr = pITADSEvent->get_lParam1(&lParam1);
            // If (hr != S_OK) process the error here...

            long lParam2=0;
            hr = pITADSEvent->get_lParam2(&lParam2);
            // If (hr != S_OK) process the error here...

            long lParam3=0; 
            hr = pITADSEvent->get_lParam3(&lParam3);
            // If (hr !=S_OK) process the error here...

            // Process the data here.
            // ...
            pITADSEvent->Release();
            break;
        }

        case TE_PHONEDEVSPECIFIC:
        {
            ITPhoneDeviceSpecificEvent* pITPhEvent = NULL;

            hr = pEvent->QueryInterface( 
                            IID_ITPhoneDeviceSpecificEvent,
                            (void **)(&pITPhEvent) );
            // If (hr != S_OK) process the error here...

            // Retrieve data received from the TSP.
            long lParam1=0;
            hr = pITPhEvent->get_lParam1(&lParam1);
            // If (hr != S_OK) process the error here...

            long lParam2=0;
            hr = pITPhEvent->get_lParam2(&lParam2);
            // If (hr != S_OK) process the error here...

            long lParam3=0;
            hr = pITPhEvent->get_lParam3(&lParam3);
            // If (hr != S_OK) process the error here...

            // Process the data here.
            //...
            pITPhEvent->Release();
            break;
        }
        //...
    } // end of switch 
    //...
}
```

 

 



