---
description: Метод Сетсинксаурце задает часы, используемые для времени.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Ккмдкуеуе. Сетсинксаурце, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3877fb52a1e2268d24974ee3575c712d27a107f4429398ada9de1ebf5e728675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757154"
---
# <a name="ccmdqueuesetsyncsource-method"></a>Ккмдкуеуе. Сетсинксаурце, метод

`SetSyncSource`Метод задает часы, используемые для времени.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пирк* 
</dt> <dd>

Указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




