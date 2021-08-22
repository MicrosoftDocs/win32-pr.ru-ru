---
description: Шаг поверхности по умолчанию для несжатого видеоматериала. STRIDE — это число байтов, необходимое для перехода от одной строки пикселей к следующей.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Атрибут MF_MT_DEFAULT_STRIDE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e130918f62d6ff986ced7dd6449dcc2d381a00fc0d7c0342eeb4afcc03833bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035242"
---
# <a name="mf_mt_default_stride-attribute"></a>MF \_ , \_ по умолчанию, \_ атрибут STRIDE

Шаг поверхности по умолчанию для несжатого видеоматериала. STRIDE — это число байтов, необходимое для перехода от одной строки пикселей к следующей.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как значение **Int32** .

## <a name="remarks"></a>Remarks

Значение атрибута хранится как **UINT32**, но должно быть приведено к значению 32-разрядного целого числа со знаком. Шаг может быть отрицательным.

Шаг имеет положительный значение для нисходящих изображений и отрицательно для изображений в нижней части.

Этот атрибут дает шаг для *непрерывного* представления изображения в памяти; то есть представление без дополнительных байтов заполнения после каждой строки. Если буфер мультимедиа поддерживает интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , используйте метод [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) , чтобы получить фактический шаг в области, который может включать дополнительные байты заполнения.

Дополнительные сведения о параметре STRIDE для поверхности см. в разделе [Шаг с изображением](image-stride.md).

Пример вычисления шага по умолчанию см. в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[Шаг изображения](image-stride.md)
</dt> </dl>

 

 




