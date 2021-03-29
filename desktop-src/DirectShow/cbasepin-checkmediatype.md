---
description: Метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Кбасепин. Чеккмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e203851a44a5468567e75ee8c0cc955f8ad0278a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657956"
---
# <a name="cbasepincheckmediatype-method"></a>Кбасепин. Чеккмедиатипе, метод

`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_Если предложенный тип мультимедиа приемлем, возвращается значение S. В противном случае возвращает \_ значение S false или код ошибки.

## <a name="remarks"></a>Комментарии

Производный класс должен переопределять этот чистый виртуальный метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




