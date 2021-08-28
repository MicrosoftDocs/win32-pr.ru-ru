---
description: Смещение между временем презентации и метками времени источников мультимедиа.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: Атрибут MF_EVENT_PRESENTATION_TIME_OFFSET (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5ff2285bc624d42f17d4662cf93e3f46a65fcbef465e731874ef255c40c076d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013084"
---
# <a name="mf_event_presentation_time_offset-attribute"></a>\_ \_ \_ Атрибут смещения времени представления событий MF \_

Смещение между временем презентации и штампами времени источника мультимедиа.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Remarks

Смещение вычисляется следующим образом: offset = время представления – источник время. Этот атрибут используется со следующими событиями:

-   [месессионнотифипресентатионтиме](mesessionnotifypresentationtime.md)
-   [месессионстартед](mesessionstarted.md)

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

[**Имфаттрибутес:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




