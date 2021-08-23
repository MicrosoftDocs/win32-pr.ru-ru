---
description: Метод ИсспеЦиалсампле определяет, являются ли данные в очереди управляющим сообщением.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Каутпуткуеуе. ИсспеЦиалсампле, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c192196869f86e8d78da2f6b38a661373e115753d99e554f4b7a868eb0b484fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688224"
---
# <a name="coutputqueueisspecialsample-method"></a>Каутпуткуеуе. ИсспеЦиалсампле, метод

`IsSpecialSample`Метод определяет, являются ли данные в очереди управляющим сообщением.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псампле* 
</dt> <dd>

Указатель на элемент в очереди.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если *псампле* является управляющим сообщением, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Метод [**каутпуткуеуе:: QueueSample**](coutputqueue-queuesample.md) может получать управляющие сообщения в дополнение к примерам мультимедиа. Управляющее сообщение — это определенная константа (приведение к \_ типу Long PTR), которая указывает потоку выполнить действие. Управляющие сообщения не содержат данных мультимедиа. Дополнительные сведения см. в разделе **каутпуткуеуе:: QueueSample**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>аутпутк. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




