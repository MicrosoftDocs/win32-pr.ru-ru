---
title: Сообщение LVM_DELETEALLITEMS (Коммктрл. h)
description: Удаляет все элементы из элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Делетеаллитемс ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- элементы управления Windows сообщений LVM_DELETEALLITEMS
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
ms.openlocfilehash: c81d2911caee047b63c4a637b6996bc90096e56d337f068beb73fe0fb42b4579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958413"
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

## <a name="remarks"></a>Remarks

Когда элемент управления "представление списка" получает сообщение **LVM \_ делетеаллитемс** , он отправляет код уведомления [**ЛВН \_ делетеаллитемс**](lvn-deleteallitems.md) в родительское окно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





