---
description: Сообщает о состоянии ошибки DVD.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c0afa9ce750016001ddbe054d8cb9a589a2c68d8856e8e4db5c59043eb881129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820531"
---
# <a name="ec_dvd_error"></a>\_Ошибка на DVD-диске EC \_

Сообщает о состоянии ошибки DVD.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение **типа DWORD** , указывающее на состояние ошибки. Член перечисленного типа данных " [**\_ Ошибка DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) ".

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Значение зависит от значения *lParam1*. Дополнительные сведения см. в разделе [**\_ об ошибках DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .

</dd> </dl>

## <a name="remarks"></a>Remarks

Это событие возникает во всех доменах.

## <a name="requirements"></a>Requirements (Требования)



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

 

 




