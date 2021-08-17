---
title: Сообщение LVM_GETFOOTERRECT (Коммктрл. h)
description: Извлекает координаты нижнего колонтитула для элемента управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеррект ListView.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- элементы управления Windows сообщений LVM_GETFOOTERRECT
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39bc2c5cd724c9b5b4885b99123489e49ead52243d43388e7eb22808fb43a826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411463"
---
# <a name="lvm_getfooterrect-message"></a>\_Сообщение LVM жетфутеррект

Извлекает координаты нижнего колонтитула для элемента управления "представление списка". Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфутеррект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется. Должно быть равно 0.

</dd> <dt>

*lParam* \[ в, out\]
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) для получения координат. Вызывающий процесс отвечает за выделение этой структуры. Полученные координаты выражаются как клиентские координаты.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

