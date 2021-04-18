---
description: 'Метод StartAt информирует ПИН-код о начале доставки данных. Этот метод реализует метод Иамстреамконтрол:: StartAt.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Метод Кбасестреамконтрол. StartAt (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656835"
---
# <a name="cbasestreamcontrolstartat-method"></a>Кбасестреамконтрол. StartAt, метод

`StartAt`Метод информирует ПИН-код, когда следует начать доставку данных. Этот метод реализует метод [**иамстреамконтрол:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птстарт* 
</dt> <dd>

Указатель на значение [**\_ времени ссылки**](reference-time.md) , указывающее, когда ПИН-код должен начать доставку данных.

</dd> <dt>

*двкукие* 
</dt> <dd>

Указывает значение для отправки вместе с уведомлением о запуске.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Стрмктл. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасестреамконтрол**](cbasestreamcontrol.md)
</dt> </dl>

 

 




