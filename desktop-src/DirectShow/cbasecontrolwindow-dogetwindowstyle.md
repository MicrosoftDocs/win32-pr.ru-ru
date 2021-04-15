---
description: Метод Дожетвиндовстиле извлекает текущие стандартные или расширенные стили окна.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Кбасеконтролвиндов. Дожетвиндовстиле, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668519"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>Кбасеконтролвиндов. Дожетвиндовстиле, метод

`DoGetWindowStyle`Метод извлекает текущие стандартные или расширенные стили окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстиле* 
</dt> <dd>

Указатель на переменную, которая получает сведения о стиле.

</dd> <dt>

*виндовлонг* 
</dt> <dd>

Значение, указывающее, какие стили следует извлечь. Должна быть одной из следующих:



|              |                                      |
|--------------|--------------------------------------|
| \_стиль ГВЛ   | Получение стилей окна.          |
| ГВЛ \_ операторе EXSTYLE | Получение расширенных стилей окна. |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция члена вызывает функцию Win32 **жетвиндовлонг** для получения стиля окна. Он вызывается функциями-членами [**кбасеконтролвиндов:: Get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) и [**кбасеконтролвиндов:: Get \_ виндовстиликс**](cbasecontrolwindow-get-windowstyleex.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




