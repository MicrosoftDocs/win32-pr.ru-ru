---
title: Сообщение DTM_CLOSEMONTHCAL (Коммктрл. h)
description: Закрывает элемент управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime клосемонскал.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- элементы управления Windows сообщений DTM_CLOSEMONTHCAL
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f458592d2842625b9826eda5963c66cbd182e3f052a2b2a70ff5219a054e8cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878244"
---
# <a name="dtm_closemonthcal-message"></a>\_Сообщение DTM клосемонскал

Закрывает элемент управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью макроса [**DateTime \_ клосемонскал**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль.

## <a name="remarks"></a>Remarks

Уничтожает элемент управления и отправляет уведомление [ДТН \_ крупный план](dtn-closeup.md) о том, что элемент управления закрывается (в отличие от раскрывающегося уведомления [ДТН \_ ](dtn-dropdown.md) ) к родителю элемента управления.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[\_раскрывающийся список ДТН](dtn-dropdown.md)
</dt> <dt>

[ДТН \_ крупный план](dtn-closeup.md)
</dt> </dl>

 

 





