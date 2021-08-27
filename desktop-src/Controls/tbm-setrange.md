---
title: Сообщение TBM_SETRANGE (Коммктрл. h)
description: Задает диапазон минимальных и максимальных логических позиций ползунка в TrackBar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- элементы управления Windows сообщений TBM_SETRANGE
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcd4bf71cfcbc36e098bc83568bdf519209ec82cc9889b6b5ec3934d349f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061144"
---
# <a name="tbm_setrange-message"></a>\_Сообщение SETRANGE ТБМ

Задает диапазон минимальных и максимальных логических позиций ползунка в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг перерисовки. Если этот параметр имеет **значение true**, то после установки диапазона значение TrackBar перерисовывается. Если этот параметр имеет **значение false**, сообщение задает диапазон, но не перерисовывает линейку.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает минимальное положение ползунка, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает максимальное положение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Если текущая позиция ползунка находится за пределами нового диапазона, сообщение **ТБМ \_ SETRANGE** задает для ползунка значение нового максимального или минимального значения.

Так как это сообщение принимает 2 16-разрядные целочисленные значения без знака, максимальный диапазон, который может указывать это сообщение, — от 0 до 65 535. Чтобы указать большие значения диапазона, используйте сообщения [**ТБМ \_ Сетранжемин**](tbm-setrangemin.md) и [**ТБМ \_ сетранжемакс**](tbm-setrangemax.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТБМ \_ сетранжемакс**](tbm-setrangemax.md)
</dt> <dt>

[**ТБМ \_ сетранжемин**](tbm-setrangemin.md)
</dt> </dl>

 

