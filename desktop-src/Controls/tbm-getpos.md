---
title: Сообщение TBM_GETPOS (Коммктрл. h)
description: Извлекает текущее логическое положение ползунка в TrackBar. Логические позиции — это целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- элементы управления Windows сообщений TBM_GETPOS
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
ms.openlocfilehash: 54ed3b8afed7b96e657984a437ff54b1099f196b8dc3d0035468835152b5a841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078088"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ТБМ \_ сетпос**](tbm-setpos.md)
</dt> </dl>

 

 





