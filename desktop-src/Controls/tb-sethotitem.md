---
title: Сообщение TB_SETHOTITEM (Коммктрл. h)
description: Задает горячий элемент на панели инструментов.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- Элементы управления Windows для TB_SETHOTITEM сообщений
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892333"
---
# <a name="tb_sethotitem-message"></a>\_Сообщение СЕСОТИТЕМ ТБ

Задает горячий элемент на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента, который будет активным. Если это значение равно-1, ни один из элементов не будет активным.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс предыдущего горячего элемента или значение-1, если элемент не был активным.

## <a name="remarks"></a>Комментарии

Поведение этого сообщения не определено для панелей инструментов, не имеющих [**\_ неструктурированного стиля тбстиле**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





