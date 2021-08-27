---
description: 'Массив выборок размера Каутпуткуеуе:: m \_ лбатчсизе.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Элемент Каутпуткуеуе:: m_ppSamples (Аутпутк. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0b27a356727fc317eb1818ecd548d944e3c4b2ace9cc11e0834bf1cf551c9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103154"
---
# <a name="coutputqueuem_ppsamples-member"></a>Элемент Каутпуткуеуе:: m \_ ппсамплес

Массив выборок размера [**каутпуткуеуе:: m \_ лбатчсизе**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Синтаксис


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Remarks

Рабочий поток извлекает образцы из очереди и помещает их в этот массив. Он передает массив в метод [**имеминпутпин:: рецеивемултипле**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) . Если объект не использует рабочий поток, объект помещает примеры непосредственно в этот массив. Переменная члена [**\_ списка каутпуткуеуе:: m**](coutputqueue-m-list.md) содержит очередь.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>аутпутк. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




