---
description: Смещение между временем презентации и метками времени источников мультимедиа.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: Атрибут MF_EVENT_PRESENTATION_TIME_OFFSET (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897726"
---
# <a name="mf_event_presentation_time_offset-attribute"></a>\_ \_ \_ Атрибут смещения времени представления событий MF \_

Смещение между временем презентации и штампами времени источника мультимедиа.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Комментарии

Смещение вычисляется следующим образом: offset = время представления – источник время. Этот атрибут используется со следующими событиями:

-   [месессионнотифипресентатионтиме](mesessionnotifypresentationtime.md)
-   [месессионстартед](mesessionstarted.md)

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

[**Имфаттрибутес:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




