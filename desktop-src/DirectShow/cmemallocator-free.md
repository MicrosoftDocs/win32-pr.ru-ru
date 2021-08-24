---
description: Метод Free вызывается во время операции дефиксации.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Метод Кмемаллокатор. Free (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c2ffea6fdd60e4053f6c00ee1c87ca9596560909864c861d46b5728dad13a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155996"
---
# <a name="cmemallocatorfree-method"></a>Кмемаллокатор. Free, метод

`Free`Метод вызывается во время операции дефиксации. Этот метод реализует чистый виртуальный метод [**кбасеаллокатор:: Free**](cbaseallocator-free.md) , но не выполняет никаких действий. Буферная память фактически не освобождается до тех пор, пока не будет уничтожен объект **кмемаллокатор** . Метод деструктора вызывает [**кмемаллокатор:: реаллифри**](cmemallocator-reallyfree.md) для освобождения памяти.

## <a name="syntax"></a>Синтаксис


```C++
void Free();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




