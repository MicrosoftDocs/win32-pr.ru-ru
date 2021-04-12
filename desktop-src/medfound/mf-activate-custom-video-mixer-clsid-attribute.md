---
description: Идентификатор CLSID пользовательского видеомикшера для приемника расширенного модуля подготовки видео (Евр).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343945"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a>MF \_ активировать \_ Пользовательский \_ \_ атрибут CLSID микшера видео \_

Идентификатор CLSID пользовательского видеомикшера для приемника расширенного модуля подготовки видео (Евр).

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

При создании Евр с помощью объекта активации этот атрибут можно использовать для установки пользовательского видеомикшера на Евр. Используйте этот атрибут, как показано ниже.

1.  Вызовите функцию [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) , чтобы создать объект активации для Евр. Функция возвращает указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

2.  Задайте этот аттрибуе в указателе [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , вызвав [**Имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). Значение атрибута является идентификатором CLSID пользовательского видеомикшера приложения.

Если этот атрибут задан, ЕВР вызывает **CoCreateInstance** с указанным идентификатором CLSID для создания пользовательского видеомикшера. Видеомикшер должен предоставлять интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Микшер создается как внутрипроцессный COM-сервер.

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

[**Имфаттрибутес:: a GUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Имфаттрибутес:: Сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Объекты активации](activation-objects.md)
</dt> </dl>

 

 




