---
description: Метод Пстателокк извлекает указатель на объект критической секции фильтра.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Метод Ксаурце. Пстателокк (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b74027e2ee2339e647938592e05162ce85108eb6985061b30a825394c2f2e7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953793"
---
# <a name="csourcepstatelock-method"></a>Ксаурце. Пстателокк, метод

Метод **пстателокк** извлекает указатель на объект критической секции фильтра.

> [!Note]  
> Несмотря на то, что именование аналогично переменной-члену, **пстателокк** является методом.

 

## <a name="syntax"></a>Синтаксис


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на переменную-член [**ксаурце:: m \_ кстателокк**](csource-m-cstatelock.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурце**](csource.md)
</dt> </dl>

 

 




