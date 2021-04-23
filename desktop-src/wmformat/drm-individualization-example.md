---
title: Пример индивидуализации DRM
description: Пример индивидуализации DRM
ms.assetid: 665a5005-d435-4783-b48e-2d8400aa7638
keywords:
- Пакет SDK для Windows Media Format, индивидуальное управление цифровыми правами DRM
- Пакет SDK для Windows Media Format, индивидуальное
- Управление цифровыми правами (DRM), индивидуальность
- DRM (Управление цифровыми правами), индивидуальность
- Управление цифровыми правами (DRM), Индивидуальная обработка DRM
- DRM (Управление цифровыми правами), Индивидуальная обработка DRM
- Расширенные API клиента DRM, индивидуальность
- Расширенные API клиента, индивидуальность
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1252fe951e306f837f2df95245b3cfc81dac03c2
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2020
ms.locfileid: "104412634"
---
# <a name="drm-individualization-example"></a><span data-ttu-id="2442b-111">Пример индивидуализации DRM</span><span class="sxs-lookup"><span data-stu-id="2442b-111">DRM Individualization Example</span></span>

<span data-ttu-id="2442b-112">Следующий код является примером принудительной индивидуализации, а также демонстрирует использование модели синхронной обработки событий с событиями, которые имеют связанные интерфейсы состояния.</span><span class="sxs-lookup"><span data-stu-id="2442b-112">The following code is an example of forced individualization, and also shows how to use the synchronous event handling model with events that have associated status interfaces.</span></span>


```C++
HRESULT Individualize(IWMDRMSecurity* pSecurity)
{
    HRESULT hr = S_OK;
    
    IMFMediaEvent*                  pEvent        = NULL;
    IUnknown*                       pCancelCookie = NULL;
    IWMDRMIndividualizationStatus*  pIndivStatus  = NULL;   

    MediaEventType EventType    = MEUnknown;
    HRESULT        EventHR      = E_FAIL;
    PROPVARIANT    EventValue;

    WM_INDIVIDUALIZE_STATUS IndivStatusStruct;

    // Intialize local variables.
    ZeroMemory(&IndivStatusStruct, sizeof(IndivStatusStruct));
    PropVariantInit(&EventValue);

    // Check input pointer.
    if (pSecurity == NULL) return E_POINTER;
    
    // Start the security update.
    hr = pSecurity->PerformSecurityUpdate(WMDRM_SECURITY_PERFORM_FORCE_INDIV,
        &pCancelCookie);

    // Get the EventGenerator from the Security interface; this 
    //  is not neccessary, merely illustrative. 
    if (SUCCEEDED(hr))
    {
        hr = pSecurity->QueryInterface( IID_IWMDRMEventGenerator, (void**)&pEventGenerator);
    }

    // Event loop.
    if (SUCCEEDED(hr))
    { 
        do
        {
            // Release the previous event (if there is one).
            SAFE_RELEASE(pEvent);
            SAFE_RELEASE(pIndivStatus);

            // Check for an event.
            hr = pEventGenerator->GetEvent(MF_EVENT_FLAG_NO_WAIT,
                                           &pEvent);

            // If an event was not found, wait a half second and retry.
            if (FAILED(hr))
            {
                Sleep(500);
                continue;
            }

            // Get the event type.
            hr = pEvent->GetType(&EventType);
            
            // 
            if (FAILED(hr))
            {
                printf("Failed to get event type");
                break;
            }

            // Display a message depending on the event.
            switch (EventType)
            {
            case MEWMDRMIndividualizationProgress:

                printf("Received a progress event.\n");
                
                // Get the value of the event.
                hr = pEvent->GetValue(&EventValue);
                if (!SUCCEEDED(hr))
                    break;

                // The event value should be of type VT_UNKNOWN
                //  (an IUnknown pointer).
                if (EventValue.vt != VT_UNKNOWN)
                {
                    // All progress events should have a value of 
                    //  type VT_UNKNOWN. Note this and continue.
                    printf("Unexpected event value type.\n");
                    PropVariantClear(&EventValue);
                    break;
                }

                // Get the extended status interface.
                hr = EventValue.punkVal->QueryInterface(
                    IID_IWMDRMIndividualizationStatus, 
                    (void**)&pIndivStatus);

                // If the interface can't be retrieved, print a
                //  note and continue.
                if (FAILED(hr))
                {
                    printf("Unable to get the extended status interface.\n");
                    PropVariantClear(&EventValue);
                    break;
                }

                // Get the status structure from the newly
                //  acquired interface.
                hr = pIndivStatus->GetStatus(&IndivStatusStruct);

                // If the structure can't be retrieved, make a
                //  note and continue.
                if (FAILED(hr))
                {
                    printf("Unable to get the status structure.\n");
                    PropVariantClear(&EventValue);
                    break;
                }

                //
                // TODO: Print or log the information in the
                //  structure to track status between events.
                //

                // Clear the event value for the next iteration.
                PropVariantClear(&EventValue);
                break;
            case MEWMDRMIndividualizationCompleted:
                printf("Individualization completed.\n");
                break;
            default:
                printf("Received event number %d.\n", EventType);
                break;
            }

            // Give up CPU time to stay out of a busy loop.
            Sleep(0);

        } while (EventType != MEWMDRMIndividualizationCompleted); 
    }

    SAFE_RELEASE(pEvent);
    SAFE_RELEASE(pCancelCookie);
    SAFE_RELEASE(pIndivStatus);
    SAFE_RELEASE(pEventGenerator);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2442b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2442b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2442b-114">**Выполнение индивидуальной управления цифровыми правами**</span><span class="sxs-lookup"><span data-stu-id="2442b-114">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> <dt>

[<span data-ttu-id="2442b-115">**Использование модели событий Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="2442b-115">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




