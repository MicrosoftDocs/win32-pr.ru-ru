---
description: Метод Комплетеконнект завершает подключение ПИН-кода.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Ктрансформфилтер. Комплетеконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657452"
---
# <a name="ctransformfiltercompleteconnect-method"></a>Ктрансформфилтер. Комплетеконнект, метод

`CompleteConnect`Метод завершает соединение с закреплением.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*direction* 
</dt> <dd>

Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какой ПИН-код фильтра делает соединение.

</dd> <dt>

*прецеивепин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода в этой попытке подключения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Методы [**ктрансформинпутпин:: комплетеконнект**](ctransforminputpin-completeconnect.md) и [**Ктрансформаутпутпин:: комплетеконнект**](ctransformoutputpin-completeconnect.md) вызывают этот метод во время процесса подключения ПИН-кода. Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




