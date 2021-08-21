---
title: Сообщение LVM_GETTOOLTIPS (Коммктрл. h)
description: Извлекает элемент управления ToolTip, используемый элементом управления "представление списка" для отображения всплывающих подсказок. Это сообщение можно отправить явным образом или воспользоваться \_ макросом ListView.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- элементы управления Windows сообщений LVM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ca4340a8c57c6551d3c46f9324e4b66250f383c9412a3772df3114f105c5f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019292"
---
# <a name="lvm_gettooltips-message"></a>Сообщение LVM с \_ ПОДсказками

Извлекает элемент управления ToolTip, используемый элементом управления "представление списка" для отображения всплывающих подсказок. Это сообщение можно отправить явным образом или воспользоваться макросом [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер элемента управления ToolTip.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LVM \_ сеттултипс**](lvm-settooltips.md)
</dt> </dl>

 

 





