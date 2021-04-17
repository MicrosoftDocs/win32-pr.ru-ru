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
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679968"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




