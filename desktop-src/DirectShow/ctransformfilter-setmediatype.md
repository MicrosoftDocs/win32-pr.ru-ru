---
description: Метод Сетмедиатипе вызывается, когда тип мультимедиа задан на одном из ПИН-кодов фильтра.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Ктрансформфилтер. Сетмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679633"
---
# <a name="ctransformfiltersetmediatype-method"></a>Ктрансформфилтер. Сетмедиатипе, метод

`SetMediaType`Метод вызывается, когда тип мультимедиа задан на одном из ПИН-кодов фильтра.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*direction* 
</dt> <dd>

Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывая ПИН-код для фильтра (входные или выходные данные).

</dd> <dt>

*состоит* 
</dt> <dd>

Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Методы [**ктрансформинпутпин:: сетмедиатипе**](ctransforminputpin-setmediatype.md) и [**Ктрансформаутпутпин:: сетмедиатипе**](ctransformoutputpin-setmediatype.md) вызывают этот метод, если задан тип носителя ПИН-кода. Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




