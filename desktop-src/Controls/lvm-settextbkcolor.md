---
title: Сообщение LVM_SETTEXTBKCOLOR (Коммктрл. h)
description: Задает цвет фона для текста в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сеттекстбкколор ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- элементы управления Windows сообщений LVM_SETTEXTBKCOLOR
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
ms.openlocfilehash: 3d9acdc193609f39fb81aa88263724a507695f15dcb8ba0c789df5c2a4f4d128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656234"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





