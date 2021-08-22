---
title: Сообщение LB_GETSELCOUNT (Winuser. h)
description: Возвращает общее число выбранных элементов в списке с множественным выбором.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- элементы управления Windows сообщений LB_GETSELCOUNT
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8cacbf266931daaeba4a98c95c7c428630708d833af7603b0be09cef3071212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434114"
---
# <a name="lb_getselcount-message"></a>Сообщение жетселкаунт балансировки нагрузки \_

Возвращает общее число выбранных элементов в списке с множественным выбором.

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

Возвращаемое значение — это количество выбранных элементов в списке. Если список является списком с одним выбором, возвращается значение фунтов \_ Err.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сетсел балансировки нагрузки \_**](lb-setsel.md)
</dt> </dl>

 

 





