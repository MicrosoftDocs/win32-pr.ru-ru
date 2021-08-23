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
ms.openlocfilehash: 72e5823b7acadd3c1c0f3752606825d1b2981aac4a64903c5944e3df82252aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017602"
---
# <a name="camthreadm_accesslock-member"></a>Элемент Камсреад:: m \_ акцесслокк

Критическая секция, которая блокирует доступ к потоку из других потоков.

## <a name="syntax"></a>Синтаксис


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Remarks

Методы [**камсреад:: Create**](camthread-create.md) и [**Камсреад:: каллворкер**](camthread-callworker.md) содержат эту блокировку для сериализации операций в потоке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




