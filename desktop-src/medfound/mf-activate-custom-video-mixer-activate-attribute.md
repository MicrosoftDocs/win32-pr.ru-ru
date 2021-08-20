---
description: Указывает объект активации, который создает пользовательский Видеомикшер для приемника расширенного модуля подготовки видео (Евр).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1966efe66efaba56c0206a9f6fac59aba30a1aea9d47100c4ce19a30af96a863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877301"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>MF \_ Активация \_ пользовательского \_ \_ микшера \_ активации атрибута

Указывает объект активации, который создает пользовательский Видеомикшер для приемника расширенного модуля подготовки видео (Евр).

## <a name="data-type"></a>Тип данных

**IUnknown\***

## <a name="remarks"></a>Remarks

При создании Евр с помощью объекта активации этот атрибут можно использовать для установки пользовательского видеомикшера на Евр. Используйте этот атрибут, как показано ниже.

1.  Вызовите функцию [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) , чтобы создать объект активации для Евр. Функция возвращает указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
2.  Установите этот атрибут для указателя [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , вызвав [**Имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). Значение атрибута является указателем на объект активации, реализованный вызывающим объектом. Объект активации вызывающего объекта должен предоставлять интерфейс **имфактивате** .

Если задать этот атрибут, ЕВР вызывает [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) для создания пользовательского видеомикшера. Видеомикшер должен предоставлять интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Расширенные атрибуты модуля подготовки видео](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: неизвестный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**Имфаттрибутес:: Сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Объекты активации](activation-objects.md)
</dt> </dl>

 

 




