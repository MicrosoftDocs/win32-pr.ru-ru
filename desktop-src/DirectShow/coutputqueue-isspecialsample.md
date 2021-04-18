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
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665339"
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

## <a name="remarks"></a>Комментарии

Метод [**каутпуткуеуе:: QueueSample**](coutputqueue-queuesample.md) может получать управляющие сообщения в дополнение к примерам мультимедиа. Управляющее сообщение — это определенная константа (приведение к \_ типу Long PTR), которая указывает потоку выполнить действие. Управляющие сообщения не содержат данных мультимедиа. Дополнительные сведения см. в разделе **каутпуткуеуе:: QueueSample**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




