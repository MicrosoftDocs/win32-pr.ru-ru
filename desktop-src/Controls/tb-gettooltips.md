---
title: Сообщение TB_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для элемента управления ToolTip (при наличии), связанного с панелью инструментов.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- элементы управления Windows сообщений TB_GETTOOLTIPS
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
ms.openlocfilehash: 41f326ffcc12e9fcf115b6f010e9fc8f7e327ce6381ce9a2fb3d397d8e322f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168230"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





