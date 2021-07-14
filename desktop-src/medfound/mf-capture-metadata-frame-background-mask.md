---
description: Сообщает метаданные и буфер маски для фоновой маски сегментации, которая различает фон и передний план видеокадра.
title: Атрибут MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK (Мфапи. h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691865"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>\_ \_ \_ \_ Атрибут маски фона кадра записи \_ MF

Сообщает метаданные и буфер маски для фоновой маски сегментации, которая различает фон и передний план видеокадра.

## <a name="data-type"></a>Тип данных

**ОБЪЕКТЕ**

## <a name="remarks"></a>Комментарии

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

 




