---
title: Сообщение LB_GETCARETINDEX (Winuser. h)
description: Извлекает индекс элемента, который находится в фокусе, в списке с множественным выбором. Элемент может быть или не выбран.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- элементы управления Windows сообщений LB_GETCARETINDEX
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74732bae571cdcba0cfe8096437bf681e7a339c5c0edb3f18d378ea610bdf8c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085544"
---
# <a name="lb_getcaretindex-message"></a>Сообщение жеткаретиндекс балансировки нагрузки \_

Извлекает индекс элемента, который находится в фокусе, в списке с множественным выбором. Элемент может быть или не выбран.

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

Возвращаемое значение — это Отсчитываемый от нуля индекс элемента списка с фокусом или 0, если ни один элемент не имеет фокуса.

## <a name="remarks"></a>Remarks

Это сообщение также может использоваться для получения индекса элемента, выбранного в данный момент в списке с одним выбором.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сеткаретиндекс балансировки нагрузки \_**](lb-setcaretindex.md)
</dt> </dl>

 

 





