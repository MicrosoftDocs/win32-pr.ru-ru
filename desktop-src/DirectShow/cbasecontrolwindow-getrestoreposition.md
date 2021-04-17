---
description: Метод Жетресторепоситион извлекает расположение, в которое окно будет восстановлено, если оно не развернуто или не развернуто.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Кбасеконтролвиндов. Жетресторепоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657317"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>Кбасеконтролвиндов. Жетресторепоситион, метод

`GetRestorePosition`Метод получает расположение, в которое будет восстановлено окно, если оно не развернуто или не развернуто.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*плефт* 
</dt> <dd>

Указатель на значение для самой левой координаты.

</dd> <dt>

*птоп* 
</dt> <dd>

Указатель на значение в верхней части окна.

</dd> <dt>

*пвидс* 
</dt> <dd>

Указатель на значение ширины окна.

</dd> <dt>

*феигхт* 
</dt> <dd>

Указатель на значение высоты окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Это то же самое, что и значения, возвращаемые функцией [**кбасеконтролвиндов:: жетвиндовпоситион**](cbasecontrolwindow-getwindowposition.md) , если окно не развернуто или не уменьшено.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




