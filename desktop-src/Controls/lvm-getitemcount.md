---
title: Сообщение LVM_GETITEMCOUNT (Коммктрл. h)
description: Извлекает количество элементов в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса GetItemCount ListView.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- элементы управления Windows сообщений LVM_GETITEMCOUNT
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1561e893930e4e3eca8de628c1df555e63794c3463edf81af798c53d873c8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109624"
---
# <a name="lvm_getitemcount-message"></a>\_Сообщение LVM GETITEMCOUNT

Извлекает количество элементов в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ GetItemCount ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число элементов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





