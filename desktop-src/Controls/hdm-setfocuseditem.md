---
title: Сообщение HDM_SETFOCUSEDITEM (Коммктрл. h)
description: Устанавливает фокус на указанный элемент в элементе управления "заголовок". Отправляйте это сообщение явным образом или с помощью \_ макроса Сетфокуседитем заголовка.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- Элементы управления Windows для HDM_SETFOCUSEDITEM сообщений
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136974"
---
# <a name="hdm_setfocuseditem-message"></a>\_Сообщение СЕТФОКУСЕДИТЕМ HDM

Устанавливает фокус на указанный элемент в элементе управления "заголовок". Отправляйте это сообщение явным образом или с помощью макроса [**\_ сетфокуседитем заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Не используется. Должен равняться нулю.</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Индекс элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

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

 

 





