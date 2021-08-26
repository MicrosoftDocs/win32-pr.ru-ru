---
description: Указывает уровень MPEG-2 или H. 264 в типе видеоматериала.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: Атрибут MF_MT_MPEG2_LEVEL (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1ac99f76d458c1c5964e61181f58f53e7bfce19ab04b09615eaf932dfa2939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060610"
---
# <a name="mf_mt_mpeg2_level-attribute"></a>\_Атрибут уровня "MF MT \_ MPEG2" \_

Указывает уровень MPEG-2 или H. 264 в типе видеоматериала.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Для видео MPEG-2 значение этого атрибута является членом перечисления [**\_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) .

Для видео H. 264 значение является членом перечисления [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) .

Этот атрибут соответствует элементу **двлевел** структуры [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .

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
</dt> </dl>

 

 
