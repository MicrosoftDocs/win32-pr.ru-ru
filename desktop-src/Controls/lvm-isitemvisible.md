---
title: Сообщение LVM_ISITEMVISIBLE (Коммктрл. h)
description: Указывает, является ли видимым элемент в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Иситемвисибле ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- Элементы управления Windows для LVM_ISITEMVISIBLE сообщений
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
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892433"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





