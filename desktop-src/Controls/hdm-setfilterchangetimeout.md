---
title: Сообщение HDM_SETFILTERCHANGETIMEOUT (Коммктрл. h)
description: Устанавливает интервал времени ожидания между временем изменения атрибутов фильтра и разноски \_ уведомления ХДН филтерчанже. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сетфилтерчанжетимеаут.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- элементы управления Windows сообщений HDM_SETFILTERCHANGETIMEOUT
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b5f8df12a7f30baa5f8b7d4bf15698b30cfbb6619fb71a81d4977b259c318b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435864"
---
# <a name="hdm_setfilterchangetimeout-message"></a>\_Сообщение СЕТФИЛТЕРЧАНЖЕТИМЕАУТ HDM

Устанавливает интервал времени ожидания между временем изменения атрибутов фильтра и разноски уведомления [ХДН \_ филтерчанже](hdn-filterchange.md) . Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сетфилтерчанжетимеаут**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение времени ожидания в миллисекундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс изменяемого элемента управления фильтра.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ХДН \_ филтерчанже](hdn-filterchange.md)
</dt> </dl>

 

 





