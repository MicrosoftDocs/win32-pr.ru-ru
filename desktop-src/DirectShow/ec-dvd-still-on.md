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
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651676"
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

## <a name="remarks"></a>Комментарии

Все сочетания кнопок и по-прежнему возможны (кнопки со всеми по-прежнему включены, кнопки с по-прежнему отключены, кнопка отключена, кнопка выключена.

Это событие возникает во всех доменах.

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

 

 




