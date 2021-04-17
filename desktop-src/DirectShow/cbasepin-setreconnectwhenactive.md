---
description: Метод Сетреконнектвхенактиве указывает, поддерживает ли ПИН-код динамическое повторное подключение.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Кбасепин. Сетреконнектвхенактиве, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665085"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>Кбасепин. Сетреконнектвхенактиве, метод

`SetReconnectWhenActive`Метод указывает, поддерживает ли ПИН-код динамическое повторное подключение.

## <a name="syntax"></a>Синтаксис


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бканреконнект* 
</dt> <dd>

Логическое значение, указывающее, может ли ПИН-код динамически переподключаться. Если **значение — true**, ПИН-код может динамически переподключаться.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

По умолчанию перед повторным подключением к любому из его ПИН-кодов необходимо отключить фильтр. Если ПИН-код может повторно подключиться, пока фильтр активен, вызовите этот метод со значением **true**. Дополнительные сведения см. в разделе [динамическое построение графа](dynamic-graph-building.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




