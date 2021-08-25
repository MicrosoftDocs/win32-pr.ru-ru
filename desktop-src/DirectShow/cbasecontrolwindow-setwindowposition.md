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
ms.openlocfilehash: 2734c93d1a3d3d3ea29e037d1bf85baacd5358a69f08d1517012c3eb250ab8ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635463"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




