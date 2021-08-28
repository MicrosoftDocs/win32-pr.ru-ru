---
description: Метод GetNext ожидает следующий запрос.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Метод Камсреад. WebRequest (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2527d43dfa59ab01bc57109bd2845e5da8286524612746067b1ff2f4cb2a3c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103204"
---
# <a name="camthreadgetrequest-method"></a>Камсреад. метод запроса

`GetRequest`Метод ожидает следующего запроса.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetRequest();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, определяемое производным классом.

## <a name="remarks"></a>Remarks

Этот метод блокируется до тех пор, пока другой поток не вызовет метод [**камсреад:: каллворкер**](camthread-callworker.md) . Затем возвращается параметр, который был передан в Каллворкер. Вызовите метод [**камсреад:: Reply**](camthread-reply.md) , чтобы освободить поток запроса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




