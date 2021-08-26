---
title: Сообщение TBM_SETRANGEMIN (Коммктрл. h)
description: Задает минимальное логическое положение ползунка в TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- элементы управления Windows сообщений TBM_SETRANGEMIN
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35cbb162b42636d886cb5e41eb9ba6de1a2101a8327ff8ddffbc71c57fa6735
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046074"
---
# <a name="tbm_setrangemin-message"></a>\_Сообщение ТБМ сетранжемин

Задает минимальное логическое положение ползунка в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг перерисовки. Если этот параметр имеет **значение true**, сообщение перерисовывается после установки диапазона. Если этот параметр имеет **значение false**, сообщение задает диапазон, но не перерисовывает линейку.

</dd> <dt>

*lParam* 
</dt> <dd>

Минимальная позиция ползунка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Если текущая позиция ползунка меньше, чем новая минимальная, сообщение **ТБМ \_ сетранжемин** устанавливает положение ползунка в новое минимальное значение.

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

[**ТБМ \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**ТБМ \_ сетранжемакс**](tbm-setrangemax.md)
</dt> </dl>

 

 





