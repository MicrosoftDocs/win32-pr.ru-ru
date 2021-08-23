---
title: Сообщение LVM_GETGROUPSTATE (Коммктрл. h)
description: Возвращает состояние указанной группы. Отправьте это сообщение явным образом или с помощью \_ макроса Жетграупстате ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- элементы управления Windows сообщений LVM_GETGROUPSTATE
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
ms.openlocfilehash: 66272dd259e80f239804ffadbd706370f948a2505173cc03aaa40057b273a629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958433"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





