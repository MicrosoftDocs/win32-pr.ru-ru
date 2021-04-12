---
title: Сообщение WM_DWMCOLORIZATIONCOLORCHANGED (Winuser. h)
description: Информирует все окна верхнего уровня о том, что цвет цветов изменился.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- Сообщение WM_DWMCOLORIZATIONCOLORCHANGED диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136074"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a>\_Сообщение ДВМКОЛОРИЗАТИОНКОЛОРЧАНЖЕД WM

Информирует все окна верхнего уровня о том, что цвет цветов изменился.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает новый цвет раскраски. Цветовой формат — 0xAARRGGBB.

</dd> <dt>

*lParam* 
</dt> <dd>

Указывает, смешивается ли новый цвет с непрозрачностью.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

[**Двмжетколоризатионколор**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) используется для определения текущего значения цвета.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

