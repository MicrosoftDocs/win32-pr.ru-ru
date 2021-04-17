---
description: Метод Филлбуффер заполняет пример носителя данными.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Метод Ксаурцестреам. Филлбуффер (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685384"
---
# <a name="csourcestreamfillbuffer-method"></a>Ксаурцестреам. Филлбуффер, метод

`FillBuffer`Метод заполняет пример носителя данными.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                             | Описание              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Конец потока<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно<br/>       |



 

## <a name="remarks"></a>Комментарии

Производный класс должен реализовывать этот метод.

Образец носителя, указанный для этого метода, не имеет штампов времени. Производный класс должен вызвать метод [**имедиасампле:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) , чтобы задать метки времени. При необходимости для типа мультимедиа производный класс также должен задавать время носителя, вызывая метод [**имедиасампле:: сетмедиатиме**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) . Дополнительные сведения см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).

Возвращает \_ значение false в конце потока. В результате класс **ксаурцестреам** отправляет уведомление об окончании потока и останавливает цикл обработки буфера. Дополнительные сведения см. в разделе [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




