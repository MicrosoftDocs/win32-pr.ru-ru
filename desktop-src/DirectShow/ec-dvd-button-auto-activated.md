---
description: Сигнализирует о том, что кнопка меню DVD была автоматически активирована для каждой инструкции на диске. Это происходит, когда время ожидания меню истекло, а на диске указана автоматическая активация кнопки.
ms.assetid: ecd79c2a-1717-473d-b111-2b1db2ca4cc1
title: EC_DVD_BUTTON_AUTO_ACTIVATED (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_AUTO_ACTIVATED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cc018630d7a994c01b81adea4b4cf567666a76625b4b3b13fbf4118b8e8a1fd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965894"
---
# <a name="ec_dvd_button_auto_activated"></a>\_ \_ \_ Автоматическая \_ Активация кнопки DVD в EC

Сигнализирует о том, что кнопка меню DVD была автоматически активирована для каждой инструкции на диске. Это происходит, когда время ожидания меню истекло, а на диске указана автоматическая активация кнопки.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение **типа DWORD** , указывающее на активированную кнопку.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

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

 

 




