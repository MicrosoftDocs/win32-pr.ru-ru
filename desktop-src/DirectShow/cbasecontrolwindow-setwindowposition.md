---
description: Метод Сетвиндовпоситион задает расположение окна на рабочем столе.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Кбасеконтролвиндов. Сетвиндовпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657598"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>Кбасеконтролвиндов. Сетвиндовпоситион, метод

`SetWindowPosition`Метод задает расположение окна на рабочем столе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Слева* 
</dt> <dd>

Новая левая координата.

</dd> <dt>

*Top* 
</dt> <dd>

Новая Верхняя координата.

</dd> <dt>

*Width* 
</dt> <dd>

Ширина окна.

</dd> <dt>

*Height* 
</dt> <dd>

Высота окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




