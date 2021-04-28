---
description: 'Ксаурцесикинг. Сетрате, метод Сетрате задает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Сетрате.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Ксаурцесикинг. Сетрате, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098742"
---
# <a name="csourceseekingsetrate-method"></a>Ксаурцесикинг. Сетрате, метод

`SetRate`Метод задает скорость воспроизведения. Этот метод реализует метод [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*драте* 
</dt> <dd>

Скорость воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод обновляет значение переменной члена [**ксаурцесикинг:: m \_ дратесикинг**](csourceseeking-m-drateseeking.md) , а затем вызывает чистый виртуальный метод [**ксаурцесикинг:: чанжерате**](csourceseeking-changerate.md). Метод не проверяет параметр *драте* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




