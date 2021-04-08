---
title: Сообщение TBM_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для элемента управления ToolTip, назначенного для TrackBar, если таковой имеется.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- Элементы управления Windows для TBM_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891953"
---
# <a name="tbm_gettooltips-message"></a>Сообщение ТБМ с \_ ПОДсказками

Получает маркер для элемента управления ToolTip, назначенного для TrackBar, если таковой имеется.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для элемента управления ToolTip, назначенного для TrackBar, или **значение NULL** , если подсказки не используются. Если элемент управления TrackBar не использует стиль [**\_ подсказок TBS**](trackbar-control-styles.md) , возвращается значение **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





