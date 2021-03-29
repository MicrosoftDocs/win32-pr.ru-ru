---
description: 'Метод Alloc выделяет память для буферов. Этот метод переопределяет метод Кбасеаллокатор:: Alloc.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Метод Цимажеаллокатор. Alloc (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657544"
---
# <a name="cimageallocatoralloc-method"></a>Цимажеаллокатор. Alloc, метод

`Alloc`Метод выделяет память для буферов. Этот метод переопределяет метод [**кбасеаллокатор:: Alloc**](cbaseallocator-alloc.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                   | Описание                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод вызывается методом [**кбасеаллокатор:: Commit**](cbaseallocator-commit.md) , когда фильтр фиксирует распределитель.

Этот метод создает список образцов мультимедиа, которые реализуются как объекты [**Цимажесампле**](cimagesample.md) . Каждый пример содержит аппаратно-независимый точечный рисунок GDI с помощью функции GDI **креатедибсектион** .

Внутренний метод вызывает [**Цимажеаллокатор:: креатедиб**](cimageallocator-createdib.md) для создания каждого DIB, а [**Цимажеаллокатор:: креатеимажесампле**](cimageallocator-createimagesample.md) — для создания каждого образца.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажеаллокатор**](cimageallocator.md)
</dt> </dl>

 

 




