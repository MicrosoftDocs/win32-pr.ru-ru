---
description: Указывает, будет ли подсистема мультимедиа воспроизводить защищенное содержимое.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: Атрибут MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cb6b9c9a49c690af84678435ac2bb4fdab76a2fb13c95fecd9ddc33771d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956444"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>\_ \_ \_ \_ Атрибут флагов защиты содержимого для механизма \_ передачи мультимедиа MF

Указывает, будет ли подсистема мультимедиа воспроизводить защищенное содержимое.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Значение этого атрибута является побитовым для **флагов из перечисления** [**\_ \_ \_ \_ флагов защиты Media Engine MF**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) . Чтобы включить воспроизведение защищенного содержимого, установите флаг **" \_ \_ \_ включить \_ защищенное \_ содержимое" для компонента MF Media Engine** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Мфмедиаенгине. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты обработчика мультимедиа](media-engine-attributes.md)
</dt> <dt>

[**Имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




