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
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094812"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансинплацефилтер**](ctransinplacefilter.md)
</dt> </dl>

 

 




