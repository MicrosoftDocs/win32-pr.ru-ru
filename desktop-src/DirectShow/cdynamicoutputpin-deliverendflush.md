---
description: Кдинамикаутпутпин. Деливерендфлуш, метод Деливерендфлуш запрашивает подключенный входной ПИН-код для завершения операции очистки.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Кдинамикаутпутпин. Деливерендфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095712"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>Кдинамикаутпутпин. Деливерендфлуш, метод

`DeliverEndFlush`Метод запрашивает подключенный входной ПИН-код для завершения операции очистки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасеаутпутпин::D еливерендфлуш**](cbaseoutputpin-deliverendflush.md) . Он сбрасывает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




