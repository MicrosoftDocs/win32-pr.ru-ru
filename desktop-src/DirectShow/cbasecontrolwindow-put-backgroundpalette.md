---
description: Метод размещения \_ баккграундпалетте устанавливает флаг для реализации палитры в фоновом режиме.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Метод CBaseControlWindow.put_BackgroundPalette (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657351"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a>Кбасеконтролвиндов. размещение \_ метода баккграундпалетте

`put_BackgroundPalette`Метод задает флаг для реализации палитры в фоновом режиме.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*баккграундпалетте* 
</dt> <dd>

Логический флаг автоматизации (0 — отключено, 1 — включено).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Для воспроизведения видео в другом приложении или документе может потребоваться использовать собственную палитру. Он может задать, чтобы видео использовало текущую палитру переднего плана, а не собственную в качестве палитры фона, установив для этого флага значение 1. Если задано значение 0, окно будет установлено и использовать собственную предпочтительную палитру. Запрос использования другой палитры в окне приведет к значительному снижению производительности.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




