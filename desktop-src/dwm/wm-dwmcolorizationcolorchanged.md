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
ms.openlocfilehash: 5bdbb854821f2a25565241700d28964b2d32319bccb8226c3d7d789c0e457fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094594"
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

## <a name="remarks"></a>Remarks

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

[**Двмжетколоризатионколор**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) используется для определения текущего значения цвета.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

