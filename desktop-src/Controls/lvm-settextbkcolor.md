---
title: Сообщение LVM_SETTEXTBKCOLOR (Коммктрл. h)
description: Задает цвет фона для текста в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сеттекстбкколор ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- Элементы управления Windows для LVM_SETTEXTBKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071456"
---
# <a name="lvm_settextbkcolor-message"></a>\_Сообщение LVM сеттекстбкколор

Задает цвет фона для текста в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ сеттекстбкколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Новый цвет фона текста. Это может быть "CLR \_ None" для отсутствия цвета фона.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





