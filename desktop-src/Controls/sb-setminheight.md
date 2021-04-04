---
title: Сообщение SB_SETMINHEIGHT (Коммктрл. h)
description: Задает минимальную высоту области отображения окна состояния.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- Элементы управления Windows для SB_SETMINHEIGHT сообщений
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989072"
---
# <a name="sb_setminheight-message"></a>\_Сообщение SB сетминхеигхт

Задает минимальную высоту области отображения окна состояния.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Минимальная высота окна в пикселях.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Минимальная высота — это сумма параметра *wParam* и удвоенная ширина (в пикселях) вертикальной границы окна состояния. Приложение должно отправить сообщение [**\_ размером WM**](/windows/desktop/winmsg/wm-size) в окно состояния, чтобы перерисовать окно. Параметры *wParam* и *lParam* сообщения **\_ размера WM** должны иметь значение 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

