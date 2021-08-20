---
description: Ктрансформфилтер. Чеккконнект, метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Ктрансформфилтер. Чеккконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a148e9edbc1cef42ecc2d1158dd18afcc908cf4d7549912b52f363aaa54cedb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953633"
---
# <a name="ctransformfiltercheckconnect-method"></a>Ктрансформфилтер. Чеккконнект, метод

`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*dir* 
</dt> <dd>

Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какой ПИН-код фильтра делает соединение.

</dd> <dt>

*ппин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода в этой попытке подключения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Методы [**ктрансформинпутпин:: чеккконнект**](ctransforminputpin-checkconnect.md) и [**Ктрансформаутпутпин:: чеккконнект**](ctransformoutputpin-checkconnect.md) вызывают этот метод во время процесса подключения ПИН-кода. Этот метод не выполняет никаких действий в базовом классе. Производный класс может переопределить его. Например, производный класс может запросить другой ПИН-код для определенного интерфейса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




