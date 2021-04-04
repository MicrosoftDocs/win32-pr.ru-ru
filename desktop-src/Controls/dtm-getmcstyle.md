---
title: Сообщение DTM_GETMCSTYLE (Коммктрл. h)
description: Возвращает стиль элемента управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime жетмонскалстиле.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- Элементы управления Windows для DTM_GETMCSTYLE сообщений
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989019"
---
# <a name="dtm_getmcstyle-message"></a>\_Сообщение DTM жетмкстиле

Возвращает стиль элемента управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью макроса [**DateTime \_ жетмонскалстиле**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение стиля элемента управления. Дополнительные сведения см. в разделе [стили элементов управления календарем месяца](month-calendar-control-styles.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





