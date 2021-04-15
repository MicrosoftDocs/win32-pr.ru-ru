---
title: Сообщение LVM_DELETEALLITEMS (Коммктрл. h)
description: Удаляет все элементы из элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Делетеаллитемс ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- Элементы управления Windows для LVM_DELETEALLITEMS сообщений
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489093"
---
# <a name="lvm_deleteallitems-message"></a>\_Сообщение LVM делетеаллитемс

Удаляет все элементы из элемента управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ делетеаллитемс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Когда элемент управления "представление списка" получает сообщение **LVM \_ делетеаллитемс** , он отправляет код уведомления [**ЛВН \_ делетеаллитемс**](lvn-deleteallitems.md) в родительское окно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





