---
description: Приблизительное время, когда сеанс мультимедиа вызвал событие.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: Атрибут MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712398"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a>\_ \_ \_ \_ Атрибут времени возникновения события MF Session примерно \_

Приблизительное время, когда сеанс мультимедиа вызвал событие.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="remarks"></a>Комментарии

Некоторые события из сеанса мультимедиа имеют этот атрибут. Значение дает приблизительное время показа при возникновении события.

Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.

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

 

 




