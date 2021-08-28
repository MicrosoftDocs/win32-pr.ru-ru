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
ms.openlocfilehash: e8a9a70d403c4251c3250fc4d6f19c985a1546ea563a0d1bfe50ef7d7c6cfeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157491"
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

## <a name="remarks"></a>Remarks

Если фильтр имеет образец, он планирует подготовку к просмотру. В противном случае, если имеется ожидающее уведомление конца потока, фильтр отправляет событие [**\_ завершения EC**](ec-complete.md) в Диспетчер графа фильтров.

Этот метод вызывает метод [**кбасерендерер:: онстартстреаминг**](cbaserenderer-onstartstreaming.md) . Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




