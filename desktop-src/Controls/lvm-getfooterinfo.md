---
title: Сообщение LVM_GETFOOTERINFO (Коммктрл. h)
description: Возвращает сведения о нижнем колонтитуле элемента управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеринфо ListView.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- Элементы управления Windows для LVM_GETFOOTERINFO сообщений
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988202"
---
# <a name="lvm_getfooterinfo-message"></a>\_Сообщение LVM жетфутеринфо

Возвращает сведения о нижнем колонтитуле элемента управления "представление списка". Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфутеринфо ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется. Должно быть равно 0.

</dd> <dt>

*lParam* \[ в, out\]
</dt> <dd>

Указатель на структуру [**лвфутеринфо**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) для получения сведений в зависимости от значения элемента **маски** . Вызывающий процесс отвечает за выделение этой структуры и задание элемента **маски** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





