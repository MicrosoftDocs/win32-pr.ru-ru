---
description: В поле Тип звукового носителя указывает назначение звуковых каналов для позиционирования динамиков.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: Атрибут MF_MT_AUDIO_CHANNEL_MASK (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 544f287ad9cc8addc60245143e079f0ccdd3c1fead043198be93eed59babc98c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955934"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a>\_ \_ \_ Атрибут маски канала MF MT Audio \_

В поле Тип звукового носителя указывает назначение звуковых каналов для позиционирования динамиков.

## <a name="data-type"></a>Тип данных

**UINT32**

Значение этого атрибута является побитовым оператором **или** для следующих флагов, которые определены в файле заголовка ммрег. h.

<dl> <dt>

<span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**Докладчик \_ ПЕРЕДНИй \_ левый** (0x1)
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**Докладчик \_ ПЕРЕДНИй \_ правый** (0x2)
</dt> <dt>

<span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**Докладчик \_ ПЕРЕДНИй \_ Центральный центр** (0x4)
</dt> <dt>

<span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**Докладчик \_ НИЗКАЯ \_ Частота** (0x8)
</dt> <dt>

<span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**Докладчик \_ НАЗАД \_ влево** (0x10)
</dt> <dt>

<span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**Докладчик \_ ЗАДНий \_ правый** (0x20)
</dt> <dt>

<span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**Докладчик \_ ПЕРЕДНИй \_ левый \_ от \_ центра Center** (0x40)
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**Докладчик \_ ПЕРЕДНИй \_ правый \_ \_ центра** (0x80)
</dt> <dt>

<span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**Докладчик \_ ЗАДНЯЯ \_ центр** (0x100)
</dt> <dt>

<span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**Докладчик \_ БОКОВая \_ слева** (0x200)
</dt> <dt>

<span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**Докладчик \_ \_Справа** (0x400)
</dt> <dt>

<span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**Докладчик \_ \_Центр вверху** (0x800)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**Докладчик \_ СВЕРХУ \_ спереди \_ слева** (0x1000)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**Докладчик \_ ВЕРХНИЙ \_ передний \_ Центральный центр** (0x2000)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**Докладчик \_ ВЕРХНИЙ \_ передний \_ правый** (0x4000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**Докладчик \_ Верхний \_ задний \_ левый край** (0x8000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**Докладчик \_ ВЕРХНИЙ \_ задний \_ центр** (0x10000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**Докладчик \_ ВЕРХНИЙ \_ задний \_ правый** (0x20000)
</dt> </dl>

## <a name="remarks"></a>Remarks

Этот атрибут соответствует элементу **двчаннелмаск** структуры [**вавеформатекстенсибле**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



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
</dt> </dl>

 

 
