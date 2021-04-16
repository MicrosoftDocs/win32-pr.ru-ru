---
description: Метод OnClose обрабатывает сообщения WM \_ Close.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Метод Кбасевиндов. OnClose (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657039"
---
# <a name="cbasewindowonclose-method"></a>Метод Кбасевиндов. OnClose

`OnClose`Метод обрабатывает сообщения WM \_ Close.

## <a name="syntax"></a>Синтаксис


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true**.

## <a name="remarks"></a>Комментарии

В базовом классе этот метод просто скрывает окно. Как правило, производный класс переопределяет этот метод, чтобы он также отправлял событие [**EC \_ усераборт**](ec-userabort.md) . Не переопределяйте метод, чтобы уничтожить окно. Вместо этого вызовите метод [**кбасевиндов::D оневисвиндов**](cbasewindow-donewithwindow.md) при уничтожении фильтра-владельца.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




