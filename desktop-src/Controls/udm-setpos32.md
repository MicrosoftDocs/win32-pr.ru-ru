---
title: Сообщение UDM_SETPOS32 (Коммктрл. h)
description: Задает расположение элемента управления "вверх-вниз" с 32-разрядной точностью.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- Элементы управления Windows для UDM_SETPOS32 сообщений
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988978"
---
# <a name="udm_setpos32-message"></a>\_Сообщение SETPOS32 UDM

Задает расположение элемента управления "вверх-вниз" с 32-разрядной точностью.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Переменная целочисленного типа, указывающая новое расположение для элемента управления "вверх/вниз". Если параметр находится за пределами указанного диапазона элемента управления, для *lParam* задается ближайшее допустимое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущее расположение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_ЖЕТПОС UDM**](udm-getpos.md)
</dt> <dt>

[**\_СЕТПОС UDM**](udm-setpos.md)
</dt> <dt>

[**\_GETPOS32 UDM**](udm-getpos32.md)
</dt> </dl>

 

 





