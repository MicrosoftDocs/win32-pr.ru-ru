---
description: Указывает роль конечной точки аудио для модуля подготовки звука.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: Атрибут MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998854"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a>\_ \_ \_ \_ Атрибут роли конечной точки для атрибута для обработчика звука MF \_

Указывает роль конечной точки аудио для модуля подготовки звука.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут можно использовать для настройки модуля подготовки звука. Использование зависит от того, какая функция вызывается для создания модуля подготовки звука:

-   [**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Задайте этот атрибут с помощью указателя интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , указанного в параметре *паудиоаттрибутес* .
-   [**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Задайте этот атрибут с помощью указателя интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного в параметре *ппактивате* . Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Устройство конечной точки аудио — это аппаратное устройство, которое использует один конец пути к звуковым данным, например наушники или динамик.

Если этот атрибут задан, модуль подготовки звука использует для указанной роли звуковое устройство по умолчанию. Значение этого атрибута является членом перечисления **ероле** , который определен в файле заголовка ммдевицеапи. h. Дополнительные сведения см. в документации по основным аудио API. Если этот атрибут не задан, модуль подготовки звука использует устройство конечной точки по умолчанию.

Если этот атрибут задан, не задавайте атрибут [**\_ \_ \_ \_ \_ ID конечной точки атрибута «модуль подготовки звука MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) ». Если заданы оба атрибута, то при создании модуля подготовки звука произойдет сбой.

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

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Потоковая прорисовка звука](streaming-audio-renderer.md)
</dt> </dl>

 

 




