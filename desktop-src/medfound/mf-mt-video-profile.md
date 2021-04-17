---
description: Задает профиль кодирования видео для выходного типа носителя. Это псевдоним \_ \_ атрибута профиля MF MT MPEG2 \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Атрибут MF_MT_VIDEO_PROFILE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712863"
---
# <a name="mf_mt_video_profile-attribute"></a>\_ \_ Атрибут профиля видео MF MT \_

Задает профиль кодирования видео для выходного типа носителя. Это псевдоним атрибута [ \_ \_ \_ профиля MF MT MPEG2](mf-mt-mpeg2-profile-attribute.md) .

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

**Кодировщики H. 264:**

В число поддерживаемых профилей входят [**eAVEncH264VProfile \_ Констраинедбасе**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) и **eAVEncH264VProfile \_ констраинедхигх**.

Кодировщики должны поддерживать методы [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) и [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) для этого атрибута.

Это статические, поэтому видеокодировщики необходимо настроить перед запуском потоковой передачи. Если приложение задает профиль, который не поддерживает кодировщик, кодировщик должен отклонить тип носителя.

Рекомендуемое значение по умолчанию: [**\_ основной профиль eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                       |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
