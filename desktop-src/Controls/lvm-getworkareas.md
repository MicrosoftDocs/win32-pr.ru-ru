---
title: Сообщение LVM_GETWORKAREAS (Коммктрл. h)
description: Извлекает рабочие области из элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетворкареас ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- элементы управления Windows сообщений LVM_GETWORKAREAS
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aed6173ef00860900d7690199cfb2c81535f088790290e30cc01898666bb068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968234"
---
# <a name="lvm_getworkareas-message"></a>\_Сообщение LVM жетворкареас

Извлекает рабочие области из элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать макрос [**\_ жетворкареас ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Число структур [**Rect**](/previous-versions//dd162897(v=vs.85)) в массиве в параметре *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив структур [**Rect**](/previous-versions//dd162897(v=vs.85)) , который получает текущие рабочие области элемента управления "представление списка". Значения в этих структурах находятся в клиентских координатах. *wParam* задает количество структур в этом массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование элементов управления List-View](using-list-view-controls.md)
</dt> </dl>

 

