---
description: Задает профиль кодирования видео для выходного типа носителя. Это псевдоним \_ \_ атрибута профиля MF MT MPEG2 \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Атрибут MF_MT_VIDEO_PROFILE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2af7c6ebbbbb78626e96385a6eda5a25c38a3ae8473fac866866248570cc48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741397"
---
# <a name="mf_mt_video_profile-attribute"></a>\_ \_ Атрибут профиля видео MF MT \_

Задает профиль кодирования видео для выходного типа носителя. Это псевдоним атрибута [ \_ \_ \_ профиля MF MT MPEG2](mf-mt-mpeg2-profile-attribute.md) .

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

**Кодировщики H. 264:**

В число поддерживаемых профилей входят [**eAVEncH264VProfile \_ Констраинедбасе**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) и **eAVEncH264VProfile \_ констраинедхигх**.

Кодировщики должны поддерживать методы [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) и [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) для этого атрибута.

Это статические, поэтому видеокодировщики необходимо настроить перед запуском потоковой передачи. Если приложение задает профиль, который не поддерживает кодировщик, кодировщик должен отклонить тип носителя.

Рекомендуемое значение по умолчанию: [**\_ основной профиль eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
