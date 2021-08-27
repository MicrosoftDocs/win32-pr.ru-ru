---
description: Отправляется при изменении значения регистра общего параметра (ГПРМ).
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: b1d6613475a3c61640a7b6b5f5c53bc1baab52c1a69ec3d3c8b7a0e32f91928c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079154"
---
# <a name="ec_dvd_gprm_change"></a>\_Изменение гпрм DVD-диска EC \_ \_

Отправляется при изменении значения регистра общего параметра (ГПРМ).

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Отсчитываемый от нуля индекс измененного значения ГПРМ.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Младшие 16 разрядов содержат новое значение ГПРМ.

</dd> </dl>

## <a name="remarks"></a>Remarks

По умолчанию это событие отключено. Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ енаблелоггинжевентс DVD** значение **true**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Двдевкоде. h (включение DShow. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> <dt>

[Коды уведомлений о событиях DVD](dvd-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[**IDvdInfo2:: Жеталлгпрмс**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 




