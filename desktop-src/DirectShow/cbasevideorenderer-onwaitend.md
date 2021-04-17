---
description: Метод Онваитенд вызывается, когда заканчивается время ожидания.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Кбасевидеорендерер. Онваитенд, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656968"
---
# <a name="cbasevideorendereronwaitend-method"></a>Кбасевидеорендерер. Онваитенд, метод

Метод Онваитенд вызывается, когда заканчивается время ожидания.

## <a name="syntax"></a>Синтаксис


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция члена выполняет только ведение журнала производительности. Он вызывается, когда поток пробудится из ожидания в окне, или когда происходит визуализация следующего образца. В конечном итоге он может использоваться для сбора информации, управляющей синхронизацией.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




