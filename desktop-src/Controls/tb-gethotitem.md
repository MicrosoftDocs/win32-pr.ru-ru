---
title: Сообщение TB_GETHOTITEM (Коммктрл. h)
description: Получает индекс горячего элемента на панели инструментов.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- элементы управления Windows сообщений TB_GETHOTITEM
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
ms.openlocfilehash: c22f33566a586ceaa524f720a9d688897f132ee227950f1f786093150955eafa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918834"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





