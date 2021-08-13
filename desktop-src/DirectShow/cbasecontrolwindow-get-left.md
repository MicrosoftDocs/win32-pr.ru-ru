---
description: Метод Get \_ Left извлекает текущую координату левого окна.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: Метод CBaseControlWindow.get_Left (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9317c1c061fe8528903bdd2e7129d0cfdc9e6dd67b9722841360d131e15cfb10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660527"
---
# <a name="cbasecontrolwindowget_left-method"></a>Кбасеконтролвиндов. Get \_ Left, метод

`get_Left`Метод получает текущую координату левого окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*плефт* 
</dt> <dd>

Указатель на левую координату в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Окно располагается на рабочем столе. Это расположение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу). Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow. Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.

Установка координат Left или Top перемещает окно влево и вверх соответственно; Эти координаты не влияют на ширину и высоту окна. Аналогично, задание ширины и высоты не влияет на координаты левой и верхней точек.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




