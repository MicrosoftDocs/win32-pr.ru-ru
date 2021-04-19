---
description: Извлекает объект КМСГ в очереди, содержащий запрос.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Кмсгсреад. Жетсреадмсг, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675659"
---
# <a name="cmsgthreadgetthreadmsg-method"></a>Кмсгсреад. Жетсреадмсг, метод

Извлекает объект [**КМСГ**](cmsg.md) в очереди, содержащий запрос.

## <a name="syntax"></a>Синтаксис


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*msg* 
</dt> <dd>

Указатель на выделенный объект [**КМСГ**](cmsg.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция-член вызывается из закрытой функции [**среадпрок**](camthread-threadproc.md) рабочего потока для получения следующей функции-члена. Параметр *MSG* должен указывать на выделенный объект [**КМСГ**](cmsg.md) , который будет заполнен параметрами для следующего запроса в очереди. Если нет запросов в очереди, эта функция-член блокируется до постановки следующего запроса в очередь (путем вызова функции-члена [**кмсгсреад::P утсреадмсг**](cmsgthread-putthreadmsg.md) ).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мсгсрд. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

 




