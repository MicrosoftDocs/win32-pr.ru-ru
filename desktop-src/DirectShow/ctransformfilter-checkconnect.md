---
description: Метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
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
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657024"
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

## <a name="remarks"></a>Комментарии

Методы [**ктрансформинпутпин:: чеккконнект**](ctransforminputpin-checkconnect.md) и [**Ктрансформаутпутпин:: чеккконнект**](ctransformoutputpin-checkconnect.md) вызывают этот метод во время процесса подключения ПИН-кода. Этот метод не выполняет никаких действий в базовом классе. Производный класс может переопределить его. Например, производный класс может запросить другой ПИН-код для определенного интерфейса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




