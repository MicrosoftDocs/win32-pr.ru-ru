---
title: Сообщение HDM_SETFILTERCHANGETIMEOUT (Коммктрл. h)
description: Устанавливает интервал времени ожидания между временем изменения атрибутов фильтра и разноски \_ уведомления ХДН филтерчанже. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сетфилтерчанжетимеаут.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- Элементы управления Windows для HDM_SETFILTERCHANGETIMEOUT сообщений
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
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071873"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ХДН \_ филтерчанже](hdn-filterchange.md)
</dt> </dl>

 

 





