---
title: Код уведомления IPN_FIELDCHANGED (Коммктрл. h)
description: Посылается, когда пользователь изменяет поле в элементе управления или перемещается из одного поля в другое. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED кода уведомления Windows элементы управления
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
ms.openlocfilehash: 467cf7f14f3ff8d62f85d973e9a9d11c4dc6d20488ad5b7e30b4c0787b4b1a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085554"
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

## <a name="remarks"></a>Remarks

Этот код уведомления не отправляется в ответ на сообщение [**IPM \_ сетаддресс**](ipm-setaddress.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





