---
description: Отправляется при изменении текущего набора заголовков видео (ВТС).
ms.assetid: 7b8849c8-c71e-44d6-b33a-8e80247bdb22
title: EC_DVD_TITLE_SET_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_SET_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a2e6c1dcc60b0b0ef74e40f235ba0b3d16b4288e0225e0ca92270d2d03f3ccd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965554"
---
# <a name="ec_dvd_title_set_change"></a>\_ \_ изменение набора заголовков DVD EC \_ \_

Отправляется при изменении текущего набора заголовков видео (ВТС).

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Номер нового набора заголовков видео (ВТСН).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="remarks"></a>Remarks

По умолчанию это событие отключено. Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ нотифипоситиончанже DVD** значение **true**.

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

 

 




