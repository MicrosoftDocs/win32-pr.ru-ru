---
description: Возвращает значение TRUE, если текущий поток является владельцем указанной критической секции.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Функция Критчеккин (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f4e9ff0078f6efe8dee9b060e61858c24aea0a64e7e35b9fb867125b8612ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908084"
---
# <a name="critcheckin-function"></a>Функция Критчеккин

Возвращает **значение true** , если текущий поток является владельцем указанной критической секции.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пккрит* 
</dt> <dd>

Указатель на критический раздел [**ккритсек**](ccritsec.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В отладочных сборках возвращает **значение true** , если текущий поток является владельцем этой критической секции, или **false** в противном случае. В розничных сборках всегда возвращает **значение true**.

## <a name="remarks"></a>Remarks

Эта функция особенно полезна в макросе [**Assert**](assert.md) , чтобы проверить, владеет ли поток заданной блокировкой.

## <a name="examples"></a>Примеры

В следующем примере кода показано, как использовать эту функцию:


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции отладки критического раздела](critical-section-debugging-functions.md)
</dt> </dl>

 

 




