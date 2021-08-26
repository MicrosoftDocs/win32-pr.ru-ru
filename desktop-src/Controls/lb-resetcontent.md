---
title: Сообщение LB_RESETCONTENT (Winuser. h)
description: Удаляет все элементы из списка.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- элементы управления Windows сообщений LB_RESETCONTENT
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c896263cd4a695583bda299b0feeff552a05ef2c938b9df348da685821c46652
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085374"
---
# <a name="lb_resetcontent-message"></a>Сообщение ресетконтент балансировки нагрузки \_

Удаляет все элементы из списка.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Если список имеет стиль, рисуемый владельцем, но не хасстрингс в [**стиле \_ фунта**](list-box-styles.md) , владелец списка получает сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) для каждого элемента в списке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





