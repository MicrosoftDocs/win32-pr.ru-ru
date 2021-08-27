---
title: Сообщение TB_SETTOOLTIPS (Коммктрл. h)
description: Связывает элемент управления ToolTip с панелью инструментов.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- элементы управления Windows сообщений TB_SETTOOLTIPS
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
ms.openlocfilehash: a75827df49eeaf8b6175cd14180ebb26ddbb642588ee77d625c701eee457baaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061234"
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

## <a name="remarks"></a>Remarks

Все кнопки, добавленные на панель инструментов перед отправкой сообщения **\_ сеттултипс ТБ** , не будут зарегистрированы в элементе управления ToolTip.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





