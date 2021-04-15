---
title: Код уведомления BCN_DROPDOWN (Winuser. h)
description: Посылается, когда пользователь щелкает стрелку раскрывающегося списка на кнопке. Родительское окно элемента управления получает этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654471"
---
# <a name="bcn_dropdown-notification-code"></a>\_Код уведомления для раскрывающегося списка BCN

Посылается, когда пользователь щелкает стрелку раскрывающегося списка на кнопке. Родительское окно элемента управления получает этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмбкдропдовн**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . Для элемента **ркбуттон** задано описание раскрывающегося области.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Получатель уведомлений выполняет приведение **lParam** для получения структуры [**нмбкдропдовн**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . **WParam** содержит идентификатор элемента управления, который отправляет это сообщение. Элемент управления "Кнопка" должен иметь стиль кнопки раскрывающегося списка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



 

 





