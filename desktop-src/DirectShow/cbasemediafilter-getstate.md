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
ms.openlocfilehash: 2a4c70412311be5ea4843a823e961fae34de2974f7365f51286ff6da36e41dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966704"
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

## <a name="remarks"></a>Remarks

В базовом классе все переходы состояния являются синхронными, а параметр *двмиллисекстимеаут* игнорируется. Если производный класс выполняет асинхронные переходы состояний, он должен переопределять этот метод для ожидания во время переходов состояния с истечением времени ожидания *двмиллисекстимеаут* миллисекунд.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




