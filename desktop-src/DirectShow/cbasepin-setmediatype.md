---
description: Метод Сетмедиатипе задает тип носителя для соединения.
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
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657665"
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

## <a name="remarks"></a>Комментарии

Этот метод устанавливает формат для соединения с закреплением. Перед вызовом этого метода ПИН-код вызывает метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) , чтобы определить, является ли тип мультимедиа допустимым. Поэтому предполагается, что параметр *ПЛТ* является допустимым типом носителя.

В базовом классе этот метод задает переменную члена [**кбасепин:: m \_ MT**](cbasepin-m-mt.md) и возвращает значение S \_ ОК. Производный класс может переопределить этот метод, если он требует уведомления, если задан тип мультимедиа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




