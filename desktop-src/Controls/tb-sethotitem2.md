---
title: Сообщение TB_SETHOTITEM2 (Коммктрл. h)
description: TB_SETHOTITEM2 сообщение — задает горячий элемент на панели инструментов.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- Элементы управления Windows для TB_SETHOTITEM2 сообщений
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104142"
---
# <a name="tb_sethotitem2-message"></a>\_Сообщение SETHOTITEM2 ТБ

Задает горячий элемент на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента, который будет активным. Если это значение равно-1, ни один из элементов не будет активным.

</dd> <dt>

*lParam* 
</dt> <dd>Сочетание \_ флагов хикф XXX. См. <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**нмтбхотитем**</a>.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс предыдущего горячего элемента или значение-1, если элемент не был активным.

## <a name="remarks"></a>Remarks

Поведение этого сообщения не определено для панелей инструментов, не имеющих [**\_ неструктурированного стиля тбстиле**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





