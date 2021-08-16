---
title: Сообщение TBM_SETRANGEMAX (Коммктрл. h)
description: Задает максимальное логическое положение ползунка в TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- элементы управления Windows сообщений TBM_SETRANGEMAX
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26b4a588e67164b96db8256116466206d0274a5bc64caedbcb1ccf25135ce62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829598"
---
# <a name="tbm_setrangemax-message"></a>\_Сообщение ТБМ сетранжемакс

Задает максимальное логическое положение ползунка в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг перерисовки. Если этот параметр имеет **значение true**, то после установки диапазона значение TrackBar перерисовывается. Если этот параметр имеет **значение false**, сообщение задает диапазон, но не перерисовывает линейку.

</dd> <dt>

*lParam* 
</dt> <dd>

Максимальное положение ползунка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Если текущая позиция ползунка больше, чем максимальный размер, сообщение **ТБМ \_ сетранжемакс** устанавливает для ползунка новое максимальное значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТБМ \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**ТБМ \_ сетранжемин**](tbm-setrangemin.md)
</dt> </dl>

 

 





