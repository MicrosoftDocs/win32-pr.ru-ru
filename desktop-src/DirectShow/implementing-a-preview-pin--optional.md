---
description: В этом разделе описывается, как реализовать предварительный ПИН-код для фильтра записи DirectShow.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Реализация предварительной версии ПИН-кода (необязательно)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e09d070be2aa154428cb8684ff1c405fac959
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423009"
---
# <a name="implementing-a-preview-pin-optional"></a><span data-ttu-id="bceaf-103">Реализация предварительной версии ПИН-кода (необязательно)</span><span class="sxs-lookup"><span data-stu-id="bceaf-103">Implementing a Preview Pin (Optional)</span></span>

<span data-ttu-id="bceaf-104">В этом разделе описывается, как реализовать предварительный ПИН-код для фильтра записи DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bceaf-104">This topic describes how to implement a preview pin on a DirectShow capture filter.</span></span>

<span data-ttu-id="bceaf-105">Если у фильтра есть Предварительная версия ПИН-кода, ПИН-код для предварительного просмотра должен отправить копию данных, доставленных ПИН-кодом записи.</span><span class="sxs-lookup"><span data-stu-id="bceaf-105">If your filter has a preview pin, the preview pin must send a copy of the data delivered by the capture pin.</span></span> <span data-ttu-id="bceaf-106">Отправляйте данные только из предварительной версии ПИН-кода, когда это не приведет к тому, что закрепление будет удалено.</span><span class="sxs-lookup"><span data-stu-id="bceaf-106">Only send data from the preview pin when doing so will not cause the capture pin to drop frames.</span></span> <span data-ttu-id="bceaf-107">ПИН-код захвата всегда имеет приоритет над ПИН-кодом предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="bceaf-107">The capture pin always has priority over the preview pin.</span></span>

<span data-ttu-id="bceaf-108">ПИН-код записи и ПИН-код для предварительного просмотра должны отправить данные с тем же форматом.</span><span class="sxs-lookup"><span data-stu-id="bceaf-108">The capture pin and the preview pin must send data with the same format.</span></span> <span data-ttu-id="bceaf-109">Поэтому они должны подключаться с использованием идентичных типов носителей.</span><span class="sxs-lookup"><span data-stu-id="bceaf-109">Therefore, they must connect using identical media types.</span></span> <span data-ttu-id="bceaf-110">Если ПИН-код записи подключается первыми, ПИН-код предварительной версии должен предоставлять тот же тип носителя и отклонять другие типы.</span><span class="sxs-lookup"><span data-stu-id="bceaf-110">If the capture pin connects first, the preview pin should offer the same media type, and reject any others types.</span></span> <span data-ttu-id="bceaf-111">Если предварительный ПИН-код подключается первым, а ПИН-код записи подключается к другому типу носителя, то предварительный ПИН-код должен повторно подключиться с помощью нового типа носителя.</span><span class="sxs-lookup"><span data-stu-id="bceaf-111">If the preview pin connects first, and the capture pin connects with a different media type, the preview pin should reconnect using the new media type.</span></span> <span data-ttu-id="bceaf-112">Если фильтр, находящийся в режиме предварительного просмотра, отклоняет новый тип, ПИН-код записи также должен отклонять тип.</span><span class="sxs-lookup"><span data-stu-id="bceaf-112">If the filter downstream from the preview pin rejects the new type, the capture pin should also reject the type.</span></span> <span data-ttu-id="bceaf-113">Используйте метод [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) для запроса фильтра, находящийся в режиме предварительного просмотра, и используйте метод [**ифилтерграф:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) для повторного подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="bceaf-113">Use the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method to query the filter downstream from the preview pin, and use the [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) method to reconnect the pin.</span></span> <span data-ttu-id="bceaf-114">Эти правила также применяются, если диспетчер графа фильтров повторно подключает ПИН-код захвата.</span><span class="sxs-lookup"><span data-stu-id="bceaf-114">These rules also apply if the Filter Graph Manager reconnects the capture pin.</span></span>

<span data-ttu-id="bceaf-115">В следующем примере показана структура этого процесса:</span><span class="sxs-lookup"><span data-stu-id="bceaf-115">The following example shows an outline of this process:</span></span>


```C++
// Override CBasePin::CheckMediaType.
CCapturePin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so query the pin it is
        // connected to. If the other pin rejects it, so do we.
        hr = m_pMyPreviewPin->GetConnected()->QueryAccept(pmt);
        if (hr != S_OK) 
        {
            // The preview pin cannot reconnect with this media type.
            return E_INVALIDARG;
        }
        // The preview pin will reconnect when SetMediaType is called.
    }
    // Decide whether the capture pin accepts the format. 
    BOOL fAcceptThisType = ...  // (Not shown.)
    return (fAcceptThisType? S_OK : E_FAIL);
}

// Override CBasePin::SetMediaType.
CCapturePin::SetMediaType(CMediaType *pmt);
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so it must reconnect.
        if (m_pMyPreviewPin->GetConnected()->QueryAccept(pmt) == S_OK)
        {
            // The downstream pin will accept the new type, so it's safe
            // to reconnect. 
            m_pFilter->m_pGraph->Reconnect(m_pMyPreviewPin);
        }
        else
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }
    // Now do anything that the capture pin needs to set the type.
    hr = MyInternalSetMediaType(pmt);

    // And finally, call the base-class method.
    return CBasePin::SetMediaType(pmt);
}

CPreviewPin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyCapturePin->IsConnected())
    {
       // The preview pin must connect with the same type.
       CMediaType cmt = m_pMyCapturePin->m_mt;
       return (*pmt == cmt ? S_OK : VFW_E_INVALIDMEDIATYPE);
    }
    // Decide whether the preview pin accepts the format. You can use your 
    // knowledge of which types the capture pin will accept. Regardless,
    // when the capture pin connects, the preview pin will reconnect.
    return (fAcceptThisType? S_OK : E_FAIL);
}
```



## <a name="related-topics"></a><span data-ttu-id="bceaf-116">См. также</span><span class="sxs-lookup"><span data-stu-id="bceaf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bceaf-117">Как подключаются фильтры</span><span class="sxs-lookup"><span data-stu-id="bceaf-117">How Filters Connect</span></span>](how-filters-connect.md)
</dt> <dt>

[<span data-ttu-id="bceaf-118">Запись фильтров записи</span><span class="sxs-lookup"><span data-stu-id="bceaf-118">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



