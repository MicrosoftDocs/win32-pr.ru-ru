---
description: Метод Канреконнектвхенактиве запрашивает, поддерживает ли ПИН-код динамическое повторное подключение.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Кбасепин. Канреконнектвхенактиве, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669014"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>Кбасепин. Канреконнектвхенактиве, метод

`CanReconnectWhenActive`Метод запрашивает, поддерживает ли ПИН-код динамическое повторное подключение.

## <a name="syntax"></a>Синтаксис


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает логическое значение, указывающее, может ли ПИН-код динамически переподключаться. Если **значение — true**, ПИН-код может динамически переподключаться.

## <a name="remarks"></a>Комментарии

По умолчанию перед повторным подключением к любому из его ПИН-кодов необходимо отключить фильтр. Однако если ПИН-код поддерживает динамическое повторное подключение, он может подключиться, пока фильтр активен. Дополнительные сведения см. в разделе [динамическое построение графа](dynamic-graph-building.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




