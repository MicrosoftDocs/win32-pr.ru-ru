---
description: Указывает пользовательские первичные цвета для типа видеоклипа.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: Атрибут MF_MT_CUSTOM_VIDEO_PRIMARIES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703145"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a>\_ \_ \_ Атрибут пользовательского первичного элемента видео MF MT \_

Указывает пользовательские первичные цвета для типа видеоклипа.

## <a name="data-type"></a>Тип данных

**UINT32**

массив байтов;

## <a name="remarks"></a>Комментарии

Данные атрибута являются [**пользовательской структурой \_ \_ \_ первичного цвета видео**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .

Этот атрибут определяет фактический цветовой объем содержимого или изображения. CEA-861,3/SMPTE ST. 2086 сведения об основных томах хранятся в этом атрибуте декодерами. Обратите внимание на то, что этот атрибут не заменяет атрибут [**\_ \_ \_ первичного видео в MF MT**](mf-mt-video-primaries-attribute.md). Этот атрибут описывает подсказку о цветовой громкости содержимого, тогда как **\_ \_ \_ первичные цвета видео MF MT** описывают цветовые цвета, в которых содержимое фактически закодировано (например, значение 1,0 в каналах R/g/B представления с плавающей запятой).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




