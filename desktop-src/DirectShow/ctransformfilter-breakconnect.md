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
ms.openlocfilehash: 3c4e77e28548c1f181cb5f8a6c106572d243314c5afd9d9126024e9b84fbe02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053814"
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

## <a name="remarks"></a>Remarks

Методы [**ктрансформинпутпин:: бреакконнект**](ctransforminputpin-breakconnect.md) и [**Ктрансформаутпутпин:: бреакконнект**](ctransformoutputpin-breakconnect.md) вызывают этот метод, если соединение с закреплением разорвано. Этот метод не выполняет никаких действий в базовом классе. При переопределении метода [**чеккконнект**](ctransformfilter-checkconnect.md) Переопределите этот метод, чтобы освободить все ресурсы, полученные в методе **чеккконнект** , включая указатели интерфейса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




