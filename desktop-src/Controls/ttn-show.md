---
title: Код уведомления TTN_SHOW (Коммктрл. h)
description: Сообщает окну-владельцу, что элемент управления ToolTip будет отображаться. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988723"
---
# <a name="ttn_show-notification-code"></a>ТТН \_ отобразить код уведомления

Сообщает окну-владельцу, что элемент управления ToolTip будет отображаться. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

[Версия 4,70](common-control-versions.md). Чтобы отобразить подсказку в расположении по умолчанию, возвратите ноль. Чтобы настроить расположение подсказки, переместите окно подсказки с помощью функции [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) и возвратите **значение true**.

> [!Note]  
> Для версий более ранних, чем 4,70, возвращаемое значение отсутствует.

 

## <a name="remarks"></a>Комментарии

Прямоугольник окна подсказки немного больше, чем его отображаемый прямоугольник, и его происхождение смещается вверх и влево. Если нужно точно разместить текстовую рамку подсказки, сообщение [**ТТМ \_ аджустрект**](ttm-adjustrect.md) преобразует текстовый прямоугольник в соответствующий прямоугольник окна подсказки и наоборот.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

