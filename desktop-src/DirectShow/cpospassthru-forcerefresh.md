---
description: Метод Форцерефреш устарел.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Кпоспасссру. Форцерефреш, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 738a528562afd04e27105691b001958f130e353ec52aa60da86bec47c81b5ba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915524"
---
# <a name="cpospassthruforcerefresh-method"></a>Кпоспасссру. Форцерефреш, метод

`ForceRefresh`Метод устарел.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Изначально этот класс был разработан для кэширования указателей на интерфейсы [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) и [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) подключенного ПИН-кода. `ForceRefresh`Метод освободил эти интерфейсы.

Как уже реализовано, этот класс не кэширует эти интерфейсы. Для обеспечения совместимости `ForceRefresh` метод по-прежнему включается, но возвращает \_ ОК, не делая ничего.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




