---
description: 'Вызывается после асинхронного завершения метода Имфмедиасессион:: Сеттопологи. Сеанс мультимедиа создает это событие после того, как оно разрешает топологию в полную топологию и помещает топологию для воспроизведения в очередь.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Событие Месессионтопологисет (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2b5454309855ff472c633388cddabe0c12fab09e2ae462aacd2de49c3c9bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957404"
---
# <a name="mesessiontopologyset-event"></a>Событие Месессионтопологисет

Вызывается после асинхронного завершения метода [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) . Сеанс мультимедиа создает это событие после того, как оно разрешает топологию в полную топологию и помещает топологию для воспроизведения в очередь.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE                | Описание                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ пуст<br/>   | Нет данных события.<br/> <br/>                                                                    |
| VT \_ Unknown<br/> | Указатель на интерфейс [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) полной топологии.<br/> <br/> |



## <a name="examples"></a>Примеры

В следующем примере извлекается указатель [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) из события месессионтопологисет.


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




