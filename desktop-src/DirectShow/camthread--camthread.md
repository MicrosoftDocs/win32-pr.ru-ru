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
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096442"
---
# <a name="camthreadcamthread-destructor"></a>Деструктор Камсреад. ~ Камсреад

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Remarks

Деструктор вызывает метод [**камсреад:: Close**](camthread-close.md) , который ожидает выхода из потока.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




