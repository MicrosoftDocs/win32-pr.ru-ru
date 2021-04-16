---
description: Метод «разместить \_ BorderColor» изменяет цвет границы.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Метод CBaseControlWindow.put_BorderColor (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657350"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a>Кбасеконтролвиндов. размещение \_ BorderColor, метод

`put_BorderColor`Метод изменяет цвет границы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Цвет* 
</dt> <dd>

Новый цвет границы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Приложение может установить конечный прямоугольник, в котором должно отображаться видео. Этот прямоугольник отсчитывается относительно клиентской области окна. Если это сделано (по умолчанию всегда закрашивать все окно), то вокруг видео отображается граница. Это свойство влияет на цвет, используемый границей. Хотя параметр указан как тип **Long** , он фактически является значением **COLORREF** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




