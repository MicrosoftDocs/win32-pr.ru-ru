---
description: Ктрансинплацефилтер. Жетмедиатипе, метод Жетмедиатипе извлекает предпочтительный тип мультимедиа для выходного ПИН-кода.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Ктрансинплацефилтер. Жетмедиатипе, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a714d3dba30b3038d6c04ecedd51db4196a3c4d899d7c607dd12f9a068f8a803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079304"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>Ктрансинплацефилтер. Жетмедиатипе, метод

`GetMediaType`Метод извлекает предпочтительный тип мультимедиа для выходного контакта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Интерфейс* 
</dt> <dd>

Значение индекса, начинающееся с нуля.

</dd> <dt>

*пмедиатипе* 
</dt> <dd>

Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ непредвиденное значение E.

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) . В классе **ктрансинплацефилтер** каждый ПИН-код вызывает противоположный подключенный ПИН-код для перечисления предпочтительных типов мультимедиа. Входной ПИН-код вызывает входной ПИН-код подчиненного фильтра, а выходной закрепление вызывает выходной ПИН-код вышестоящего фильтра. Поэтому метод фильтра никогда не `GetMediaType` вызывается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансип. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансинплацефилтер**](ctransinplacefilter.md)
</dt> </dl>

 

 




