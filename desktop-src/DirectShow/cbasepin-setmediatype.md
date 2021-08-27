---
description: Кбасепин. Сетмедиатипе, метод Сетмедиатипе задает тип носителя для соединения.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Кбасепин. Сетмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e71047b5063a5975266e5e24db936a0baf9e7b65e81ce29b402ccce4638267a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108644"
---
# <a name="cbasepinsetmediatype-method"></a>Кбасепин. Сетмедиатипе, метод

`SetMediaType`Метод задает тип носителя для соединения.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод устанавливает формат для соединения с закреплением. Перед вызовом этого метода ПИН-код вызывает метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) , чтобы определить, является ли тип мультимедиа допустимым. Поэтому предполагается, что параметр *ПЛТ* является допустимым типом носителя.

В базовом классе этот метод задает переменную члена [**кбасепин:: m \_ MT**](cbasepin-m-mt.md) и возвращает значение S \_ ОК. Производный класс может переопределить этот метод, если он требует уведомления, если задан тип мультимедиа.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




