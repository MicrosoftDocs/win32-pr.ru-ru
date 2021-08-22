---
description: Сигнализирует началу все еще (PGC, Cell или ВОБУ).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 801db7f1e14002aa6333b18349e259e40928a0cd45958c0e1aa618d1d1143be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119303334"
---
# <a name="ec_dvd_still_on"></a>\_ \_ все еще на DVD-диске EC \_

Сигнализирует началу все еще (PGC, Cell или ВОБУ).

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Логическое значение (**bool**), указывающее, доступны ли кнопки. Ноль (0) означает, что кнопки доступны, поэтому метод [**IDvdControl2:: стиллофф**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) не будет работать. Один (1) означает, что кнопки недоступны, поэтому **IDvdControl2:: стиллофф** будет работать.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Значение **типа DWORD** , указывающее время в секундах, по истечении которого будет выполняться последнее. значение 0xFFFFFFFF указывает на бесконечность. Это означает Ожидание нажатия пользователем кнопки или до тех пор, пока приложение не вызовет [**IDvdControl2:: стиллофф**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).

</dd> </dl>

## <a name="remarks"></a>Remarks

Все сочетания кнопок и по-прежнему возможны (кнопки со всеми по-прежнему включены, кнопки с по-прежнему отключены, кнопка отключена, кнопка выключена.

Это событие возникает во всех доменах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Двдевкоде. h (включение DShow. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> <dt>

[Коды уведомлений о событиях DVD](dvd-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




