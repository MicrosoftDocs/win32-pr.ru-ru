---
title: Сообщение TB_SETHOTITEM2 (Коммктрл. h)
description: TB_SETHOTITEM2 сообщение — задает горячий элемент на панели инструментов.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- элементы управления Windows сообщений TB_SETHOTITEM2
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
ms.openlocfilehash: 8f4bb1e560e2be2b6952406d548215d60f2c2974e57b2388580da7453b51c184
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318824"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





