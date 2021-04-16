---
description: 'Метод GetObject получает состояние объекта (запущен, остановлен или приостановлен). Этот метод реализует метод Имедиафилтер:: WebMethod.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Метод Кбасемедиафилтер. WebMethod (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665279"
---
# <a name="cbasemediafiltergetstate-method"></a>Кбасемедиафилтер. метод State

`GetState`Метод получает состояние объекта (запущен, остановлен или приостановлен). Этот метод реализует метод [**имедиафилтер::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) WebMethod.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двмиллисекстимеаут* 
</dt> <dd>

Интервал времени ожидания (в миллисекундах).

</dd> <dt>

*Состояние* 
</dt> <dd>

Указатель на переменную, которая получает член перечислимого [**типа \_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) , указывая состояние объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="remarks"></a>Комментарии

В базовом классе все переходы состояния являются синхронными, а параметр *двмиллисекстимеаут* игнорируется. Если производный класс выполняет асинхронные переходы состояний, он должен переопределять этот метод для ожидания во время переходов состояния с истечением времени ожидания *двмиллисекстимеаут* миллисекунд.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




