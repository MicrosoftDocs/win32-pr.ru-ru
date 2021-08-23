---
description: Метод Remove удаляет объект Кдеферредкомманд из очереди.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Метод Ккмдкуеуе. Remove (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d0b0a4b416c5adb97b1a9efba1fbd5f6142b0e0fb761c6d4c0b277ac0cda7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954583"
---
# <a name="ccmdqueueremove-method"></a>Ккмдкуеуе. Remove, метод

`Remove`Метод удаляет объект [**кдеферредкомманд**](cdeferredcommand.md) из очереди.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pCmd* 
</dt> <dd>

Указатель на объект **кдеферредкомманд** , который необходимо удалить из очереди.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает VFW \_ E \_ не \_ найден, если объект не найден в очереди. В противном случае возвращается значение S \_ ОК.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




