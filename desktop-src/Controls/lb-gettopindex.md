---
title: Сообщение LB_GETTOPINDEX (Winuser. h)
description: Возвращает индекс первого видимого элемента в поле со списком.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- элементы управления Windows сообщений LB_GETTOPINDEX
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b23360da45041e5a728f370e54f8250f216507dd439291a2ffce5ed383d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085384"
---
# <a name="lb_gettopindex-message"></a>Сообщение жеттопиндекс балансировки нагрузки \_

Возвращает индекс первого видимого элемента в поле со списком. Изначально элемент с индексом 0 находится в верхней части окна списка, но если содержимое списка было прокручено, то в верхней части может находиться другой элемент. Первый видимый элемент в списке с несколькими столбцами является верхним левым элементом.

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

Возвращаемое значение — это индекс первого видимого элемента в списке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сеттопиндекс балансировки нагрузки \_**](lb-settopindex.md)
</dt> </dl>

 

 





