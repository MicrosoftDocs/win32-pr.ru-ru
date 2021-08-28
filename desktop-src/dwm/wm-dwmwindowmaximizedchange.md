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
ms.openlocfilehash: 93cfa4ac380b6ff439fb2bf4805846c0b774a90bcfdcd83673ead2334a3c7094
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117754"
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

## <a name="remarks"></a>Remarks

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

