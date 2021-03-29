---
description: Указывает, как создать пользовательское микшер для расширенного обработчика видео (Евр).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815513"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>MF \_ активировать \_ Пользовательский \_ \_ \_ атрибут флагов микшера видео

Указывает, как создать пользовательское микшер для расширенного обработчика видео (Евр).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут можно задать для указателя [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного из функции [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) . Значение этого атрибута является побитовым оператором **или** для следующих значений.



| Значение                                      | Описание                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ Активация \_ настраиваемого \_ алловфаил микшера \_** | Если метод [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) не может создать пользовательское микшер приложения, вместо него используется микшер Евр по умолчанию. По умолчанию, если при попытке создания пользовательского микшера происходит сбой объекта [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , метод **активатеобжект** завершается ошибкой. |



 

Приложения могут использовать [**\_ \_ настраиваемый атрибут \_ \_ \_ CLSID "порт MF**](mf-activate-custom-video-mixer-clsid-attribute.md) ", чтобы указать пользовательское микшер для Евр.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Расширенные атрибуты модуля подготовки видео](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Объекты активации](activation-objects.md)
</dt> </dl>

 

 




