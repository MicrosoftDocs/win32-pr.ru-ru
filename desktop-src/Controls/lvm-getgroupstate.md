---
title: Сообщение LVM_GETGROUPSTATE (Коммктрл. h)
description: Возвращает состояние указанной группы. Отправьте это сообщение явным образом или с помощью \_ макроса Жетграупстате ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- Элементы управления Windows для LVM_GETGROUPSTATE сообщений
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489267"
---
# <a name="lvm_getgroupstate-message"></a>\_Сообщение LVM жетграупстате

Возвращает состояние указанной группы. Отправьте это сообщение явным образом или с помощью макроса [**\_ жетграупстате ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Задает Group By **играупид** (см. структуру [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Указывает извлекаемые значения состояния. Это сочетание флагов, перечисленных для элемента **State** элемента [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает сочетание заданных значений состояния. Например, если параметр *lParam* лвгс \_ свернут и возвращенное значение равно нулю, то лвгс \_ свернутое состояние не задано. Если группа не найдена, возвращается ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





