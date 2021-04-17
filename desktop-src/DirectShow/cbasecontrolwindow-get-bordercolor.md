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
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665281"
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

## <a name="remarks"></a>Комментарии

Приложение может задать конечный прямоугольник, в котором должно отображаться видео. Этот прямоугольник отсчитывается относительно клиентской области окна. Если это сделано (по умолчанию всегда закрашивать все окно), то вокруг видео отображается граница. Это свойство влияет на цвет, используемый границей. Хотя параметр указан как тип **Long** , он фактически является значением **COLORREF** .

Эта функция-член предназначена для вызова внешними объектами через интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и, следовательно, блокирует критический раздел для синхронизации с соответствующим фильтром. Вызовите функцию члена [**кбасеконтролвиндов:: жетбордерколаур**](cbasecontrolwindow-getbordercolour.md) , чтобы получить это свойство, если не вызывается из внешнего объекта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




