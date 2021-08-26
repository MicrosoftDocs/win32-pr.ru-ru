---
title: Сообщение LVM_GETFOCUSEDGROUP (Коммктрл. h)
description: Возвращает группу, в которой находится фокус. Отправьте это сообщение явным образом или с помощью \_ макроса Жетфокуседграуп ListView.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- элементы управления Windows сообщений LVM_GETFOCUSEDGROUP
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9b253405683c058518706e92e62f09041ae4db0e4bee426aa653103bda2188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877434"
---
# <a name="lvm_getfocusedgroup-message"></a>\_Сообщение LVM жетфокуседграуп

Возвращает группу, в которой находится фокус. Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфокуседграуп ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс группы с состоянием ЛВГС \_ Focused или-1, если нет группы с состоянием лвгс \_ Focused.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





