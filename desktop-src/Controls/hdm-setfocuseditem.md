---
title: Сообщение HDM_SETFOCUSEDITEM (Коммктрл. h)
description: Устанавливает фокус на указанный элемент в элементе управления "заголовок". Отправляйте это сообщение явным образом или с помощью \_ макроса Сетфокуседитем заголовка.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- элементы управления Windows сообщений HDM_SETFOCUSEDITEM
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
ms.openlocfilehash: 9ea853cf625473bee608111eddf877eb09457ee5c2ac6089542b5add0a212195
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171079"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Сведения об элементах управления "заголовок"](header-controls.md)
</dt> </dl>

 

 





