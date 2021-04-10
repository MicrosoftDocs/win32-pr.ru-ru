---
title: Код уведомления IPN_FIELDCHANGED (Коммктрл. h)
description: Посылается, когда пользователь изменяет поле в элементе управления или перемещается из одного поля в другое. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071871"
---
# <a name="ipn_fieldchanged-notification-code"></a>\_Код уведомления ИПН фиелдчанжед

Посылается, когда пользователь изменяет поле в элементе управления или перемещается из одного поля в другое. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмипаддресс**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) , содержащую сведения об измененном адресе. Элемент **iValue** этой структуры будет содержать указанное значение, даже если оно выходит за пределы диапазона поля. Этот элемент можно изменить на любое значение в диапазоне для поля в ответ на этот код уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Комментарии

Этот код уведомления не отправляется в ответ на сообщение [**IPM \_ сетаддресс**](ipm-setaddress.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





