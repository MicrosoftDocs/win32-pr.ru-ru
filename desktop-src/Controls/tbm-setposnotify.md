---
title: Сообщение TBM_SETPOSNOTIFY (Коммктрл. h)
description: TBM_SETPOSNOTIFY сообщение — задает текущую логическую точку ползунка в TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- элементы управления Windows сообщений TBM_SETPOSNOTIFY
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
ms.openlocfilehash: 677ab818524614f89d16ae851376d8776a4ccca3ef7798d4ac90aa6d36962ca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046084"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





