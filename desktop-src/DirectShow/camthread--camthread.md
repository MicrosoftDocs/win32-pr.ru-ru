---
description: Метод деструктора Камсреад. ~ Камсреад.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Деструктор Камсреад. ~ Камсреад (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 884460b0c1af3b96a610a18b7475d2a144dc32bf308ea0e0191f0f526565726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662380"
---
# <a name="camthreadcamthread-destructor"></a>Деструктор Камсреад. ~ Камсреад

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Remarks

Деструктор вызывает метод [**камсреад:: Close**](camthread-close.md) , который ожидает выхода из потока.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




