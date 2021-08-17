---
description: Указывает, выполняется ли воспроизведение блока угла и могут быть выполнены изменения угла.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e95c692aed8ac6c709ff0db1d6056fc59219fa73f5aa2e4cfb9b31b2c1a03d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015992"
---
# <a name="ec_dvd_angles_available"></a>\_Доступные углы для DVD-диска EC \_ \_

Указывает, выполняется ли воспроизведение блока угла и могут быть выполнены изменения угла.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Логическое значение (**bool**), указывающее, выполняется ли воспроизведение блока угла. Ноль (0) означает, что воспроизведение не находится в блоке угла, а углы недоступны, один (1) указывает, что выполняется воспроизведение блока угла и можно выполнить изменения угла.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="remarks"></a>Remarks

Изменения угла не ограничиваются блоками углов, а возможность изменения угла может быть видна только в блоке угла.

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

 

 




