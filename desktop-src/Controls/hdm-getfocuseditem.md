---
title: Сообщение HDM_GETFOCUSEDITEM (Коммктрл. h)
description: Возвращает элемент в элементе управления "заголовок", который находится в фокусе. Отправляйте это сообщение явным образом или с помощью \_ макроса Жетфокуседитем заголовка.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- Элементы управления Windows для HDM_GETFOCUSEDITEM сообщений
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491478"
---
# <a name="hdm_getfocuseditem-message"></a>\_Сообщение ЖЕТФОКУСЕДИТЕМ HDM

Возвращает элемент в элементе управления "заголовок", который находится в фокусе. Отправляйте это сообщение явным образом или с помощью макроса [**\_ жетфокуседитем заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Не используется. Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Не используется. Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента в фокусе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сведения об элементах управления "заголовок"](header-controls.md)
</dt> </dl>

 

 





