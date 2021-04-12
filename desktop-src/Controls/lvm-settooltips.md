---
title: Сообщение LVM_SETTOOLTIPS (Коммктрл. h)
description: Задает элемент управления ToolTip, который будет использоваться элементом управления "представление списка" для отображения всплывающих подсказок. Это сообщение можно отправить явным образом или использовать \_ макрос Сеттултипс ListView.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- Элементы управления Windows для LVM_SETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489966"
---
# <a name="lvm_settooltips-message"></a>\_Сообщение LVM сеттултипс

Задает элемент управления ToolTip, который будет использоваться элементом управления "представление списка" для отображения всплывающих подсказок. Это сообщение можно отправить явным образом или использовать макрос [**\_ сеттултипс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Обрабатываемый элемент управления ToolTip.</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер предыдущего элемента управления ToolTip.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LVM \_ подсказки**](lvm-gettooltips.md)
</dt> </dl>

 

 





