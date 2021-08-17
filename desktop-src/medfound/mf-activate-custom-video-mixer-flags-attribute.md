---
description: Указывает, как создать пользовательское микшер для расширенного обработчика видео (Евр).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd536328bf454a70b35376aca3b7c6a0cea9ec7e0e2408a05cd6d0e8da0854ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957094"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>MF \_ активировать \_ Пользовательский \_ \_ \_ атрибут флагов микшера видео

Указывает, как создать пользовательское микшер для расширенного обработчика видео (Евр).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут можно задать для указателя [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного из функции [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) . Значение этого атрибута является побитовым оператором **или** для следующих значений.



| Значение                                      | Описание                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ Активация \_ настраиваемого \_ алловфаил микшера \_** | Если метод [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) не может создать пользовательское микшер приложения, вместо него используется микшер Евр по умолчанию. По умолчанию, если при попытке создания пользовательского микшера происходит сбой объекта [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , метод **активатеобжект** завершается ошибкой. |



 

Приложения могут использовать [**\_ \_ настраиваемый атрибут \_ \_ \_ CLSID "порт MF**](mf-activate-custom-video-mixer-clsid-attribute.md) ", чтобы указать пользовательское микшер для Евр.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



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

 

 




