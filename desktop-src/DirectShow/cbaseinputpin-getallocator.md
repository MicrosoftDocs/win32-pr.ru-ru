---
description: Кбасеинпутпин. метод распределителя — метод метода распределителя извлекает распределитель памяти, предложенный этим ПИН-кодом. Этот метод реализует метод Имеминпутпин::/распределителя.
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Метод Кбасеинпутпин. методом перераспределения (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72aaf6bb4c1ff8bf108086a8a42a618267c4bc06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099721"
---
# <a name="cbaseinputpingetallocator-method"></a>Кбасеинпутпин. метод распределения

`GetAllocator`Метод извлекает распределитель памяти, предложенный этим ПИН-кодом. Этот метод реализует метод [**имеминпутпин::/распределителя**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппаллокатор* 
</dt> <dd>

Адрес переменной, которая получает указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК в случае успеха или код ошибки из функции **CoCreateInstance** .

## <a name="remarks"></a>Remarks

Этот метод создает объект [**кмемаллокатор**](cmemallocator.md) . Переопределите этот метод, если фильтр использует распределитель из подчиненного ПИН-кода или пользовательского распределителя.

Если метод выполнен успешно, то интерфейс **имемаллокатор** имеет необработанный счетчик ссылок. Не забудьте освободить его по завершении.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




