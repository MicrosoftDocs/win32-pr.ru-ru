---
description: Метод Чеккмедиатипе определяет, принимает ли фильтр конкретный тип носителя.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Кбасерендерер. Чеккмедиатипе, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668748"
---
# <a name="cbaserenderercheckmediatype-method"></a>Кбасерендерер. Чеккмедиатипе, метод

`CheckMediaType`Метод определяет, принимает ли фильтр конкретный тип носителя.

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

Входной ПИН-код вызывает этот метод из собственного метода [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) . Производный класс должен реализовывать этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




