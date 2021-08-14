---
description: Определяет Номинальный диапазон сведений о цвете в видеоролике.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Атрибут MF_MT_VIDEO_NOMINAL_RANGE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b294ea3c63f845b51c9636f78ee78f04135e17929ae6e64d92ab85720f3c7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876724"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>\_ \_ \_ Атрибут диапазона номинального видео MF MT \_

Определяет Номинальный диапазон сведений о цвете в видеоролике.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Значение этого атрибута является членом перечисления [**мфноминалранже**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

**Кодировщики H. 264/AVC:**

На выходном типе носителя для \_ \_ параметра номинальный формат видео MF MT \_ \_ можно задать значение **мфноминалранже \_ 0 \_ 255** и **мфноминалранже \_ 16 \_ 235**.

Кодировщик H. 264/AVC должен обрабатывать **мфноминалранже \_ Unknown** как **мфноминалранже \_ 16 \_ 235**.

H. 264/AVC-кодировщик должен отклонить тип выходного \_ носителя \_ \_ , если Номинальный диапазон для видео MF MT \_ имеет значение **мфноминалранже \_ 48 \_ 208**, **мфноминалранже \_ 64 \_ 127** или любые другие значения, не определенные в [**мфноминалранже**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
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

 

 




