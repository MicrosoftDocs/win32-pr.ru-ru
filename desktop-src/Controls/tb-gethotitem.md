---
title: Сообщение TB_GETHOTITEM (Коммктрл. h)
description: Получает индекс горячего элемента на панели инструментов.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- Элементы управления Windows для TB_GETHOTITEM сообщений
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490194"
---
# <a name="tb_gethotitem-message"></a>\_Сообщение ЖЕСОТИТЕМ ТБ

Получает индекс горячего элемента на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс горячего элемента или значение-1, если не задан ни один активный элемент. Элементы управления ToolBar, у которых нет [**\_ неструктурированного стиля тбстиле**](toolbar-control-and-button-styles.md) , не имеют активных элементов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





