---
title: Сообщение LB_SELITEMRANGE (Winuser. h)
description: Выбирает или отменяет выбор одного или нескольких последовательных элементов в списке с множественным выбором.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- Элементы управления Windows для LB_SELITEMRANGE сообщений
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
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071912"
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

## <a name="remarks"></a>Комментарии

Это сообщение следует использовать только в списках с множественным выбором.

Это сообщение может выбрать диапазон только в пределах первых 65 536 элементов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



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

 

