---
title: Сообщение TBM_GETPOS (Коммктрл. h)
description: Извлекает текущее логическое положение ползунка в TrackBar. Логические позиции — это целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- Элементы управления Windows для TBM_GETPOS сообщений
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490698"
---
# <a name="tbm_getpos-message"></a>\_Сообщение ТБМ жетпос

Извлекает текущее логическое положение ползунка в TrackBar. Логические позиции — это целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 32-разрядное значение, указывающее текущую логическую точку ползунка TrackBar.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ТБМ \_ сетпос**](tbm-setpos.md)
</dt> </dl>

 

 





