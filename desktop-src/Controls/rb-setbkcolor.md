---
title: Сообщение RB_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона элемента управления главной панели по умолчанию.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- Элементы управления Windows для RB_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654541"
---
# <a name="rb_setbkcolor-message"></a>\_Сообщение СЕТБККОЛОР RB

Задает цвет фона элемента управления главной панели по умолчанию.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее новый цвет фона по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее предыдущий цвет фона по умолчанию.

## <a name="remarks"></a>Комментарии

Цвет фона по умолчанию элемента управления главной панели используется для рисования фона в элементе управления главной панели и всех полос, добавленных после отправки сообщения. Цвет фона по умолчанию для определенного диапазона можно переопределить при добавлении или изменении диапазона, установив \_ флаг рббим Colors в **фмаск** и установив **клрбакк** в структуре [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

Если стили оформления включены, это сообщение не действует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТБККОЛОР RB**](rb-getbkcolor.md)
</dt> </dl>

 

