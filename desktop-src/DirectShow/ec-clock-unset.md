---
description: Поставщик часов был отключен.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ead35d89eee94bbffb38a96f658ccb2bb6e6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675572"
---
# <a name="ec_clock_unset"></a>неопределенное \_ время EC \_

Поставщик часов был отключен.

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

## <a name="default-action"></a>Действие по умолчанию

Диспетчер графов фильтров выбирает новый эталонный таймер при следующей приостановке или выполнении команды. Он также перенаправляет событие в приложение.

## <a name="remarks"></a>Комментарии

Кспрокси сигнализирует об этом событии, когда закрепление фильтра, предоставляющего часы, отключено.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




