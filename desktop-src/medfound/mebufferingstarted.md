---
description: Сообщает, что источник мультимедиа начал работу с данными буфера.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Событие Мебуфферингстартед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719407"
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



## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




