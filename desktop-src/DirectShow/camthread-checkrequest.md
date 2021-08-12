---
description: Метод Чеккрекуест проверяет наличие запроса без блокировки.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Камсреад. Чеккрекуест, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 292f8a7fb1ed4f12ad558993d6b1932b2ddff4656bada5e0a89067bac1baa9c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662360"
---
# <a name="camthreadcheckrequest-method"></a>Камсреад. Чеккрекуест, метод

`CheckRequest`Метод проверяет наличие запроса без блокировки.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппарам* 
</dt> <dd>

Указатель на переменную, которая получает значение, переданное в последнем вызове метода [**камсреад:: каллворкер**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если имеется ожидающий запрос, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Этот метод является неблокирующей версией метода [**камсреад::-request**](camthread-getrequest.md) .

Если другой поток ожидает вызова Каллворкер, этот метод извлекает параметр запроса и возвращает **значение true**. В противном случае возвращается **значение false**. Если метод возвращает **значение true**, вызовите метод [**Камсреад:: Reply**](camthread-reply.md) , чтобы освободить поток запроса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




