---
title: Сообщение TB_BUTTONSTRUCTSIZE (Коммктрл. h)
description: Задает размер структуры ТББУТТОН.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- элементы управления Windows сообщений TB_BUTTONSTRUCTSIZE
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
ms.openlocfilehash: ceed10eec9038b338d060f28acdab8a10aa88aecef6b264b6d6d0682168f4937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919144"
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

## <a name="remarks"></a>Remarks

Система использует размер для определения используемой версии библиотеки динамической компоновки (DLL) общего элемента управления.

Если приложение использует функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) для создания панели инструментов, приложение должно отправить это сообщение на панель инструментов перед отправкой сообщения [**ТБ \_ аддбитмап**](tb-addbitmap.md) или [**ТБ \_ аддбуттонс**](tb-addbuttons.md) . Функция [**креатетулбарекс**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) автоматически отправляет **ТБ \_ буттонструктсизе**, а размер структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) является параметром функции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

