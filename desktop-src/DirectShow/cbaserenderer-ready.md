---
description: Метод Ready сигнализирует о завершении перехода состояния.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Метод Кбасерендерер. ready (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a1870af825f2a33236d0fd86d0f730e0013df59297fec5cdaa2baf46a2b773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757524"
---
# <a name="cbaserendererready-method"></a>Кбасерендерер. ready, метод

`Ready`Метод сигнализирует о завершении перехода состояния.

## <a name="syntax"></a>Синтаксис


```C++
void Ready();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод приводит к тому, что метод [**кбасерендерер::**](cbaserenderer-getstate.md) noreturn возвращает значение S \_ OK, что означает, что фильтр завершил переход в текущее состояние. Фильтр вызывает этот метод при каждом завершении смены состояния.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> <dt>

[**Кбасерендерер:: Чеккреади**](cbaserenderer-checkready.md)
</dt> <dt>

[**Кбасерендерер:: NotReady**](cbaserenderer-notready.md)
</dt> </dl>

 

 




