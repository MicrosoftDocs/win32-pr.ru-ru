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
ms.openlocfilehash: 880e82ca527972b5074ac290fda34ad1c7868a33cbbe1cad12885b56720cef99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635144"
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

## <a name="remarks"></a>Remarks

В базовом классе этот метод просто скрывает окно. Как правило, производный класс переопределяет этот метод, чтобы он также отправлял событие [**EC \_ усераборт**](ec-userabort.md) . Не переопределяйте метод, чтобы уничтожить окно. Вместо этого вызовите метод [**кбасевиндов::D оневисвиндов**](cbasewindow-donewithwindow.md) при уничтожении фильтра-владельца.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




