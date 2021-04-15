---
title: Сообщение TBM_SETRANGEMAX (Коммктрл. h)
description: Задает максимальное логическое положение ползунка в TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- Элементы управления Windows для TBM_SETRANGEMAX сообщений
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
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489027"
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

## <a name="remarks"></a>Комментарии

Если текущая позиция ползунка больше, чем максимальный размер, сообщение **ТБМ \_ сетранжемакс** устанавливает для ползунка новое максимальное значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТБМ \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**ТБМ \_ сетранжемин**](tbm-setrangemin.md)
</dt> </dl>

 

 





