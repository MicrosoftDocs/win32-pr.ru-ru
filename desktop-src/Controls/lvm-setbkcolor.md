---
title: Сообщение LVM_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сетбкколор ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- Элементы управления Windows для LVM_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988907"
---
# <a name="lvm_setbkcolor-message"></a>\_Сообщение LVM сетбкколор

Задает цвет фона для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ сетбкколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Цвет фона для установки или значение CLR \_ None для отсутствия цвета фона. Элементы управления "представление списка" с фоновыми цветами перерисуются значительно быстрее, чем без фоновых цветов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





