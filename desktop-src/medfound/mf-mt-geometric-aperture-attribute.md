---
description: Определяет геометрическое апертуру для типа видеоклипа.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: Атрибут MF_MT_GEOMETRIC_APERTURE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991473"
---
# <a name="mf_mt_geometric_aperture-attribute"></a>\_ \_ Атрибут геометрического \_ Апертура MF

Определяет геометрическое апертуру для типа видеоклипа.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Значением этого атрибута является структура [**мфвидеоареа**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Пропорции изображения рассчитываются относительно геометрического апертуры с использованием следующей формулы: пропорции рисунка = (геометрическое значение ширины и геометрического апертуры) x пиксельных пропорций.

Если этот атрибут не задан, то геометрический апертурой считается весь кадр видео. Этот атрибут следует задавать только в том случае, если тип носителя описывает стандарт видео с определенной активной областью.

Например, в NTSC-телевидении видеокадр равен 720 × 480 с активной областью 704 x 480 и соотношением пропорций 10:11 в пикселях. Полученное изображение имеет пропорции (704/480) × (10/11) = 4:3.

> [!Note]  
> В средстве визуализации по умолчанию для [расширенного обработчика видео](enhanced-video-renderer.md) (Евр) отображается геометрическое Апертура видео, если оно указано.

 

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="examples"></a>Примеры


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Пропорции рисунка](picture-aspect-ratio.md)
</dt> <dt>

[Типы видеоклипов](video-media-types.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_ \_ \_ Апертура для поиска MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




