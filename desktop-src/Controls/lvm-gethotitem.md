---
title: Сообщение LVM_GETHOTITEM (Коммктрл. h)
description: Извлекает индекс горячего элемента. Это сообщение можно отправить явным образом или использовать \_ макрос Жесотитем ListView.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- элементы управления Windows сообщений LVM_GETHOTITEM
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 743bd7a80a58bec41fa5a75f24b0e333ab33ad152909adb6ea69a9c4ca0fd78b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958403"
---
# <a name="lvm_gethotitem-message"></a>\_Сообщение LVM жесотитем

Извлекает индекс горячего элемента. Это сообщение можно отправить явным образом или использовать макрос [**\_ жесотитем ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс неактивного элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





