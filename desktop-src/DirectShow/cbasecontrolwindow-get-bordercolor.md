---
description: Метод Get \_ BorderColor извлекает текущий цвет границы.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Метод CBaseControlWindow.get_BorderColor (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a351e794765f3dddb5275d8a588ca54ade06bb789ed720bfb17997fc11e358f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660758"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>Кбасеконтролвиндов. Get \_ BorderColor, метод

`get_BorderColor`Метод получает текущий цвет границы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Цвет* 
</dt> <dd>

Указатель на текущий цвет границы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Приложение может задать конечный прямоугольник, в котором должно отображаться видео. Этот прямоугольник отсчитывается относительно клиентской области окна. Если это сделано (по умолчанию всегда закрашивать все окно), то вокруг видео отображается граница. Это свойство влияет на цвет, используемый границей. Хотя параметр указан как тип **Long** , он фактически является значением **COLORREF** .

Эта функция-член предназначена для вызова внешними объектами через интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и, следовательно, блокирует критический раздел для синхронизации с соответствующим фильтром. Вызовите функцию члена [**кбасеконтролвиндов:: жетбордерколаур**](cbasecontrolwindow-getbordercolour.md) , чтобы получить это свойство, если не вызывается из внешнего объекта.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




