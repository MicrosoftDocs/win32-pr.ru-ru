---
title: Сообщение TTM_NEWTOOLRECT (Коммктрл. h)
description: Задает новый ограничивающий прямоугольник для инструмента.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- элементы управления Windows сообщений TTM_NEWTOOLRECT
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
ms.openlocfilehash: 13889b0e9c0d80392b88130c33e5e9723ceb776a60a6b941d205d514d96ca22f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750984"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ НЕВТУЛРЕКТВ** (Юникод) и **ТТМ \_ невтулректа** (ANSI)<br/>           |



 

 





