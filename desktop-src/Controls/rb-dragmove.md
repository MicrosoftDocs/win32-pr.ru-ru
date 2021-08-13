---
title: Сообщение RB_DRAGMOVE (Коммктрл. h)
description: Обновляет расположение перетаскивания в элементе управления главной панели после предыдущего \_ сообщения RB бегиндраг.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- элементы управления Windows сообщений RB_DRAGMOVE
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a511bd1ad13442489f3f6dbf3de1b897b30e54f9d503b30b9031426b0aedcef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409726"
---
# <a name="rb_dragmove-message"></a>\_Сообщение ДРАГМОВЕ RB

Обновляет расположение перетаскивания в элементе управления главной панели после предыдущего сообщения [**RB \_ бегиндраг**](rb-begindrag.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение **типа DWORD** , содержащее новые координаты мыши. Горизонтальная координата содержится в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) , а вертикальная координата содержится в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Если передать (DWORD) значение 1, элемент управления "Главная панель" будет использовать расположение мыши во время последнего потока элемента управления [**с именем "**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage)".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_ЕНДДРАГ RB**](rb-enddrag.md)
</dt> </dl>

 

