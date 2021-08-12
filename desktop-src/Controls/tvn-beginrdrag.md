---
title: Код уведомления TVN_BEGINRDRAG (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления об инициации операции перетаскивания, включающей правую кнопку мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7ce3fb92f39097c51cf54d707fac4341bc2a4c098b5abb0b36abcbd47f5744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669178"
---
# <a name="tvn_beginrdrag-notification-code"></a>\_Код уведомления ТВН бегинрдраг

Сообщает родительскому окну элемента управления иерархического представления об инициации операции перетаскивания, включающей правую кнопку мыши. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Элемент **итемнев** — это структура [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , которая содержит допустимые сведения в членах **хитем**, **State** и **lParam** о перемещенном элементе. Элемент **птдраг** указывает текущие экранные координаты мыши.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ БЕГИНРДРАГВ** (Юникод) и **ТВН \_ бегинрдрага** (ANSI)<br/>             |



 

 





