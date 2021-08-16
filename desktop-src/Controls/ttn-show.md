---
title: Код уведомления TTN_SHOW (Коммктрл. h)
description: Сообщает окну-владельцу, что элемент управления ToolTip будет отображаться. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW кода уведомления Windows элементы управления
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
ms.openlocfilehash: 74397223f20668487e78cea15e2e1507026ee65089e5011065b3f177514e899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408816"
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

 

## <a name="remarks"></a>Remarks

Прямоугольник окна подсказки немного больше, чем его отображаемый прямоугольник, и его происхождение смещается вверх и влево. Если нужно точно разместить текстовую рамку подсказки, сообщение [**ТТМ \_ аджустрект**](ttm-adjustrect.md) преобразует текстовый прямоугольник в соответствующий прямоугольник окна подсказки и наоборот.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

