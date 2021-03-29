---
title: Сообщение LVM_GETTOOLTIPS (Коммктрл. h)
description: Извлекает элемент управления ToolTip, используемый элементом управления "представление списка" для отображения всплывающих подсказок. Это сообщение можно отправить явным образом или воспользоваться \_ макросом ListView.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- Элементы управления Windows для LVM_GETTOOLTIPS сообщений
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
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492402"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LVM \_ сеттултипс**](lvm-settooltips.md)
</dt> </dl>

 

 





