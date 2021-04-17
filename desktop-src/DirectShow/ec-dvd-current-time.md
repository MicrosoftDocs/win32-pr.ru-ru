---
description: Сигнализирует о начале каждой единицы видеообъекта (ВОБУ) — сегмента видео, 0,4 – 1,0 секунд в длину.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651856"
---
# <a name="ec_dvd_current_time"></a>\_ \_ Текущее время на DVD-диске EC \_

Сигнализирует о начале каждой единицы видеообъекта (ВОБУ) — сегмента видео, 0,4 – 1,0 секунд в длину.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение **типа DWORD** , указывающее время текущего времени воспроизведения в формате двоично-кодированных десятичных значений (BCD) часов, минут, секунд, кадров (чч: мм: СС: FF). Элемент структуры времени в формате [**DVD \_**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Логическое значение (**bool**), указывающее временной код. Ноль (0) указывает 25 кадров в секунду, а 1 — 30 кадров в секунду (не отброшенных). Значение 2 указывает, что время воспроизведения не может быть определено.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это событие сигнализирует только простым линейным роликам.

Это событие возникает в домене Title.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Двдевкоде. h (включение DShow. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> <dt>

[Коды уведомлений о событиях DVD](dvd-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




