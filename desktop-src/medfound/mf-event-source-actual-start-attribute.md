---
description: Содержит время начала, с которого источник мультимедиа перезапускается с текущей позиции.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Атрибут MF_EVENT_SOURCE_ACTUAL_START (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423825"
---
# <a name="mf_event_source_actual_start-attribute"></a>\_Атрибут "источник события MF — \_ \_ фактическое \_ Начало"

Содержит время начала, с которого источник мультимедиа перезапускается с текущей позиции.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="remarks"></a>Комментарии

Этот атрибут используется с событием [месаурцестартед](mesourcestarted.md) . Атрибут имеет значение, если данные события пусты (**VT \_ Empty**), что указывает на то, что источник мультимедиа запущен из текущей позицией воспроизведения. В этом случае в атрибуте **\_ \_ \_ \_ Start источника события MF** указан фактическое время начала. Если данные события имеют значение **VT \_ Empty** и этот атрибут не задан, то время начала считается равным нулю.

Если данные о событии [месаурцестартед](mesourcestarted.md) содержат время начала (**VT \_ i8**), этот атрибут задавать не следует.

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

 

 




