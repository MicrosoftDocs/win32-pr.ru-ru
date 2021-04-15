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
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688866"
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

## <a name="remarks"></a>Комментарии

Этот метод является неблокирующей версией метода [**камсреад::-request**](camthread-getrequest.md) .

Если другой поток ожидает вызова Каллворкер, этот метод извлекает параметр запроса и возвращает **значение true**. В противном случае возвращается **значение false**. Если метод возвращает **значение true**, вызовите метод [**Камсреад:: Reply**](camthread-reply.md) , чтобы освободить поток запроса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




