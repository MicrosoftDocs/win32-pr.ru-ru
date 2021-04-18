---
description: Метод Стартстреаминг инициирует потоковую передачу, когда фильтр переключается в состояние выполнения.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Кбасерендерер. Стартстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669340"
---
# <a name="cbaserendererstartstreaming-method"></a>Кбасерендерер. Стартстреаминг, метод

`StartStreaming`Метод инициирует потоковую передачу, когда фильтр переключается в состояние выполнения.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Комментарии

Если фильтр имеет образец, он планирует подготовку к просмотру. В противном случае, если имеется ожидающее уведомление конца потока, фильтр отправляет событие [**\_ завершения EC**](ec-complete.md) в Диспетчер графа фильтров.

Этот метод вызывает метод [**кбасерендерер:: онстартстреаминг**](cbaserenderer-onstartstreaming.md) . Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




