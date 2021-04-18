---
description: Сигнализирует, что изменилось число кнопок в меню DVD, или что кнопка была изменена.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652128"
---
# <a name="ec_dvd_button_change"></a>\_ \_ изменение кнопки DVD \_ EC

Сигнализирует, что изменилось число кнопок в меню DVD, или что кнопка была изменена.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение **типа DWORD** , указывающее количество доступных кнопок.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Значение **типа DWORD** , указывающее номер выбранного в данный момент кнопки. Номер выбранной кнопки ноль означает, что кнопка не выбрана.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Номера кнопок находятся в диапазоне от 1 до 36.

Выбранная в данный момент кнопка может изменяться автоматически при помощи команды навигации, созданной на диске, а также через Управление приложениями с помощью интерфейса [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .

Это событие может подать сигнал любому из доступных номеров кнопок. Эти числа не всегда соответствуют номерам кнопок, используемых для [**IDvdControl2:: селектандактиватебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) , так как этот метод может активировать только подмножество кнопок.

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

 

 




