---
description: Определяет, является ли исходный прямоугольник допустимым.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Кбасеконтролвидео. Чекксаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf7ac41d626eceee048afc4671a5e171e7164adfbd9a941b1b70bc85ea988c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873014"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>Кбасеконтролвидео. Чекксаурцерект, метод

Определяет, является ли исходный прямоугольник допустимым.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псаурцерект* 
</dt> <dd>

Указатель на исходный прямоугольник для проверки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение E \_ INVALIDARG, если недопустимо; в противном случае возвращает значение \_ "Error" (ОК).

## <a name="remarks"></a>Remarks

Эта функция члена проверяет, что запрошенный исходный прямоугольник не превышает доступный исходный видеоролик. Координаты Left и Top не могут быть отрицательными, а ширина и высота не могут превышать правую и нижнюю часть видео.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




