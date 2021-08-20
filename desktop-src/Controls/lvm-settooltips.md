---
title: Сообщение LVM_SETTOOLTIPS (Коммктрл. h)
description: Задает элемент управления ToolTip, который будет использоваться элементом управления "представление списка" для отображения всплывающих подсказок. Это сообщение можно отправить явным образом или использовать \_ макрос Сеттултипс ListView.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- элементы управления Windows сообщений LVM_SETTOOLTIPS
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
ms.openlocfilehash: 7bf2256d94630b8e792fd1f148864f3588b27e73ea5781eb0bdcd24bf9571507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170400"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**LVM \_ подсказки**](lvm-gettooltips.md)
</dt> </dl>

 

 





