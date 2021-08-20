---
title: Сообщение RB_GETTOOLTIPS (Коммктрл. h)
description: Извлекает маркер любого элемента управления ToolTip, связанного с элементом управления "Главная панель".
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- элементы управления Windows сообщений RB_GETTOOLTIPS
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859934dcdec85d0b160f9076f2a77263a02a187ebf49f8ccbb4af20fc3e82d13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540064"
---
# <a name="rb_gettooltips-message"></a>\_Сообщение о ВЫсказке RB

Извлекает маркер любого элемента управления ToolTip, связанного с элементом управления "Главная панель".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HWND** , которое является дескриптором элемента управления ToolTip, связанного с элементом управления главной панели, или нулем, если элемент управления ToolTip не связан с элементом управления главной панели.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





