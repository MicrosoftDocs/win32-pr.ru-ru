---
description: Метод Каллворкер сигнализирует потоку запрос.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Камсреад. Каллворкер, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689202"
---
# <a name="camthreadcallworker-method"></a>Камсреад. Каллворкер, метод

`CallWorker`Метод сигнализирует потоку запрос.

## <a name="syntax"></a>Синтаксис


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двпарам* 
</dt> <dd>

Параметр запроса. Производный класс определяет значение параметра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, определяемое производным классом.

## <a name="remarks"></a>Комментарии

Методы [**камсреад:: WebRequest**](camthread-getrequest.md) и [**Камсреад:: чеккрекуест**](camthread-checkrequest.md) извлекают значение параметра *двпарам* . Метод WebRequest блокируется до `CallWorker` вызова метода.

Этот метод блокируется до тех пор, пока не будет вызван метод [**камсреад:: Reply**](camthread-reply.md) . Возвращаемое значение — это параметр, заданный для ответа.

Этот метод удерживает блокировку [**камсреад:: m \_ акцесслокк**](camthread-m-accesslock.md) для сериализации запросов. Поэтому Вызывайте этот метод из самого потока или из любой функции члена, которая выполняется в контексте потока.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




