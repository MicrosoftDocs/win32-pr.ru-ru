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
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988737"
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

## <a name="remarks"></a>Комментарии

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

Функции [**двмжетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) и [**двмсетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) используются для получения или задания политики отрисовки без клиента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

