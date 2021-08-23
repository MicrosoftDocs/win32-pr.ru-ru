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
ms.openlocfilehash: b9a522dd2b10e7ced60b65c84621bb1817be4b8abbca8656ba23f49e95fe3892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687404"
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
| <dl> <dt>**\_ОК**</dt> </dl>    | Success<br/>       |



 

## <a name="remarks"></a>Remarks

Производный класс должен реализовывать этот метод.

Образец носителя, указанный для этого метода, не имеет штампов времени. Производный класс должен вызвать метод [**имедиасампле:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) , чтобы задать метки времени. При необходимости для типа мультимедиа производный класс также должен задавать время носителя, вызывая метод [**имедиасампле:: сетмедиатиме**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) . Дополнительные сведения см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).

Возвращает \_ значение false в конце потока. В результате класс **ксаурцестреам** отправляет уведомление об окончании потока и останавливает цикл обработки буфера. Дополнительные сведения см. в разделе [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




