---
description: Метод Перформанцеалигнвиндов совмещает расположение окна до границ DWORD, что обеспечивает максимальную производительность.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Кбасевиндов. Перформанцеалигнвиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3c077b6cf00f61565124f3d79ad905f6d34a3d8da50d58396e2df1bd35b0d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016472"
---
# <a name="cbasewindowperformancealignwindow-method"></a>Кбасевиндов. Перформанцеалигнвиндов, метод

`PerformanceAlignWindow`Метод совмещает расположение окна до границ **DWORD** , что обеспечивает максимальную производительность.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод выровняйте левый и верхний края окна до границ DWORD, что может повысить производительность. Если окно имеет родителя, метод возвращает значение S ОК, \_ но выполняет выравнивание.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




