---
description: Состояние графа фильтра изменилось.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685439"
---
# <a name="ec_state_change"></a>\_изменение состояния \_ EC

Состояние графа фильтра изменилось.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Член перечисляемого [**типа \_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) , указывающий новое состояние диаграммы.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет действия по умолчанию. Событие не отправляется в приложение.

> [!Note]  
> Это событие может возникать при завершении работы графа. Если вы Переопределите действие по умолчанию и прослушиваете это событие, необходимо быть особенно осторожным, чтобы не обрабатывать события после выпуска диспетчера графа фильтров. В противном случае приложение может ссылаться на недопустимый указатель [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) и на сбой. Дополнительные сведения см. [в разделе реагирование на события](responding-to-events.md).

 

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

 

 




