---
title: Сообщение LVN_ODFINDITEM (Коммктрл. h)
description: Отправляется виртуальным элементом управления "представление списка", когда ему требуется владелец для поиска конкретного элемента обратного вызова.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- Элементы управления Windows для LVN_ODFINDITEM сообщений
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136654"
---
# <a name="lvn_odfinditem-message"></a>\_Сообщение ЛВН одфиндитем

Отправляется виртуальным элементом управления " [представление списка](list-view-controls-overview.md) ", когда ему требуется владелец для поиска конкретного элемента обратного вызова. Например, элемент управления будет отсылать этот код уведомления при получении сочетания клавиш для ввода с клавиатуры или при получении сообщения [**LVM \_ FINDITEM**](lvm-finditem.md) . \_Код уведомления ЛВН одфиндитем отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) , которая содержит сведения, используемые для поиска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс найденного элемента или значение-1, если элемент не найден.

## <a name="remarks"></a>Комментарии

Данные поиска отправляются в виде структуры [**лвфиндинфо**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , которая является членом структуры [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ЛВН \_ ОДФИНДИТЕМВ** (Юникод) и **ЛВН \_ одфиндитема** (ANSI)<br/>             |



 

 





