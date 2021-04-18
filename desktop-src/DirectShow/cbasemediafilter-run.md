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
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656925"
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

## <a name="remarks"></a>Комментарии

Если объект остановлен, этот метод приостанавливает работу объекта, вызывая метод [**кбасемедиафилтер::P Аусе**](cbasemediafilter-pause.md) . Затем он задает для переменной члена [**\_ состояния кбасемедиафилтер:: m**](cbasemediafilter-m-state.md) состояние \_ работает.

Время потока вычисляется как текущее время ссылки минус *тстарт*. Пример носителя с нулевой меткой времени должен быть визуализирован во время *тстарт*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




