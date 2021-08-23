---
title: Сообщение TTM_RELAYEVENT (Коммктрл. h)
description: Передает сообщение мыши элементу управления ToolTip для обработки.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- элементы управления Windows сообщений TTM_RELAYEVENT
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
ms.openlocfilehash: 051a0b7ab8ecd93b15ceb9187eefd6f566b55d653b751889cd29acec58366716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166367"
---
# <a name="ttm_relayevent-message"></a>\_Сообщение ТТМ релайевент

Передает сообщение мыши элементу управления ToolTip для обработки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю. **Windows 7 и более поздних версий:** Если позиция подсказки смещена от позиции курсора (в порядке, когда палец или указывающее устройство не затронула), этот параметр может содержать дополнительные сведения, взятые из сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Извлеките эту лишнюю информацию с помощью [**жетмессажеекстраинфо**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , содержащую сообщение для ретрансляции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

