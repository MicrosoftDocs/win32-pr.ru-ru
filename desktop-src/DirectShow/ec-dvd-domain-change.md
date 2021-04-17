---
description: Указывает новый домен проигрывателя DVD.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 815b6b2dd318d0b7716f4cf640ef3f83dacd0d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651772"
---
# <a name="ec_dvd_domain_change"></a>\_изменение домена на DVD-диске EC \_ \_

Указывает новый домен проигрывателя DVD.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение **типа DWORD** , указывающее новый домен. Член типа данных "перечислимый [**\_ домен DVD-диска**](/windows/win32/api/strmif/ne-strmif-dvd_domain) ".

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Проигрыватель DVD сигнализирует об этом событии при каждом изменении доменов.

Это событие возникает во всех доменах DVD.

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

 

 




