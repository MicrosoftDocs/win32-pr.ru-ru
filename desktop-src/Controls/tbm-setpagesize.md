---
title: Сообщение TBM_SETPAGESIZE (Коммктрл. h)
description: Задает число логических позиций, на которое ползунок TrackBar перемещается в ответ на ввод с клавиатуры, например клавиши или, или ввод с помощью мыши, например щелчки в канале TrackBar.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- Элементы управления Windows для TBM_SETPAGESIZE сообщений
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071854"
---
# <a name="tbm_setpagesize-message"></a>\_Сообщение ТБМ SETPAGESIZE

Задает число логических позиций, на которое ползунок TrackBar перемещается в ответ на ввод с клавиатуры, например клавиши или, или ввод с помощью мыши, например щелчки в канале TrackBar. Логическое положение — это целое число, увеличивающееся в диапазоне значений TrackBar от минимума до максимальной позиции ползунка.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Новый размер страницы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 32-разрядное значение, указывающее размер предыдущей страницы.

## <a name="remarks"></a>Комментарии

Эта линейка также отправляет сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) с \_ кодами уведомлений ТБ PageUp и ТБ \_ PageDown в родительское окно, когда оно получает ввод с клавиатуры или с помощью мыши для прокрутки страницы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ТБМая \_ pageSize**](tbm-getpagesize.md)
</dt> </dl>

 

 





