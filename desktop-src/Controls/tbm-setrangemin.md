---
title: Сообщение TBM_SETRANGEMIN (Коммктрл. h)
description: Задает минимальное логическое положение ползунка в TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- Элементы управления Windows для TBM_SETRANGEMIN сообщений
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
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988188"
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

## <a name="remarks"></a>Комментарии

Если текущая позиция ползунка меньше, чем новая минимальная, сообщение **ТБМ \_ сетранжемин** устанавливает положение ползунка в новое минимальное значение.

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

[**ТБМ \_ сетранжемакс**](tbm-setrangemax.md)
</dt> </dl>

 

 





