---
description: Сигнализирует, что диск DVD был извлечен.
ms.assetid: 031156c2-f0f0-4a9e-b792-4d656ec49aef
title: EC_DVD_DISC_EJECTED (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_EJECTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: ab6c1333245b589d4f13bafcba89eada3ef98ab0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651855"
---
# <a name="ec_dvd_disc_ejected"></a>\_DVD- \_ диск EC \_ извлечен

Сигнализирует, что диск DVD был извлечен.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ноль.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Воспроизведение автоматически останавливается при извлечении диска. Приложению не нужно предпринимать никаких специальных действий в ответ на это событие.

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

 

 




