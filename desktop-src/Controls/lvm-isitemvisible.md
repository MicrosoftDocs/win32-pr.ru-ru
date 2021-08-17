---
title: Сообщение LVM_ISITEMVISIBLE (Коммктрл. h)
description: Указывает, является ли видимым элемент в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Иситемвисибле ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- элементы управления Windows сообщений LVM_ISITEMVISIBLE
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424d321b79b4a4f497942c36ca78c751cc5404cdfaf965b451eea94a8b3c8e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958183"
---
# <a name="lvm_isitemvisible-message"></a>\_Сообщение LVM иситемвисибле

Указывает, является ли видимым элемент в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью макроса [**\_ иситемвисибле ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Индекс элемента в элементе управления List-View.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если видимое, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





