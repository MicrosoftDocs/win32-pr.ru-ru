---
description: Метод метода распределителе извлекает распределитель памяти, предложенный этим ПИН-кодом. Этот метод реализует метод Имеминпутпин::/распределителя.
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
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657066"
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

## <a name="remarks"></a>Комментарии

Этот метод создает объект [**кмемаллокатор**](cmemallocator.md) . Переопределите этот метод, если фильтр использует распределитель из подчиненного ПИН-кода или пользовательского распределителя.

Если метод выполнен успешно, то интерфейс **имемаллокатор** имеет необработанный счетчик ссылок. Не забудьте освободить его по завершении.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




