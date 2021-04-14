---
description: Содержит флаги, указывающие, какие возможности были изменены в сеансе мультимедиа на основе текущей презентации.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Атрибут MF_EVENT_SESSIONCAPS_DELTA (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423801"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>\_ \_ \_ Разностный атрибут сессионкапс события MF

Содержит флаги, указывающие, какие возможности были изменены в сеансе мультимедиа на основе текущей презентации.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут содержит битовую маску, указывающую, какие флаги возможностей изменились. Список возможных флагов см. в разделе [**имфмедиасессион:: жетсессионкапабилитиес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Биты имеют значение 1 в битовой маске по любой из следующих причин:

-   Соответствующий бит для возможностей изменился с 0 на 1.
-   Соответствующий бит возможностей изменился с 1 на 0.
-   Соответствующий бит остался 1, но подробные сведения об этой возможности изменились. Например, изменена максимальная скорость воспроизведения.

Этот атрибут используется с событием [месессионкапабилитиесчанжед](mesessioncapabilitieschanged.md) .

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

[Атрибуты событий](event-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




