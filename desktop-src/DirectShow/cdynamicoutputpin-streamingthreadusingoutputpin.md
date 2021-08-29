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
ms.openlocfilehash: 4687db225a616adef6d1c756ae9295e2c273c0315f37d119c7bacd0c226233e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539724"
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

## <a name="remarks"></a>Remarks

Если какие-либо потоки успешно возвращали метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) и не выполнили соответствующий вызов метода [**Кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) , этот метод возвращает **значение true**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




