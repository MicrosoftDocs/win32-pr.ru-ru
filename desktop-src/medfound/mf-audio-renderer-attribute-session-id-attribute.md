---
description: Указывает класс политики аудио для модуля подготовки звука.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: Атрибут MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911424"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a>\_ \_ \_ \_ Атрибут идентификатора сеанса атрибута для обработчика звука MF \_

Указывает класс политики аудио для модуля подготовки звука.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Этот атрибут связывает модуль подготовки звука с классом политики аудио. Каждый класс политики имеет свой собственный том и элемент управления политикой. Если этот атрибут не задан, новое приложение будет соединено с звуковым сеансом приложения по умолчанию. Дополнительные сведения см. в разделе [**иаудиоклиент:: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) в основной документации по API аудио.

Этот атрибут можно использовать для настройки модуля подготовки звука. Использование зависит от того, какая функция вызывается для создания модуля подготовки звука:

-   [**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Задайте этот атрибут с помощью указателя интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , указанного в параметре *паудиоаттрибутес* .
-   [**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Задайте этот атрибут с помощью указателя интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного в параметре *ппактивате* . Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

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

[Атрибуты модуля подготовки звука](audio-renderer-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: a GUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Имфаттрибутес:: Сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Потоковая прорисовка звука](streaming-audio-renderer.md)
</dt> </dl>

 

 
