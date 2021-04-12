---
title: Сообщение LVM_GETWORKAREAS (Коммктрл. h)
description: Извлекает рабочие области из элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетворкареас ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- Элементы управления Windows для LVM_GETWORKAREAS сообщений
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
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492396"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование элементов управления List-View](using-list-view-controls.md)
</dt> </dl>

 

