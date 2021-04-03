---
title: Код уведомления CBEN_DRAGBEGIN (Коммктрл. h)
description: Посылается, когда пользователь начинает перетаскивать изображение элемента, отображаемого в области редактирования элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137283"
---
# <a name="cben_dragbegin-notification-code"></a>\_Код уведомления кбен драгбегин

Посылается, когда пользователь начинает перетаскивать изображение элемента, отображаемого в области редактирования элемента управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмкбедрагбегин**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) , содержащую сведения о коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Комментарии

Если принимающее приложение реализует функцию перетаскивания из элемента управления, приложение начнет операцию перетаскивания в ответ на этот код уведомления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Кбен \_ ДРАГБЕГИНВ** (Юникод) и **кбен \_ драгбегина** (ANSI)<br/>             |



 

 





