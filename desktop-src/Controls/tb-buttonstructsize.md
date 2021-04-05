---
title: Сообщение TB_BUTTONSTRUCTSIZE (Коммктрл. h)
description: Задает размер структуры ТББУТТОН.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- Элементы управления Windows для TB_BUTTONSTRUCTSIZE сообщений
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072031"
---
# <a name="tb_buttonstructsize-message"></a>\_Сообщение БУТТОНСТРУКТСИЗЕ ТБ

Задает размер структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Размер (в байтах) структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Система использует размер для определения используемой версии библиотеки динамической компоновки (DLL) общего элемента управления.

Если приложение использует функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) для создания панели инструментов, приложение должно отправить это сообщение на панель инструментов перед отправкой сообщения [**ТБ \_ аддбитмап**](tb-addbitmap.md) или [**ТБ \_ аддбуттонс**](tb-addbuttons.md) . Функция [**креатетулбарекс**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) автоматически отправляет **ТБ \_ буттонструктсизе**, а размер структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) является параметром функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

