---
description: Сообщает, что источник мультимедиа начал работу с данными буфера.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Событие Мебуфферингстартед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55a691b723fc2e09487752ee8f5226e32504d60a6d68a4652bbb2b5b3e5aa7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724274"
---
# <a name="mebufferingstarted-event"></a>Событие Мебуфферингстартед

Сообщает, что источник мультимедиа начал работу с данными буфера.

Источник мультимедиа может отправить это событие, если исходные буферы находятся во время выполнения сеанса мультимедиа. Когда сеанс мультимедиа получает это событие, он приостанавливает время презентации, пока источник мультимедиа не отправит событие [мебуфферингстоппед](mebufferingstopped.md) . Сеанс мультимедиа также перенаправляет событие Мебуфферингстартед в приложение.

Потоковые потоки, которые реализуют интерфейс [**имфбитестреамбуфферинг**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) , также отправляют это событие.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Remarks

Если источник мультимедиа отправляет событие Мебуфферингстартед, он должен отправить событие [мебуфферингстоппед](mebufferingstopped.md) при остановке буферизации данных. Источник мультимедиа должен отправить соответствующее событие Мебуфферингстоппед для каждого события Мебуфферингстартед. Источник мультимедиа не должен пересылать эти события перед вызовом метода [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) источника или после вызова метода [**Имфмедиасаурце:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) источника.

При потоковой передаче из Media Foundation сетевого источника можно получить ход буферизации, запросив статистику по **\_ \_ идентификатору буфферпрогресс мфнетсаурце** . Дополнительные сведения см. в разделе [**мфнетсаурце \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

## <a name="examples"></a>Примеры


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
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
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




