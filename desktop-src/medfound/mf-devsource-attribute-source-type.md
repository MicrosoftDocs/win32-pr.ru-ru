---
description: Указывает тип устройств, например запись звука или запись видео.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1160242b32ce6b6b902d1575cba4d275388a38b980d69a0bad0a528f377085d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060688"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a>\_ \_ \_ Атрибут типа источника атрибута MF девсаурце \_

Указывает тип устройства, например запись звука или запись видео.

## <a name="data-type"></a>Тип данных

**GUID**

Для этого атрибута определены следующие значения:



| Значение                                                                                                                                                                                                                                                                 | Значение                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <dt>**\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ аудкап \_ GUID**</dt> </dl> | Устройство для записи звука.<br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <dt>**\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ GUID**</dt> </dl> | Устройство видеозаписи.<br/> |



 

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Remarks

Используйте этот атрибут в качестве входных данных для следующих функций:

-   [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Кроме того, этот атрибут задается для объектов активации, возвращаемых функцией [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Захват аудио- и видеоданных](audio-video-capture.md)
</dt> <dt>

[Запись атрибутов устройства](capture-device-attributes.md)
</dt> </dl>

 

 




