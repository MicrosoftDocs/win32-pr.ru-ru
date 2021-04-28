---
description: 'Ктрансформаутпутпин:: m_pPosition элемент вспомогательного объекта для передачи команд поиска в восходящий поток.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Элемент Ктрансформаутпутпин:: m_pPosition (Трансфрм. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084862"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Элемент Ктрансформаутпутпин:: m \_ ппоситион

Вспомогательный объект для передачи команд поиска в восходящий поток.

## <a name="syntax"></a>Синтаксис


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Remarks

Когда ПИН-код сначала запрашивает интерфейс [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) или [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , он создает и выполняет статистическую обработку объекта вспомогательного приложения [**кпоспасссру**](cpospassthru.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




