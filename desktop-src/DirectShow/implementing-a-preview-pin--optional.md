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
# <a name="implementing-a-preview-pin-optional"></a>Реализация предварительной версии ПИН-кода (необязательно)

В этом разделе описывается, как реализовать предварительный ПИН-код для фильтра записи DirectShow.

Если у фильтра есть Предварительная версия ПИН-кода, ПИН-код для предварительного просмотра должен отправить копию данных, доставленных ПИН-кодом записи. Отправляйте данные только из предварительной версии ПИН-кода, когда это не приведет к тому, что закрепление будет удалено. ПИН-код захвата всегда имеет приоритет над ПИН-кодом предварительной версии.

ПИН-код записи и ПИН-код для предварительного просмотра должны отправить данные с тем же форматом. Поэтому они должны подключаться с использованием идентичных типов носителей. Если ПИН-код записи подключается первыми, ПИН-код предварительной версии должен предоставлять тот же тип носителя и отклонять другие типы. Если предварительный ПИН-код подключается первым, а ПИН-код записи подключается к другому типу носителя, то предварительный ПИН-код должен повторно подключиться с помощью нового типа носителя. Если фильтр, находящийся в режиме предварительного просмотра, отклоняет новый тип, ПИН-код записи также должен отклонять тип. Используйте метод [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) для запроса фильтра, находящийся в режиме предварительного просмотра, и используйте метод [**ифилтерграф:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) для повторного подключения ПИН-кода. Эти правила также применяются, если диспетчер графа фильтров повторно подключает ПИН-код захвата.

В следующем примере показана структура этого процесса:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Как подключаются фильтры](how-filters-connect.md)
</dt> <dt>

[Запись фильтров записи](writing-capture-filters.md)
</dt> </dl>

 

 



