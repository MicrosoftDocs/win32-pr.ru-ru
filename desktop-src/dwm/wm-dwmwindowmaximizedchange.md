---
title: Сообщение WM_DWMWINDOWMAXIMIZEDCHANGE (Winuser. h)
description: Посылается, когда развернутое окно диспетчер окон рабочего стола (DWM) развернуто.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- Сообщение WM_DWMWINDOWMAXIMIZEDCHANGE диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415608"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a>\_Сообщение ДВМВИНДОВМАКСИМИЗЕДЧАНЖЕ WM

Посылается, когда развернутое окно диспетчер окон рабочего стола (DWM) развернуто.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Задайте значение true, чтобы указать, что окно развернуто.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

