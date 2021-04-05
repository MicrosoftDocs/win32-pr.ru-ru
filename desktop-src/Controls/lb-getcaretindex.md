---
title: Сообщение LB_GETCARETINDEX (Winuser. h)
description: Извлекает индекс элемента, который находится в фокусе, в списке с множественным выбором. Элемент может быть или не выбран.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- Элементы управления Windows для LB_GETCARETINDEX сообщений
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
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071970"
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

## <a name="remarks"></a>Комментарии

Это сообщение также может использоваться для получения индекса элемента, выбранного в данный момент в списке с одним выбором.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сеткаретиндекс балансировки нагрузки \_**](lb-setcaretindex.md)
</dt> </dl>

 

 





