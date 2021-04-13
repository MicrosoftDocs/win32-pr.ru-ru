---
title: Сообщение LVM_INSERTCOLUMN (Коммктрл. h)
description: Вставляет новый столбец в элемент управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Инсертколумн ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- Элементы управления Windows для LVM_INSERTCOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535033"
---
# <a name="lvm_insertcolumn-message"></a>\_Сообщение LVM инсертколумн

Вставляет новый столбец в элемент управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ инсертколумн ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс нового столбца.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) , содержащую атрибуты нового столбца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс нового столбца, если он выполнен успешно, или значение-1 в противном случае.

## <a name="remarks"></a>Комментарии

Столбцы видимы только в представлении отчета (Details).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





