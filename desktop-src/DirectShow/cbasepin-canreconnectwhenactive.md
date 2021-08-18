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
ms.openlocfilehash: ffe4cc09efa53ac4d3ab8089a1061d860206f9734c214d250b5c3cdc907eaf84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916924"
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

## <a name="remarks"></a>Remarks

По умолчанию перед повторным подключением к любому из его ПИН-кодов необходимо отключить фильтр. Однако если ПИН-код поддерживает динамическое повторное подключение, он может подключиться, пока фильтр активен. дополнительные сведения см. в разделе [Dynamic Graph здание](dynamic-graph-building.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




