---
description: Метод Сетсаурцерект задает исходный прямоугольник.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Кдравимаже. Сетсаурцерект, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665248"
---
# <a name="cdrawimagesetsourcerect-method"></a>Кдравимаже. Сетсаурцерект, метод

`SetSourceRect`Метод задает исходный прямоугольник.

## <a name="syntax"></a>Синтаксис


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псаурцерект* 
</dt> <dd>

Указатель на структуру **Rect** , определяющую новый исходный прямоугольник.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Фильтр-владелец должен вызывать этот метод, если исходный прямоугольник изменяется; Например, в ответ на вызов [**ибасиквидео:: сетсаурцепоситион**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .

Проверьте прямоугольник, указанный в *псаурцерект* , перед вызовом этого метода, чтобы убедиться, что он не выходит за пределы собственного видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> </dl>

 

 




