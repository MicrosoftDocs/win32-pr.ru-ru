---
description: Содержит время начала, с которого источник мультимедиа перезапускается с текущей позиции.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Атрибут MF_EVENT_SOURCE_ACTUAL_START (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ce39e8a9f90ad0cd7f0cbd590b32719ab10dbd8e498c396e86772ce333e94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104840"
---
# <a name="mf_event_source_actual_start-attribute"></a>\_Атрибут "источник события MF — \_ \_ фактическое \_ Начало"

Содержит время начала, с которого источник мультимедиа перезапускается с текущей позиции.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="remarks"></a>Remarks

Этот атрибут используется с событием [месаурцестартед](mesourcestarted.md) . Атрибут имеет значение, если данные события пусты (**VT \_ Empty**), что указывает на то, что источник мультимедиа запущен из текущей позицией воспроизведения. В этом случае в атрибуте **\_ \_ \_ \_ Start источника события MF** указан фактическое время начала. Если данные события имеют значение **VT \_ Empty** и этот атрибут не задан, то время начала считается равным нулю.

Если данные о событии [месаурцестартед](mesourcestarted.md) содержат время начала (**VT \_ i8**), этот атрибут задавать не следует.

Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
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

 

 




