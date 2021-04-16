---
description: Указывает исходный прямоугольник для видеомикшера расширенного обработчика видео (Евр). Исходный прямоугольник — это часть видеокадра, блитс микшер на поверхность назначения.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: Атрибут VIDEO_ZOOM_RECT (Евр. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662680"
---
# <a name="video_zoom_rect-attribute"></a>\_ \_ Атрибут Rect масштаба видео

Указывает исходный прямоугольник для видеомикшера [расширенного обработчика видео](enhanced-video-renderer.md) (Евр). Исходный прямоугольник — это часть видеокадра, блитс микшер на поверхность назначения.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Значением этого атрибута является структура [**мфвидеонормализедрект**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .

Исходный прямоугольник определяется относительно нормализованной системы координат, в которой весь кадр видео занимает прямоугольник с координатами {0, 0, 1, 1}. Исходный прямоугольник должен помещаться в кадре видео; координаты исходного прямоугольника имеют диапазон (0... 1).

Стандартный выступающий Евр задает этот атрибут для микшера. Чтобы задать атрибут, выполните следующие действия.

1.  Вызовите [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в микшере, чтобы получить хранилище атрибутов микшера.
2.  Вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) , чтобы задать для микшера атрибут **\_ \_ Rect масштаба видео** . Значение является структурой [**мфвидеонормализедрект**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .

В пользовательском выступающем Евр можно использовать этот атрибут для реализации метода [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) . Дополнительные сведения см. в разделе [прямоугольники источника и назначения](how-to-write-an-evr-presenter.md).

Константа GUID для этого атрибута экспортируется из стрмиидс. lib.

## <a name="examples"></a>Примеры

В следующем примере задается исходный прямоугольник в микшере.


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                             |
| Header<br/>                   | <dl> <dt>Евр. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Расширенные атрибуты модуля подготовки видео](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Написание выступающего Евр](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




