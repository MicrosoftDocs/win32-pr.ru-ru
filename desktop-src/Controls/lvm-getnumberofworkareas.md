---
title: Сообщение LVM_GETNUMBEROFWORKAREAS (Коммктрл. h)
description: Извлекает количество рабочих областей в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетнумберофворкареас ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- элементы управления Windows сообщений LVM_GETNUMBEROFWORKAREAS
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 735dbb808755857df3dec4c5e8a021b9fe873e555607dc547bc77e67e123b948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088884"
---
# <a name="lvm_getnumberofworkareas-message"></a>\_Сообщение LVM жетнумберофворкареас

Извлекает количество рабочих областей в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать макрос [**\_ жетнумберофворкареас ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на значение UINT, которое получает количество рабочих областей в элементе управления "представление списка". Если в эту переменную помещается ноль, то в настоящее время не заданы никакие рабочие области. Это значение не может быть **равно NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование элементов управления List-View](using-list-view-controls.md)
</dt> </dl>

 

 





