---
title: Сообщение LVM_GETITEMCOUNT (Коммктрл. h)
description: Извлекает количество элементов в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса GetItemCount ListView.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- Элементы управления Windows для LVM_GETITEMCOUNT сообщений
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
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803394"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





