---
description: Метод Чекктаржетрект определяет, является ли целевой прямоугольник допустимым.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Кбасеконтролвидео. Чекктаржетрект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8444764af729f9536471a6a9df221cc118edb7d043112eb0b5351f45982d87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057324"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>Кбасеконтролвидео. Чекктаржетрект, метод

`CheckTargetRect`Метод определяет, является ли целевой прямоугольник допустимым.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птаржетрект* 
</dt> <dd>

Указатель на целевой прямоугольник для проверки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение E \_ INVALIDARG, если недопустимо; в противном случае возвращает значение \_ "Error" (ОК).

## <a name="remarks"></a>Remarks

Эта функция-член определяет, является ли запрошенный целевой прямоугольник допустимым. Так как конечный прямоугольник указывает на расположение в логическом клиенте окна, координаты могут быть отрицательными, хотя общая ширина и высота не могут быть равны нулю или отрицательному значению.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




