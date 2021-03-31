---
title: Сообщение DTM_SETMCSTYLE (Коммктрл. h)
description: Задает стиль элемента управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime сетмонскалстиле.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- Элементы управления Windows для DTM_SETMCSTYLE сообщений
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136671"
---
# <a name="dtm_setmcstyle-message"></a>\_Сообщение DTM сетмкстиле

Задает стиль элемента управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью макроса [**DateTime \_ сетмонскалстиле**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>Значение стиля. Дополнительные сведения см. в разделе <a href="month-calendar-control-styles.md">стили элементов управления календарем месяца</a>.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение предыдущего стиля.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





