---
description: Метод размещения \_ ширины задает ширину окна.
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: Метод CBaseControlWindow.put_Width (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f32175fe2b86f3b05105f5627cf1e02b2509e25ee12cc415cd88ea2baba5536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635714"
---
# <a name="cbasecontrolwindowput_width-method"></a>Кбасеконтролвиндов. размещение \_ метода Width

`put_Width`Метод задает ширину окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Width* 
</dt> <dd>

Новая ширина окна в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Окно располагается на рабочем столе. Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу). Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow. Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.

Установка координат Left или Top приводит к перемещению окна влево или вверх соответственно. Эти координаты не влияют на ширину и высоту окна. Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




