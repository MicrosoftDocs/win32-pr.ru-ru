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
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675785"
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

## <a name="remarks"></a>Комментарии

Изначально этот класс был разработан для кэширования указателей на интерфейсы [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) и [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) подключенного ПИН-кода. `ForceRefresh`Метод освободил эти интерфейсы.

Как уже реализовано, этот класс не кэширует эти интерфейсы. Для обеспечения совместимости `ForceRefresh` метод по-прежнему включается, но возвращает \_ ОК, не делая ничего.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




