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
ms.openlocfilehash: bf6c7793af3cb7866ddaaaae8823acd91ed10ac71d939af8bc9e71eff768d75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657659"
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

## <a name="remarks"></a>Remarks

Этот метод сохраняет новую ширину и высоту. Чтобы получить эти значения, вызовите методы [**кбасевиндов:: жетвиндовхеигхт**](cbasewindow-getwindowheight.md) и [**Кбасевиндов:: жетвиндоввидс**](cbasewindow-getwindowwidth.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




