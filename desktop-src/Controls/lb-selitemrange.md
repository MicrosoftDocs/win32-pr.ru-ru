---
title: Сообщение LB_SELITEMRANGE (Winuser. h)
description: Выбирает или отменяет выбор одного или нескольких последовательных элементов в списке с множественным выбором.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- элементы управления Windows сообщений LB_SELITEMRANGE
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a08019f3d60e6c9bfe841067b48220b8fcfe75891c9bcc8db64bf28d219b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958603"
---
# <a name="lb_selitemrange-message"></a>Сообщение селитемранже балансировки нагрузки \_

Выбирает или отменяет выбор одного или нескольких последовательных элементов в списке с множественным выбором.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

**Значение true** , чтобы выбрать диапазон элементов, или **false** , чтобы снять его выделение.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) Указывает отсчитываемый от нуля индекс первого выбираемого элемента. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Указывает отсчитываемый от нуля индекс последнего выбираемого элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если возникает ошибка, возвращается значение фунтов \_ Err.

## <a name="remarks"></a>Remarks

Это сообщение следует использовать только в списках с множественным выбором.

Это сообщение может выбрать диапазон только в пределах первых 65 536 элементов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**селитемранжеекс балансировки нагрузки \_**](lb-selitemrangeex.md)
</dt> <dt>

[**сетсел балансировки нагрузки \_**](lb-setsel.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**макелпарам**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

