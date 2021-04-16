---
description: Метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Ктрансформфилтер. Бреакконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657025"
---
# <a name="ctransformfilterbreakconnect-method"></a>Ктрансформфилтер. Бреакконнект, метод

`BreakConnect`Метод освобождает ПИН-код из соединения.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*dir* 
</dt> <dd>

Член перечислимого [**типа \_ направления ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какое подключение к закреплению было разорвано (входные или выходные данные).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Методы [**ктрансформинпутпин:: бреакконнект**](ctransforminputpin-breakconnect.md) и [**Ктрансформаутпутпин:: бреакконнект**](ctransformoutputpin-breakconnect.md) вызывают этот метод, если соединение с закреплением разорвано. Этот метод не выполняет никаких действий в базовом классе. При переопределении метода [**чеккконнект**](ctransformfilter-checkconnect.md) Переопределите этот метод, чтобы освободить все ресурсы, полученные в методе **чеккконнект** , включая указатели интерфейса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




