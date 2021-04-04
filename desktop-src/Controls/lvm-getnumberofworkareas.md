---
title: Сообщение LVM_GETNUMBEROFWORKAREAS (Коммктрл. h)
description: Извлекает количество рабочих областей в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетнумберофворкареас ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- Элементы управления Windows для LVM_GETNUMBEROFWORKAREAS сообщений
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
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989174"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование элементов управления List-View](using-list-view-controls.md)
</dt> </dl>

 

 





