---
description: Указывает профиль MPEG-2 или H. 264 в типе видеоматериала.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: Атрибут MF_MT_MPEG2_PROFILE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911188"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a>\_ \_ Атрибут профиля MF MT MPEG2 \_

Указывает профиль MPEG-2 или H. 264 в типе видеоматериала.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Для видео MPEG-2 значение этого атрибута является членом перечисления [**\_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) .

Для видео H. 264 значение является членом перечисления [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .

Этот атрибут соответствует элементу **двпрофиле** структуры [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .

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
</dt> </dl>

 

 
