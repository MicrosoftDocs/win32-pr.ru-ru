---
title: Сообщение TB_SETTOOLTIPS (Коммктрл. h)
description: Связывает элемент управления ToolTip с панелью инструментов.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- Элементы управления Windows для TB_SETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071378"
---
# <a name="tb_settooltips-message"></a>\_Сообщение СЕТТУЛТИПС ТБ

Связывает элемент управления ToolTip с панелью инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик для элемента управления ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Все кнопки, добавленные на панель инструментов перед отправкой сообщения **\_ сеттултипс ТБ** , не будут зарегистрированы в элементе управления ToolTip.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





