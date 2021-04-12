---
title: Сообщение LVM_GETFOOTERRECT (Коммктрл. h)
description: Извлекает координаты нижнего колонтитула для элемента управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеррект ListView.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- Элементы управления Windows для LVM_GETFOOTERRECT сообщений
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
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135127"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

