---
title: Сообщение WM_DPICHANGED_AFTERPARENT (Winuser. h)
description: Для окон верхнего уровня на мониторе версии 2 это сообщение отправляется во все HWND в дочернем дереве ХВДН окна, которое является изменением DPI. | Сообщение WM_DPICHANGED_AFTERPARENT (Winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT высокое разрешение для сообщения
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684960"
---
# <a name="wm_dpichanged_afterparent-message"></a>\_Сообщение WM DPICHANGED \_ афтерпарент

Для окон верхнего уровня [на мониторе версии 2](dpi-awareness-context.md) это сообщение отправляется во все HWND в дочернем дереве хвдн окна, которое является изменением dpi. Это сообщение появляется после того, как окно верхнего уровня получает [**WM \_ DPICHANGED**](wm-dpichanged.md)и перебирает дочернее дерево сверху вниз.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Это значение не используется и будет равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Это значение не используется и будет равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это значение не используется и игнорируется системой.

## <a name="remarks"></a>Комментарии

Обработка этого сообщения по умолчанию в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca)отсутствует.

Это сообщение отправляется только в том случае, если окно верхнего уровня имеет контекст с отслеживанием DPI для PMv2.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**WM \_ DPICHANGED**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ DPICHANGED \_ бефорепарент**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

