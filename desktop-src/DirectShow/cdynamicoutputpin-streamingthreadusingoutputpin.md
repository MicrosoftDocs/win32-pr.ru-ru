---
description: Метод Стреамингсреадусингаутпутпин определяет, выполняет ли поток потоковую операцию с закреплением.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Кдинамикаутпутпин. Стреамингсреадусингаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669130"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>Кдинамикаутпутпин. Стреамингсреадусингаутпутпин, метод

Метод Стреамингсреадусингаутпутпин определяет, выполняет ли поток потоковую операцию с закреплением.

## <a name="syntax"></a>Синтаксис


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если поток выполняет потоковую операцию над закреплением. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Комментарии

Если какие-либо потоки успешно возвращали метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) и не выполнили соответствующий вызов метода [**Кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) , этот метод возвращает **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




