---
title: Сообщение DTM_GETDATETIMEPICKERINFO (Коммктрл. h)
description: Возвращает сведения об элементе управления "Выбор даты и времени" (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- элементы управления Windows сообщений DTM_GETDATETIMEPICKERINFO
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48dc639a48455564b9f925f7d6eea9634c01e597323f81d951cfde372a34ea37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878224"
---
# <a name="dtm_getdatetimepickerinfo-message"></a>\_Сообщение DTM жетдатетимепиккеринфо

Возвращает сведения об элементе управления "Выбор даты и времени" (DTP).

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd> Указатель на <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**датетимепиккеринфо**</a> для получения информации. Вызывающий объект отвечает за выделение памяти для этой структуры. Перед отправкой этого сообщения установите для элемента **кбсизе** структуры значение sizeof (датетимепиккеринфо).</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не учитывается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





