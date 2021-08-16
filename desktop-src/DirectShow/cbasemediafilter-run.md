---
description: 'Метод Run запускает объект. Этот метод реализует метод Имедиафилтер:: Run.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Метод Кбасемедиафилтер. Run (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 73ab65404b6946a1cf220db54789df1234e14bf815c44633d3237ab50e04e2e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823694"
---
# <a name="cbasemediafilterrun-method"></a>Кбасемедиафилтер. Run, метод

`Run`Метод выполняет объект. Этот метод реализует метод [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тстарт* 
</dt> <dd>

Время в ссылке, соответствующее времени потока 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Если объект остановлен, этот метод приостанавливает работу объекта, вызывая метод [**кбасемедиафилтер::P Аусе**](cbasemediafilter-pause.md) . Затем он задает для переменной члена [**\_ состояния кбасемедиафилтер:: m**](cbasemediafilter-m-state.md) состояние \_ работает.

Время потока вычисляется как текущее время ссылки минус *тстарт*. Пример носителя с нулевой меткой времени должен быть визуализирован во время *тстарт*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




