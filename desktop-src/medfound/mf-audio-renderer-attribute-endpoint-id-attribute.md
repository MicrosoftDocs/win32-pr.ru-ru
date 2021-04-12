---
description: Указывает идентификатор для устройства конечной точки аудио.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: Атрибут MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344595"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>\_ \_ \_ \_ Атрибут идентификатора конечной точки атрибута для модуля подготовки звука MF \_

Указывает идентификатор для устройства конечной точки аудио.

## <a name="data-type"></a>Тип данных

Строка расширенных символов

## <a name="remarks"></a>Комментарии

Этот атрибут можно использовать для настройки модуля подготовки звука. Использование зависит от того, какая функция вызывается для создания модуля подготовки звука:

-   [**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Задайте этот атрибут с помощью указателя интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , указанного в параметре *паудиоаттрибутес* .
-   [**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Задайте этот атрибут с помощью указателя интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного в параметре *ппактивате* . Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Устройство конечной точки аудио — это аппаратное устройство, которое использует один конец пути к звуковым данным, например наушники или динамик. Чтобы получить идентификатор конечной точки аудио, используйте следующие основные API аудио:

-   Используйте интерфейс [**иммдевицеенумератор**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) для перечисления устройств в системе.
-   Вызовите [**иммдевице:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , чтобы получить идентификатор для устройства.

Дополнительные сведения см. в документации по [основным аудио](../coreaudio/core-audio-apis-in-windows-vista.md) API. Если этот атрибут не задан, модуль подготовки звука использует устройство конечной точки по умолчанию.

Если этот атрибут задан, не устанавливайте атрибут [**\_ \_ \_ \_ \_ роли конечной точки для атрибута «модуль подготовки звука MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) ». Если заданы оба атрибута, то при создании модуля подготовки звука произойдет сбой.

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

[**Имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[Потоковая прорисовка звука](streaming-audio-renderer.md)
</dt> </dl>

 

 
