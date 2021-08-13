---
title: Код уведомления TVN_GETINFOTIP (Коммктрл. h)
description: Посылается элементом управления "представление дерева", имеющим стиль подсказки "ТЕЛЕВИЗОРы" \_ . Этот код уведомления отправляется, когда элемент управления запрашивает дополнительную текстовую информацию для отображения в подсказке. Код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5129e1fa97397cfa9c037c7c65099ee3bd961f184b1bf9b43d2dc87e35880f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261164"
---
# <a name="tvn_getinfotip-notification-code"></a>\_Код уведомления ТВН жетинфотип

Посылается элементом управления "представление дерева", имеющим стиль [**\_ подсказки "телевизоры**](tree-view-control-window-styles.md) ". Этот код уведомления отправляется, когда элемент управления запрашивает дополнительную текстовую информацию для отображения в подсказке. Код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтвжетинфотип**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) , содержащую сведения об этом коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Элемент управления игнорирует возвращаемое значение для этого кода уведомления.

## <a name="remarks"></a>Remarks

Этот код уведомления отправляется только элементами управления "дерево", имеющим стиль [**\_ подсказки для телевизоров**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ЖЕТИНФОТИПВ** (Юникод) и **ТВН \_ жетинфотипа** (ANSI)<br/>             |



 

 





