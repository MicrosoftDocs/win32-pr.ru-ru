---
title: Сообщение LVM_GETFOCUSEDGROUP (Коммктрл. h)
description: Возвращает группу, в которой находится фокус. Отправьте это сообщение явным образом или с помощью \_ макроса Жетфокуседграуп ListView.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- Элементы управления Windows для LVM_GETFOCUSEDGROUP сообщений
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
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489057"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





