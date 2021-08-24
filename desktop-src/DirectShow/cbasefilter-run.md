---
description: 'Метод Run запускает фильтр. Этот метод реализует метод Имедиафилтер:: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Метод Кбасефилтер. Run (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6259e6ce00b0a2f93e0b71d6b44d1c6ed4aa65eaadca21ed0a78f1d16d98a42b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793284"
---
# <a name="cbasefilterrun-method"></a>Кбасефилтер. Run, метод

`Run`Метод выполняет фильтр. Этот метод реализует метод [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

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

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.

## <a name="remarks"></a>Remarks

Если фильтр остановлен, этот метод приостанавливает фильтр, вызывая метод [**кбасефилтер::P Аусе**](cbasefilter-pause.md) . Затем он вызывает метод [**кбасепин:: Run**](cbasepin-run.md) для каждого подключенного контакта фильтра. Наконец, он устанавливает переменную члена [**\_ состояния кбасефилтер:: m**](cbasefilter-m-state.md) в состояние \_ работает.

Время потока вычисляется как текущее время ссылки минус *тстарт*. Пример носителя с нулевой меткой времени должен быть визуализирован во время *тстарт*.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




