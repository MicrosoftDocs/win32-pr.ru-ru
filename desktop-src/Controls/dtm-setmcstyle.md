---
title: Сообщение DTM_SETMCSTYLE (Коммктрл. h)
description: Задает стиль элемента управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime сетмонскалстиле.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- элементы управления Windows сообщений DTM_SETMCSTYLE
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
ms.openlocfilehash: 2805f2213bcbb1fa91a10ea80005b8b23bbc7447973bba6930bfdcb1e52a9e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877804"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





