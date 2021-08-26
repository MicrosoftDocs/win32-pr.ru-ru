---
description: Метод Креатедиб создает независимый от устройства точечный рисунок GDI (DIB). DIB выделяется в общем блоке мемпори, который удаляет операцию копирования, когда фильтр-владелец блитс изображение.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Цимажеаллокатор. Креатедиб, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a629831ea50219b47500c0637cfeaebfbc95b1ee99a8b9d3872a655ab5485c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055484"
---
# <a name="cimageallocatorcreatedib-method"></a>Цимажеаллокатор. Креатедиб, метод

`CreateDIB`Метод создает аппаратно-независимый точечный рисунок GDI (DIB). DIB выделяется в общем блоке мемпори, который удаляет операцию копирования, когда фильтр-владелец блитс изображение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Неразмерность* 
</dt> <dd>

Размер точечного рисунка.

</dd> <dt>

*Дибдата* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на структуру [**дибдата**](dibdata.md) . Метод заполняет эту структуру сведениями об элементе DIB.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК, если успешно, или код ошибки в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажеаллокатор**](cimageallocator.md)
</dt> <dt>

[**Цимажеаллокатор:: Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




