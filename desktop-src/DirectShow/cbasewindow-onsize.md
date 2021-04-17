---
description: Метод OnSize обрабатывает \_ сообщения размером WM.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Метод Кбасевиндов. OnSize (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675087"
---
# <a name="cbasewindowonsize-method"></a>Кбасевиндов. OnSize, метод

`OnSize`Метод обрабатывает \_ сообщения размером WM.

## <a name="syntax"></a>Синтаксис


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Width* 
</dt> <dd>

Ширина клиентской области в пикселях.

</dd> <dt>

*Height* 
</dt> <dd>

Высота клиентской области в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true**.

## <a name="remarks"></a>Комментарии

Этот метод сохраняет новую ширину и высоту. Чтобы получить эти значения, вызовите методы [**кбасевиндов:: жетвиндовхеигхт**](cbasewindow-getwindowheight.md) и [**Кбасевиндов:: жетвиндоввидс**](cbasewindow-getwindowwidth.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




