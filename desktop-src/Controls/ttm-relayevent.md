---
title: Сообщение TTM_RELAYEVENT (Коммктрл. h)
description: Передает сообщение мыши элементу управления ToolTip для обработки.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- Элементы управления Windows для TTM_RELAYEVENT сообщений
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353252"
---
# <a name="ttm_relayevent-message"></a>\_Сообщение ТТМ релайевент

Передает сообщение мыши элементу управления ToolTip для обработки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю. **Windows 7 и более поздние версии:** Если позиция подсказки смещена от позиции курсора (в порядке, когда палец или указывающее устройство не затронула), этот параметр может содержать дополнительные сведения, взятые из сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Извлеките эту лишнюю информацию с помощью [**жетмессажеекстраинфо**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , содержащую сообщение для ретрансляции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Элемент управления ToolTip обрабатывает только следующие сообщения, переданные в него сообщением **ТТМ \_ релайевент** :

-   WM \_ лбуттондовн
-   WM \_ лбуттонуп
-   WM \_ мбуттондовн
-   WM \_ мбуттонуп
-   WM \_ MOUSEMOVE
-   WM \_ нкмаусемове
-   WM \_ рбуттондовн
-   WM \_ рбуттонуп

Все остальные сообщения игнорируются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

