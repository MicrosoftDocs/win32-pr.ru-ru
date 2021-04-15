---
description: Метод Сеттаржетрект задает целевой прямоугольник.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Кдравимаже. Сеттаржетрект, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665473"
---
# <a name="cdrawimagesettargetrect-method"></a>Кдравимаже. Сеттаржетрект, метод

`SetTargetRect`Метод задает целевой прямоугольник.

## <a name="syntax"></a>Синтаксис


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птаржетрект* 
</dt> <dd>

Указатель на структуру **Rect** , определяющую новый целевой прямоугольник.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Фильтр-владелец должен вызывать этот метод, если исходный прямоугольник изменяется; Например, в ответ на вызов [**ибасиквидео:: сетдестинатионпоситион**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .

Перед вызовом этого метода проверьте прямоугольник, заданный в *птаржетрект*, относительно окна видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> </dl>

 

 




