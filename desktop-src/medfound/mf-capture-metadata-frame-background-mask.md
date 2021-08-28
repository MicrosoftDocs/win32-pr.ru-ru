---
description: Сообщает метаданные и буфер маски для фоновой маски сегментации, которая различает фон и передний план видеокадра.
title: Атрибут MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK (Мфапи. h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 1c9cf48235483f13cfa6f9fc04aace5baaf030cf1eb2597b86e9361176a0b9b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973983"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>\_ \_ \_ \_ Атрибут маски фона кадра записи \_ MF

Сообщает метаданные и буфер маски для фоновой маски сегментации, которая различает фон и передний план видеокадра.

## <a name="data-type"></a>Тип данных

**ОБЪЕКТЕ**

## <a name="remarks"></a>Remarks

Данными, переданными по этому атрибуту, является структура [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) , содержащая сведения об измерениях фоновой маски, а также о покрытии фрейма, от которого она выводится, это кадр, выводимый потоком. Он также содержит непрерывный буфер, представляющий маску, используемую приложением для определения того, какие пиксели считаются частью переднего плана или фона. Масштабирование и корреляция координат изображения маски, относящейся к кадру, обрабатываются приложением, которое использует приложение. 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 22000t сборки<br/>                          |
| Минимальная версия сервера<br/> | Windows Сборка 22000<br/>                      |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 




