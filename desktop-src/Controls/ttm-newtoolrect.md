---
title: Сообщение TTM_NEWTOOLRECT (Коммктрл. h)
description: Задает новый ограничивающий прямоугольник для инструмента.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- Элементы управления Windows для TTM_NEWTOOLRECT сообщений
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490671"
---
# <a name="ttm_newtoolrect-message"></a>\_Сообщение ТТМ невтулрект

Задает новый ограничивающий прямоугольник для инструмента.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Элементы **HWND** и **uId** определяют инструмент, а член **Rect** задает новый ограничивающий прямоугольник. Перед отправкой этого сообщения необходимо заполнить элемент **кбсизе** этой структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ НЕВТУЛРЕКТВ** (Юникод) и **ТТМ \_ невтулректа** (ANSI)<br/>           |



 

 





