---
description: Шаг поверхности по умолчанию для несжатого видеоматериала. STRIDE — это число байтов, необходимое для перехода от одной строки пикселей к следующей.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Атрибут MF_MT_DEFAULT_STRIDE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263621"
---
# <a name="mf_mt_default_stride-attribute"></a>MF \_ , \_ по умолчанию, \_ атрибут STRIDE

Шаг поверхности по умолчанию для несжатого видеоматериала. STRIDE — это число байтов, необходимое для перехода от одной строки пикселей к следующей.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как значение **Int32** .

## <a name="remarks"></a>Комментарии

Значение атрибута хранится как **UINT32**, но должно быть приведено к значению 32-разрядного целого числа со знаком. Шаг может быть отрицательным.

Шаг имеет положительный значение для нисходящих изображений и отрицательно для изображений в нижней части.

Этот атрибут дает шаг для *непрерывного* представления изображения в памяти; то есть представление без дополнительных байтов заполнения после каждой строки. Если буфер мультимедиа поддерживает интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , используйте метод [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) , чтобы получить фактический шаг в области, который может включать дополнительные байты заполнения.

Дополнительные сведения о параметре STRIDE для поверхности см. в разделе [Шаг с изображением](image-stride.md).

Пример вычисления шага по умолчанию см. в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

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

 

 




