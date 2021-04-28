---
title: Сообщение TBM_SETPOSNOTIFY (Коммктрл. h)
description: TBM_SETPOSNOTIFY сообщение — задает текущую логическую точку ползунка в TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- Элементы управления Windows для TBM_SETPOSNOTIFY сообщений
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104082"
---
# <a name="tbm_setposnotify-message"></a>\_Сообщение ТБМ сетпоснотифи

Задает текущую логическую точку ползунка в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

wParam не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Новое логическое положение ползунка. Допустимыми логическими позициями являются целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка. Если это значение находится за пределами максимального и минимального значений элемента управления, то для этой должности устанавливается максимальное или минимальное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Вызов **ТБМ \_ сетпоснотифи** установит положение ползунка TrackBar, например [**ТБМ \_ сетпос**](tbm-setpos.md) , но также приведет к тому, что свойство TrackBar будет уведомлять его родителя перемещения через сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





