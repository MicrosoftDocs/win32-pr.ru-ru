---
title: Сообщение TTM_GETBUBBLESIZE (Коммктрл. h)
description: Возвращает ширину и высоту элемента управления ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- Элементы управления Windows для TTM_GETBUBBLESIZE сообщений
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135946"
---
# <a name="ttm_getbubblesize-message"></a>\_Сообщение ТТМ жетбубблесизе

Возвращает ширину и высоту элемента управления ToolTip.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ToolTip.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ширину подсказки в нижнем слове и высоту в высоком слове в случае успеха. В противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Если \_ Флаги TTF Track и TTF \_ заданы в элементе **Уфлагс** структуры подсказки [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , это сообщение можно использовать для точного размещения подсказки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





