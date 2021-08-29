---
title: Сообщение LVM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент из элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса DeleteItem ListView.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- элементы управления Windows сообщений LVM_DELETEITEM
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88520e7d4f9d0d3ff22f90d7cea033b7674cfcbadbf55358f7ced8cc36c2399a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958423"
---
# <a name="lvm_deleteitem-message"></a>\_Сообщение LVM DELETEITEM

Удаляет элемент из элемента управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ DeleteItem ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс удаляемого элемента списка.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





