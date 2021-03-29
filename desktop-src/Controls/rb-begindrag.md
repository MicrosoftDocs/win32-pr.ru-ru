---
title: Сообщение RB_BEGINDRAG (Коммктрл. h)
description: Помещает элемент управления главной панели в режим перетаскивания. Это сообщение не приводит к \_ отправке уведомления РБН бегиндраг.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- Элементы управления Windows для RB_BEGINDRAG сообщений
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491781"
---
# <a name="rb_begindrag-message"></a>\_Сообщение БЕГИНДРАГ RB

Помещает элемент управления главной панели в режим перетаскивания. Это сообщение не приводит к отправке уведомления [РБН \_ бегиндраг](rbn-begindrag.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс диапазона, на который будет влиять операция перетаскивания.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение **типа DWORD** , содержащее начальные координаты мыши. Горизонтальная координата содержится в ЛОВОРД, а вертикальная координата содержится в HIWORD. Если передать (**DWORD**) значение 1, элемент управления "Главная панель" будет использовать расположение мыши во время последнего потока элемента управления [**с именем "**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="remarks"></a>Комментарии

Сообщения **RB \_ бегиндраг**, [**RB \_ драгмове**](rb-dragmove.md)и [**RB \_ енддраг**](rb-enddrag.md) позволяют реализовать интерфейс [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) для элемента управления "Главная панель". Вы отправляете **сообщение \_ RB бегиндраг** в ответ на [**интерфейс IDropTarget::D ражентер**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), отправляете сообщение **RB \_ Драгмове** в ответ на [**интерфейс IDropTarget::D Раговер**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), а сообщение **RB \_ Енддраг** в ответ на [**интерфейс IDropTarget::D верхнем**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) и [**интерфейс IDropTarget::D раглеаве**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

