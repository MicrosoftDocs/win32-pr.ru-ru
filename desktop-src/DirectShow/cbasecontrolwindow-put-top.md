---
description: Метод размещения \_ Top задает координату верхнего окна.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: Метод CBaseControlWindow.put_Top (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdbce19c3caf4129b1f224a740b27209b855a1f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658068"
---
# <a name="cbasecontrolwindowput_top-method"></a>Метод Кбасеконтролвиндов. Where \_ Top

`put_Top`Метод задает координату верхнего окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Top* 
</dt> <dd>

Новая Верхняя координата (в пикселях).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Окно располагается на рабочем столе. Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу). Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow. Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.

Установка координат Left или Top перемещает окно влево или вверх соответственно; Эти координаты не влияют на ширину и высоту окна. Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




