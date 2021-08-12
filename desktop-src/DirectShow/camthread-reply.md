---
description: Метод Reply отвечает на запрос.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Метод Камсреад. Reply (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9783703d711800b8002aa0372292349d83620eafb097be2256ffde6ab2c91c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662370"
---
# <a name="camthreadreply-method"></a>Камсреад. Reply, метод

`Reply`Метод отвечает на запрос.

## <a name="syntax"></a>Синтаксис


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*dw* 
</dt> <dd>

Значение, возвращаемое методом [**камсреад:: каллворкер**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод Каллворкер блокируется до вызова этого метода. Параметр *DW* предоставляет возвращаемое значение для каллворкер. Вызовите этот метод в процедуре потока после получения запроса, чтобы освободить поток запроса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




