---
title: Сообщение DTM_GETDATETIMEPICKERINFO (Коммктрл. h)
description: Возвращает сведения об элементе управления "Выбор даты и времени" (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- Элементы управления Windows для DTM_GETDATETIMEPICKERINFO сообщений
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
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489297"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





