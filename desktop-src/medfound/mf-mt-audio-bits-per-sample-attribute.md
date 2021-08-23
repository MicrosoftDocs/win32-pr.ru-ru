---
description: Число битов на аудио в типе звукового носителя.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: Атрибут MF_MT_AUDIO_BITS_PER_SAMPLE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9697ff5ce97bc7dd9066b57f94e41ff02a599fcf14d1ea8f51c9dea69efc7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104560"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>\_ \_ Звуковой бит MF \_ MT \_ на \_ образец атрибута

Число битов на аудио в типе звукового носителя.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут соответствует элементу **вбитсперсампле** структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .

Если в некоторых битах содержится заполнение, задайте для атрибута номер версии [**MF \_ MT \_ Audio \_ Valid \_ \_ \_**](mf-mt-audio-valid-bits-per-sample-attribute.md) для каждого образца, чтобы указать число битов допустимых звуковых данных в каждом примере.

Если в аудио содержится 8 бит на пример, то звуковые примеры являются неподписанными значениями. (Каждый звуковой образец имеет диапазон от 0 до 255.) Если звук содержит 16 бит на выборку или выше, то звуковые примеры являются значениями со знаком.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



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
</dt> </dl>

 

 
