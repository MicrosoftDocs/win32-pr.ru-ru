---
description: Состояние графа фильтра изменилось.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2b476c923f0b812196a5697444433ea0be65b8d3f46bd0388261b2a67a66881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905734"
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
> Это событие может возникать при завершении работы графа. если вы переопределите действие по умолчанию и прослушиваете это событие, необходимо быть особенно осторожным, чтобы не обрабатывать события после выпуска Graph диспетчера фильтров. В противном случае приложение может ссылаться на недопустимый указатель [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) и на сбой. Дополнительные сведения см. [в разделе реагирование на события](responding-to-events.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




