---
title: Сообщение TBM_GETTICPOS (Коммктрл. h)
description: Извлекает текущее физическое расположение деления в TrackBar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- элементы управления Windows сообщений TBM_GETTICPOS
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d191034fc1551d4ffc1840498e352e2f3cd82985f1bbc5a7ae8d5350a41fb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046344"
---
# <a name="tbm_getticpos-message"></a>\_Сообщение ТБМ жеттикпос

Извлекает текущее физическое расположение деления в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс, указывающий деление. Позиции первой и последней делений не доступны напрямую через это сообщение.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает расстояние в клиентских координатах от левого или верхнего края клиентской области TrackBar до указанного деления. Возвращаемое значение — это координата x деления горизонтальной линейки или координаты y для вертикальной линейки. Если параметр *wParam* не является допустимым индексом, возвращается значение-1.

## <a name="remarks"></a>Remarks

Поскольку первая и последняя деления недоступны через это сообщение, допустимые индексы смещаются относительно их позиции на TrackBar. Если разница между [**ТБМ \_ Жетранжемин**](tbm-getrangemin.md) и [**ТБМ \_ жетранжемакс**](tbm-getrangemax.md) меньше двух, то допустимый индекс отсутствует, и это сообщение не будет выполнено.

Ниже показано отношение между тактами на TrackBar, тактами, доступными через это сообщение, и индексами, начинающимися с нуля.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





