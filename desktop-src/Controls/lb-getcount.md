---
title: Сообщение LB_GETCOUNT (Winuser. h)
description: Возвращает число элементов в поле со списком.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- элементы управления Windows сообщений LB_GETCOUNT
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4f4792bf290343e2868b754f8efb1bfc03d0be1f600c9f7584f051053400b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435483"
---
# <a name="lb_getcount-message"></a>\_Сообщение счетчика нагрузки

Возвращает число элементов в поле со списком.

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

Возвращаемое значение — это число элементов в списке или ошибка балансировки нагрузки \_ при возникновении ошибки.

## <a name="remarks"></a>Remarks

Возвращаемое значение счетчика больше значения индекса последнего элемента (индекс отсчитывается от нуля).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сеткаунт балансировки нагрузки \_**](lb-setcount.md)
</dt> </dl>

 

 





