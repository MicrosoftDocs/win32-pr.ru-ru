---
description: Извлекает следующий элемент из очереди.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Ккуеуе. Жеткуеуеобжект, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679682"
---
# <a name="cqueuegetqueueobject-method"></a>Ккуеуе. Жеткуеуеобжект, метод

Извлекает следующий элемент из очереди.

## <a name="syntax"></a>Синтаксис


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект типа **T** (тип шаблона).

## <a name="remarks"></a>Комментарии

Этот метод блокируется, пока элемент не будет доступен в очереди.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккуеуе**](cqueue.md)
</dt> </dl>

 

 




