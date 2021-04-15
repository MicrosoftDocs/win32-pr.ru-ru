---
description: Критическая секция, которая блокирует доступ к потоку из других потоков.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Элемент Камсреад:: m_AccessLock (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689104"
---
# <a name="camthreadm_accesslock-member"></a>Элемент Камсреад:: m \_ акцесслокк

Критическая секция, которая блокирует доступ к потоку из других потоков.

## <a name="syntax"></a>Синтаксис


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Примечания

Методы [**камсреад:: Create**](camthread-create.md) и [**Камсреад:: каллворкер**](camthread-callworker.md) содержат эту блокировку для сериализации операций в потоке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




