---
title: Сообщение LVM_GETFOOTERITEM (Коммктрл. h)
description: Возвращает сведения о элементе нижнего колонтитула в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеритем ListView.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- Элементы управления Windows для LVM_GETFOOTERITEM сообщений
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071116"
---
# <a name="lvm_getfooteritem-message"></a>\_Сообщение LVM жетфутеритем

Возвращает сведения о элементе нижнего колонтитула в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфутеритем ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Индекс элемента.

</dd> <dt>

*lParam* \[ в, out\]
</dt> <dd>

Указатель на структуру [**лвфутеритем**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) для получения значения для элементов **State** и/или **псзтекст** в соответствии со значением элемента **маски** . Вызывающий процесс отвечает за выделение этой структуры и установку ее членов для указания получателю возвращаемой информации. Дополнительные сведения см. в разделе **лвфутеритем**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





