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
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688773"
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

## <a name="remarks"></a>Комментарии

Эта функция-член определяет, является ли запрошенный целевой прямоугольник допустимым. Так как конечный прямоугольник указывает на расположение в логическом клиенте окна, координаты могут быть отрицательными, хотя общая ширина и высота не могут быть равны нулю или отрицательному значению.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




