---
description: Метод деструктора.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Деструктор Ксаурцестреам. ~ Ксаурцестреам (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa27d50a9c1acbc9c8a27407cb97673d60158e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657446"
---
# <a name="csourcestreamcsourcestream-destructor"></a>Деструктор Ксаурцестреам. ~ Ксаурцестреам

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
~CSourceStream();
```



## <a name="remarks"></a>Примечания

Деструктор автоматически удаляет ПИН-код из фильтра владельца, вызывая [**ксаурце:: ремовепин**](csource-removepin.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




