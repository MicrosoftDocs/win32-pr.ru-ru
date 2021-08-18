---
description: Метод Фастрендер рисует изображение видео с помощью функций BitBlt или Стретчблт.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Кдравимаже. Фастрендер, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146c3736f7aaa89fc9a724d9dd7e4bfb58160e21e2de57f40a8e855c8a3c1446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043613"
---
# <a name="cdrawimagefastrender-method"></a>Кдравимаже. Фастрендер, метод

`FastRender`Метод рисует изображение видео с помощью функций **BitBlt** или **стретчблт** .

## <a name="syntax"></a>Синтаксис


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца, который содержит изображение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод [**кдравимаже::D равимаже**](cdrawimage-drawimage.md) вызывает этот метод, но только в том случае, если распределитель для соединения является объектом [**Цимажеаллокатор**](cimageallocator.md) . В этом случае пример носителя гарантированно будет объектом [**Цимажесампле**](cimagesample.md) . Объект **Цимажесампле** использует функцию **креатедибсектион** для выделения общей памяти для точечного рисунка, что дает возможность рисовать изображение с помощью **BitBlt** или **стретчблт**.

Этот метод вызывает **BitBlt** , если прямоугольники источника и недопустимая точно совпадают, или **стретчблт** в противном случае.

Если фильтр не владеет распределителем, метод **DrawImage** использует [**Кдравимаже:: словрендер**](cdrawimage-slowrender.md) для рисования изображения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> </dl>

 

 




