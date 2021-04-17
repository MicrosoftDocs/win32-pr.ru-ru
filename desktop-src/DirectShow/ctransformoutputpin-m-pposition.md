---
description: Вспомогательный объект для передачи команд поиска в восходящий поток.
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
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657726"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Элемент Ктрансформаутпутпин:: m \_ ппоситион

Вспомогательный объект для передачи команд поиска в восходящий поток.

## <a name="syntax"></a>Синтаксис


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Примечания

Когда ПИН-код сначала запрашивает интерфейс [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) или [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , он создает и выполняет статистическую обработку объекта вспомогательного приложения [**кпоспасссру**](cpospassthru.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




