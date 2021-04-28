---
description: Ктрансформфилтер. ДеЦидебуфферсизе, метод ДеЦидебуфферсизе устанавливает требования к буферу выходного контакта.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Ктрансформфилтер. ДеЦидебуфферсизе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3276170f1256bba41aa075b0e5f06fb7becbcd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095152"
---
# <a name="ctransformfilterdecidebuffersize-method"></a>Ктрансформфилтер. ДеЦидебуфферсизе, метод

`DecideBufferSize`Метод задает требования к буферу выходного контакта.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паллок* 
</dt> <dd>

Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) на распределителье выходного контакта.

</dd> <dt>

*ппропинпутрекуест* 
</dt> <dd>

Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу из нисходящего входного ПИН-кода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Remarks

Метод [**ктрансформаутпутпин::D еЦидебуфферсизе**](ctransformoutputpin-decidebuffersize.md) для выходного контакта вызывает этот метод. Производный класс должен реализовывать этот метод. Дополнительные сведения см. в разделе [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




