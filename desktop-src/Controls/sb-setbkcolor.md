---
title: Сообщение SB_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона в строке состояния.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- Элементы управления Windows для SB_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415940"
---
# <a name="sb_setbkcolor-message"></a>\_Сообщение SB сетбкколор

Задает цвет фона в строке состояния.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение [**COLORREF**](/windows/desktop/gdi/colorref) , указывающее новый цвет фона. Укажите \_ значение по умолчанию CLR, чтобы строка состояния использовала цвет фона по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущий цвет фона или \_ значение по умолчанию CLR, если цвет фона является цветом по умолчанию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

