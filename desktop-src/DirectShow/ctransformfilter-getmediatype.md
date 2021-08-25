---
description: Ктрансформфилтер. Жетмедиатипе, метод Жетмедиатипе извлекает предпочтительный тип мультимедиа для выходного ПИН-кода.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Ктрансформфилтер. Жетмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b471ac42ceb44f5e65a2ac08365bf97ab0e3157816b772b331cde0fa0b13bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907534"
---
# <a name="ctransformfiltergetmediatype-method"></a>Ктрансформфилтер. Жетмедиатипе, метод

`GetMediaType`Метод извлекает предпочтительный тип мультимедиа для выходного контакта.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
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

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                                            | Описание                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                   | Успешно.<br/>              |
| <dl> <dt>**VFW \_ S \_ больше \_ \_ элементов**</dt> </dl> | Индекс вне допустимого диапазона.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Индекс меньше нуля.<br/> |



 

## <a name="remarks"></a>Remarks

Метод [**ктрансформаутпутпин:: жетмедиатипе**](ctransformoutputpin-getmediatype.md) выходного контакта вызывает этот метод. Производный класс должен реализовывать этот метод. Дополнительные сведения см. в разделе [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




