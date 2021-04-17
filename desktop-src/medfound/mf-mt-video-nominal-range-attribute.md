---
description: Определяет Номинальный диапазон сведений о цвете в видеоролике.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Атрибут MF_MT_VIDEO_NOMINAL_RANGE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674343"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>\_ \_ \_ Атрибут диапазона номинального видео MF MT \_

Определяет Номинальный диапазон сведений о цвете в видеоролике.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Значение этого атрибута является членом перечисления [**мфноминалранже**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

**Кодировщики H. 264/AVC:**

На выходном типе носителя для \_ \_ параметра номинальный формат видео MF MT \_ \_ можно задать значение **мфноминалранже \_ 0 \_ 255** и **мфноминалранже \_ 16 \_ 235**.

Кодировщик H. 264/AVC должен обрабатывать **мфноминалранже \_ Unknown** как **мфноминалранже \_ 16 \_ 235**.

H. 264/AVC-кодировщик должен отклонить тип выходного \_ носителя \_ \_ , если Номинальный диапазон для видео MF MT \_ имеет значение **мфноминалранже \_ 48 \_ 208**, **мфноминалранже \_ 64 \_ 127** или любые другие значения, не определенные в [**мфноминалранже**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).

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

[Расширенные сведения о цвете](extended-color-information.md)
</dt> </dl>

 

 




