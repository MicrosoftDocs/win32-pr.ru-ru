---
description: Повторное подключение входных данных для обеспечения конкретных типов выходных данных
ms.assetid: c83d002e-59bf-4d03-9917-e39ceab9a4ce
title: Повторное подключение входных данных для обеспечения конкретных типов выходных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74d6914989231542ddfea9f97e93ce860d34eb4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416600"
---
# <a name="reconnecting-your-input-to-ensure-specific-output-types"></a><span data-ttu-id="29b95-103">Повторное подключение входных данных для обеспечения конкретных типов выходных данных</span><span class="sxs-lookup"><span data-stu-id="29b95-103">Reconnecting Your Input to Ensure Specific Output Types</span></span>

<span data-ttu-id="29b95-104">Фильтры реализуют метод [**иамстреамконфиг:: сетформат**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , чтобы задать формат аудио или видео перед подключением ПИН-кодов фильтра.</span><span class="sxs-lookup"><span data-stu-id="29b95-104">Filters implement the [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method to set the audio or video format before the filter's pins are connected.</span></span> <span data-ttu-id="29b95-105">Если ПИН-код выхода уже подключен и вы можете указать новый тип, подключите ПИН-код, но только в том случае, если другой фильтр может принять новый тип.</span><span class="sxs-lookup"><span data-stu-id="29b95-105">If your output pin is already connected and you can provide a new type, then reconnect your pin, but only if the other filter can accept the new type.</span></span> <span data-ttu-id="29b95-106">Если другой фильтр не может принять тип мультимедиа, завершите вызов **сетформат** и оставьте только подключение.</span><span class="sxs-lookup"><span data-stu-id="29b95-106">If the other filter cannot accept the media type, fail the call to **SetFormat** and leave your connection alone.</span></span>

<span data-ttu-id="29b95-107">Фильтр преобразования может не иметь предпочтительных выходных типов, если только их входной ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="29b95-107">A transform filter may not have any preferred output types unless their input pin is connected.</span></span> <span data-ttu-id="29b95-108">В этом случае методы **сетформат** и [**Иамстреамконфиг:: жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) должны возвращать VFW \_ E \_ без \_ подключения, пока не будет подключен входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="29b95-108">In that case, the **SetFormat** and [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) methods should return VFW\_E\_NOT\_CONNECTED until the input pin is connected.</span></span> <span data-ttu-id="29b95-109">В противном случае эти методы могут работать как обычно.</span><span class="sxs-lookup"><span data-stu-id="29b95-109">Otherwise, these methods can function as usual.</span></span>

<span data-ttu-id="29b95-110">В некоторых случаях полезно повторно подключить ПИН-коды при создании формата для установленного соединения.</span><span class="sxs-lookup"><span data-stu-id="29b95-110">In certain cases it is useful to reconnect pins when you are offering a format on an established connection.</span></span> <span data-ttu-id="29b95-111">Например, предположим, что фильтр может сжимать 24-битное видео RGB в формате X и может сжимать 8-битное видео RGB в формате Y. ПИН-код выхода может выполнять одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="29b95-111">For example, suppose that a filter can compress 24-bit RGB video into format X, and that it can compress 8-bit RGB video into format Y. The output pin can do either of the following:</span></span>

-   <span data-ttu-id="29b95-112">Всегда предлагать как X и Y в **жетстреамкапс** и всегда принимать как x, так и y в **сетформат**.</span><span class="sxs-lookup"><span data-stu-id="29b95-112">Always offer both X and Y in **GetStreamCaps**, and always accept both X and Y in **SetFormat**.</span></span>
-   <span data-ttu-id="29b95-113">Предложение и принять только формат X, если входной тип — 24-разрядный RGB.</span><span class="sxs-lookup"><span data-stu-id="29b95-113">Offer and accept just format X if the input type is 24-bit RGB.</span></span> <span data-ttu-id="29b95-114">Предложение и принимает просто формат Y, если тип входных данных 8-разрядный RGB.</span><span class="sxs-lookup"><span data-stu-id="29b95-114">Offer and accept just format Y if the input type 8-bit RGB.</span></span> <span data-ttu-id="29b95-115">Завершать оба метода, если входной ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="29b95-115">Fail both methods if the input pin is not connected.</span></span>

<span data-ttu-id="29b95-116">В любом случае потребуется переподключить код, который будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="29b95-116">In either case, you will need some reconnecting code that looks like this:</span></span>


```C++
HRESULT MyOutputPin::CheckMediaType(const CMediaType *pmtOut)
{
    // Fail if the input pin is not connected.
    if (!m_pFilter->m_pInput->IsConnected()) {
        return VFW_E_NOT_CONNECTED;
    }

    // (Not shown: Reject any media types that you know in advance your 
    // filter cannot use. Check the major type and subtype GUIDs.)

    // (Not shown: If SetFormat was previously called, check whether
    // pmtOut exactly matches the format that was specified in SetFormat.
    // Return S_OK if they match, or VFW_E_INVALIDMEDIATYPE otherwise.)
   
    // Now do the normal check for this media type.
    HRESULT hr;
    hr = m_pFilter->CheckTransform(
        &m_pFilter->m_pInput->CurrentMediaType(),  // The input type.
        pmtOut  // The proposed output type.
    );
    if (hr == S_OK)
    {
        // This format is compatible with the current input type.
        return S_OK;
    }
 
    // This format is not compatible with the current input type. 
    // Maybe we can reconnect the input pin with a new input type.
    
    // Enumerate the upstream filter's preferred output types, and 
    // see if one of them will work.
    CMediaType *pmtEnum;
    BOOL fFound = FALSE;
    IEnumMediaTypes *pEnum;
    hr = m_pFilter->m_pInput->GetConnected()->EnumMediaTypes(&pEnum);
    if (hr != S_OK)
    {
        return E_FAIL;
    }
    while (hr = pEnum->Next(1, (AM_MEDIA_TYPE **)&pmtEnum, NULL), hr == S_OK)
    {
        // Check this input type against the proposed output type.
        hr = m_pFilter->CheckTransform(pmtEnum, pmtOut);
        if (hr != S_OK) 
        {
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }

        // This input type is a possible candidate. But, we have to make
        // sure that the upstream filter can switch to this type. 
        hr = m_pFilter->m_pInput->GetConnected()->QueryAccept(pmtEnum);
        if (hr != S_OK) 
        {
            // The upstream filter will not switch to this type.
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }
        fFound = TRUE;
        DeleteMediaType(pmtEnum);
        break;
    }
    pEnum->Release();

    if (fFound)
    {
        // This output type is OK, but if we are asked to use it, we will
        // need to reconnect our input pin. (See SetFormat, below.)
        return S_OK;
    }
    else
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
}

HRESULT MyOutputPin::SetFormat(AM_MEDIA_TYPE *pmt)
{
    CheckPointer(pmt, E_POINTER);
    HRESULT hr;

    // Hold the filter state lock, to make sure that streaming isn't 
    // in the middle of starting or stopping:
    CAutoLock cObjectLock(&m_pFilter->m_csFilter);

    // Cannot set the format unless the filter is stopped.
    if (m_pFilter->m_State != State_Stopped)
    {
        return VFW_E_NOT_STOPPED;
    }

    // The set of possible output formats depends on the input format,
    // so if the input pin is not connected, return a failure code.
    if (!m_pFilter->m_pInput->IsConnected())
    {
        return VFW_E_NOT_CONNECTED;
    }

    // If the pin is already using this format, there's nothing to do.
    if (IsConnected() && CurrentMediaType() == *pmt)
    {
        return S_OK;
    }

    // See if this media type is acceptable.
    if ((hr = CheckMediaType((CMediaType *)pmt)) != S_OK) 
    {
        return hr;
    }

    // If we're connected to a downstream filter, we have to make
    // sure that the downstream filter accepts this media type.
    if (IsConnected()) 
    {
        hr = GetConnected()->QueryAccept(pmt);
        if (hr != S_OK)
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }

    // Now make a note that from now on, this is the only format allowed,
    // and refuse anything but this in the CheckMediaType code above.

    // Changing the format means reconnecting if necessary.
    if (IsConnected())
    {
        m_pFilter->m_pGraph->Reconnect(this);
    }

    return NOERROR;
}


// Override CTransformFilter::SetMediaType to reconnect the input pin. 
// This method is called immediately after the media type is set on a pin.
HRESULT MyFilter::SetMediaType(
    PIN_DIRECTION direction, 
    const CMediaType *pmt
)
{
    HRESULT hr;
    if (direction == PINDIR_OUTPUT) 
    {
        // Before we set the output type, we might need to reconnect 
        // the input pin with a new type.
        if (m_pInput && m_pInput->IsConnected()) 
        {
            // Check if the current input type is compatible.
            hr = CheckTransform(
                    &m_pInput->CurrentMediaType(),
                    &m_pOutput->CurrentMediaType());
            if (SUCCEEDED(hr))
            {
                return S_OK;
            }
            // Otherwise, we need to reconnect the input pin.
            // Note: The CheckMediaType method has already called 
            // QueryAccept on the upstream filter. 
            hr = m_pGraph->Reconnect(m_pInput);
            return hr;
        }
    }
    return S_OK;
}
```



 

 



