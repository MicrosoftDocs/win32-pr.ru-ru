---
title: Сообщение TBM_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для элемента управления ToolTip, назначенного для TrackBar, если таковой имеется.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- элементы управления Windows сообщений TBM_GETTOOLTIPS
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
ms.openlocfilehash: 4c97c94ab3a696f5967f724e76d2d8702a01275bedc06ad7c13907d57710a078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078068"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





