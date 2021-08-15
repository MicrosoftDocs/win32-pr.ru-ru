---
description: Метод Стопстреаминг останавливает потоковую передачу, когда фильтр переходит из состояния выполнения.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Кбасерендерер. Стопстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097ad9fd1548b709f7eb74a3e468c34c3b18a73621720e249a3c626c252c898d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016802"
---
# <a name="cbaserendererstopstreaming-method"></a>Кбасерендерер. Стопстреаминг, метод

`StopStreaming`Метод останавливает потоковую передачу, когда фильтр переходит из состояния выполнения.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод вызывает метод [**кбасерендерер:: онстопстреаминг**](cbaserenderer-onstopstreaming.md) . Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




