---
description: 'Вызывается после асинхронного завершения метода Имфмедиасессион:: Сеттопологи. Сеанс мультимедиа создает это событие после того, как оно разрешает топологию в полную топологию и помещает топологию для воспроизведения в очередь.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Событие Месессионтопологисет (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991487"
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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




