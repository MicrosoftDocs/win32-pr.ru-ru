---
title: Сообщение WM_DWMNCRENDERINGCHANGED (Winuser. h)
description: Посылается, когда изменилась политика отрисовки области, не являющейся клиентской.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- Сообщение WM_DWMNCRENDERINGCHANGED диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcae8595315d43737d88d6a302bcac3a328418abd19d77b96bd13ee5ef66496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502657"
---
# <a name="wm_dwmncrenderingchanged-message"></a>\_Сообщение ДВМНКРЕНДЕРИНГЧАНЖЕД WM

Посылается, когда изменилась политика отрисовки области, не являющейся клиентской.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, включена ли визуализация DWM для области окна, не являющейся клиентской. **Значение true** , если включено; в противном случае — **значение false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

Функции [**двмжетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) и [**двмсетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) используются для получения или задания политики отрисовки без клиента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

