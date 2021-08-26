---
title: Сообщение LVM_UPDATE (Коммктрл. h)
description: Обновляет элемент представления списка. Если элемент управления "список" имеет \_ стиль АВТОУПОРЯДОЧИТЬ LVS, этот макрос приводит к упорядочиванию элемента управления "список". Это сообщение можно отправить явно или с помощью \_ макроса обновления ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- элементы управления Windows сообщений LVM_UPDATE
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
ms.openlocfilehash: ff9067d6eb80c5db7880ee9331a04e9259e9c841ccfe7dd80158a2afbcd06c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915234"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





