---
description: Метод Унинитиалисевиндов освобождает ресурсы окна.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Кбасевиндов. Унинитиалисевиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658044"
---
# <a name="cbasewindowuninitialisewindow-method"></a>Кбасевиндов. Унинитиалисевиндов, метод

`UninitialiseWindow`Метод освобождает ресурсы окна.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод освобождает ресурсы, которые были получены методом [**кбасевиндов:: инитиалисевиндов**](cbasewindow-initialisewindow.md) . Метод [**кбасевиндов::D оневисвиндов**](cbasewindow-donewithwindow.md) вызывает этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




