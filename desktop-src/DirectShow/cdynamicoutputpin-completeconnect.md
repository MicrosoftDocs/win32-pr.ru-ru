---
description: Кдинамикаутпутпин. Комплетеконнект, метод Комплетеконнект завершает соединение с входным закреплением.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Кдинамикаутпутпин. Комплетеконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fa15c84b9d9e0b686e17110c656b74161687705
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095742"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a>Кдинамикаутпутпин. Комплетеконнект, метод

`CompleteConnect`Метод завершает соединение с входным закреплением.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прецеивепин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного контакта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасеаутпутпин:: комплетеконнект**](cbaseoutputpin-completeconnect.md) . Для поддержки динамического повторного подключения этот метод фиксирует распределитель, если фильтр активен. В базовом классе соединения могут происходить только в том случае, если фильтр остановлен, поэтому распределитель всегда фиксируется в методе [**кбасеаутпутпин:: Active**](cbaseoutputpin-active.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




