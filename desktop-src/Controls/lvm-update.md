---
title: Сообщение LVM_UPDATE (Коммктрл. h)
description: Обновляет элемент представления списка. Если элемент управления "список" имеет \_ стиль АВТОУПОРЯДОЧИТЬ LVS, этот макрос приводит к упорядочиванию элемента управления "список". Это сообщение можно отправить явно или с помощью \_ макроса обновления ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- Элементы управления Windows для LVM_UPDATE сообщений
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891497"
---
# <a name="lvm_update-message"></a>\_Сообщение об обновлении LVM

Обновляет элемент представления списка. Если элемент управления "список" имеет стиль [**\_ Автоупорядочить LVS**](list-view-window-styles.md) , этот макрос приводит к упорядочиванию элемента управления "список". Это сообщение можно отправить явно или с помощью макроса [**\_ обновления ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс обновляемого элемента.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





