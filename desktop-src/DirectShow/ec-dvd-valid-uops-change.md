---
description: Сигнализирует, что доступный набор методов интерфейса IDvdControl2 изменился.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fafdbb5443a32a8029ad73d92a2b23c5f05c96d5dfc32375fd05e6d4502484a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051814"
---
# <a name="ec_dvd_valid_uops_change"></a>\_ \_ изменение УОПС допустимого DVD-диска EC \_ \_

Сигнализирует, что доступный набор методов интерфейса [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) изменился.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение **типа DWORD** , содержащее сочетание одного или нескольких флагов из [**допустимого \_ перечисления \_ флагов УОП**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) . Биты указывают, какие команды [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) были явно отключены DVD-диском.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это событие указывает только, какие операции явно отключены содержимым на DVD-диске. Он не гарантирует, что он может вызывать методы, которые не были отключены. Например, если нет кнопок, метод [**IDvdControl2:: активатебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) не будет работать, даже если метод явно не отключен.

Это событие возникает во всех доменах.

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
</dt> </dl>

 

 




