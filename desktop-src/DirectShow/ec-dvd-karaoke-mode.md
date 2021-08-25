---
description: Указывает, что Навигатор DVD начал играть или завершил воспроизведение данных караоке.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4edbdb337c4b57a7ed09bd63a8ed4fb0d1946b289b369badab64b561000d3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928574"
---
# <a name="ec_dvd_karaoke_mode"></a>\_режим Караоке на DVD-диске EC \_ \_

Указывает, что [Навигатор DVD](data-flow-in-the-dvd-navigator.md) начал играть или завершил воспроизведение данных караоке.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

. Если задано **значение true**, проигрываться запись караоке. В противном случае запись караоке не будет воспроизводиться.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="remarks"></a>Remarks

Проигрыватель DVD сигнализирует об этом событии при каждом изменении доменов.

Это событие возникает во всех доменах DVD.

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

 

 




