---
description: Метод Нотифисампле освобождает все потоки, ожидающие выборки.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Кбасеаллокатор. Нотифисампле, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669145"
---
# <a name="cbaseallocatornotifysample-method"></a>Кбасеаллокатор. Нотифисампле, метод

`NotifySample`Метод освобождает все потоки, ожидающие выборки.

## <a name="syntax"></a>Синтаксис


```C++
void NotifySample();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если имеются потоки, ожидающие выборки, значение [**кбасеаллокатор:: m \_ лваитинг**](cbaseallocator-m-lwaiting.md) больше нуля. Если значение *m \_ лваитинг* больше нуля, этот метод вызывает функцию **ReleaseSemaphore** для семафора [**кбасеаллокатор:: m \_ хсем**](cbaseallocator-m-hsem.md) , активируя все ожидающие потоки. Он также сбрасывает значение *m \_ лваитинг* до нуля.

Этот метод вызывается из метода [**кбасеаллокатор:: релеасебуффер**](cbaseallocator-releasebuffer.md) , когда образец возвращается в свободный список. и из метода [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) , когда распределитель является незафиксированным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




