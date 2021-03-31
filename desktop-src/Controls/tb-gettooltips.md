---
title: Сообщение TB_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для элемента управления ToolTip (при наличии), связанного с панелью инструментов.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- Элементы управления Windows для TB_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071706"
---
# <a name="tb_gettooltips-message"></a>\_Сообщение о СОсказках в ТБ

Получает маркер для элемента управления ToolTip (при наличии), связанного с панелью инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для элемента управления ToolTip или **значение NULL** , если у панели инструментов нет связанной подсказки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





