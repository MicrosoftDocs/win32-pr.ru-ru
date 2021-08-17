---
description: Количество допустимых битов звуковых данных в каждом звуковом примере.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: Атрибут MF_MT_AUDIO_VALID_BITS_PER_SAMPLE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f84fa3938e4d74473da70bd28e5ccbb1bab71441c694b670cdb8b54bead31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973583"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>\_ \_ \_ Допустимый бит MF \_ \_ на \_ примере атрибута

Количество допустимых битов звуковых данных в каждом звуковом примере.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Для звуковых форматов, содержащих заполнение после каждого аудио-образца, используется звуковая подложка **MF \_ MT. \_ \_ Допустимые \_ биты \_ на \_ Пример** атрибута. Общий размер каждого образца звука, включая биты заполнения, задается в атрибуте [**MF \_ \_ Audio \_ бит \_ \_**](mf-mt-audio-bits-per-sample-attribute.md) в указанном примере.

Если для образца атрибута не задано **допустимое количество аудио-файлов MF \_ MT на \_ \_ \_ \_ \_ выборку** , то для определения числа допустимых битов на выборку используйте номер [**MF \_ MT Audio- \_ \_ бит \_ на \_ Пример**](mf-mt-audio-bits-per-sample-attribute.md) .

Если формат аудио не содержит никаких битов заполнения, то этот атрибут не должен быть установлен или должен иметь то же значение, что и [**\_ \_ звуковый бит MF MT \_ \_ на каждый \_ Пример**](mf-mt-audio-bits-per-sample-attribute.md) атрибута.

Этот атрибут соответствует элементу **ввалидбитсперсампле** структуры [**вавеформатекстенсибле**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .

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

 

 
