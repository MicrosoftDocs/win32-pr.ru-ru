---
title: Сообщение LVM_SETHOTITEM (Коммктрл. h)
description: Задает активный элемент для элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Сесотитем ListView.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- элементы управления Windows сообщений LVM_SETHOTITEM
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6937cbed8150bf14eb71e167b8ed54d6f6b47ae995a3af989613cba30c7ca3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077244"
---
# <a name="lvm_sethotitem-message"></a>\_Сообщение LVM сесотитем

Задает активный элемент для элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать макрос [**\_ сесотитем ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс элемента, который должен быть установлен в качестве горячего элемента.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента, который ранее был неактивен.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





