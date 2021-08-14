---
description: Функция Исекуалобжект проверяет, находятся ли два интерфейса в одном объекте.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Функция Исекуалобжект (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e385cf887dceddcdc470b908d46f59405f573ab47837b26f8453ce6154eb0d72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817457"
---
# <a name="isequalobject-function"></a>Функция Исекуалобжект

`IsEqualObject`Функция проверяет, находятся ли два интерфейса на одном объекте.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфирст* 
</dt> <dd>

Указатель на один интерфейс.

</dd> <dt>

*псеконд* 
</dt> <dd>

Указатель на другой интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если интерфейсы находятся в одном объекте, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Различные вспомогательные функции](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




