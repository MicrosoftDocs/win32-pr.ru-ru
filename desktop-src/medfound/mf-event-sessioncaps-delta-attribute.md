---
description: Содержит флаги, указывающие, какие возможности были изменены в сеансе мультимедиа на основе текущей презентации.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Атрибут MF_EVENT_SESSIONCAPS_DELTA (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e227e5608296a9b30fa2fc68f37215d687349516367d8689b20825e1ed4e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714846"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>\_ \_ \_ Разностный атрибут сессионкапс события MF

Содержит флаги, указывающие, какие возможности были изменены в сеансе мультимедиа на основе текущей презентации.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут содержит битовую маску, указывающую, какие флаги возможностей изменились. Список возможных флагов см. в разделе [**имфмедиасессион:: жетсессионкапабилитиес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Биты имеют значение 1 в битовой маске по любой из следующих причин:

-   Соответствующий бит для возможностей изменился с 0 на 1.
-   Соответствующий бит возможностей изменился с 1 на 0.
-   Соответствующий бит остался 1, но подробные сведения об этой возможности изменились. Например, изменена максимальная скорость воспроизведения.

Этот атрибут используется с событием [месессионкапабилитиесчанжед](mesessioncapabilitieschanged.md) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты событий](event-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




