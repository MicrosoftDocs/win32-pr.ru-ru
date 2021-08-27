---
title: Код уведомления LVN_DELETEITEM (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент собирается удалиться. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637cf2e8de98c056635cef2e68a7672f52b649c0162920f647384a2ceb4e64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062164"
---
# <a name="lvn_deleteitem-notification-code"></a>\_Код уведомления ЛВН DELETEITEM

Сообщает родительскому окну элемента управления "представление списка", что элемент собирается удалиться. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Член **Член iItem** определяет удаляемый элемент. Если у элемента управления нет стиля **LVS \_ овнердата** , то параметр *lParam* является определяемыми приложением данными, связанными с элементом. Все остальные члены этой структуры равны нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Не добавляйте, удаляйте и не Переупорядочивайте элементы в представлении списка при обработке этого кода уведомления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





