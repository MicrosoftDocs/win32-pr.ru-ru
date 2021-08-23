---
description: 'Неактивный метод уведомляет ПИН-код о том, что фильтр больше не активен. Этот метод переопределяет метод Кбасепин:: Inactive. Если поток потоковой передачи активен, этот метод останавливает его и ждет выхода из потока.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Ксаурцестреам. Inactive-метод (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9d9424f4299d7a07ad98010846fa917307bd38eead028b4b8c38c40e2284c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687374"
---
# <a name="csourcestreaminactive-method"></a>Ксаурцестреам. Inactive, метод

`Inactive`Метод уведомляет ПИН-код о том, что фильтр больше не активен. Этот метод переопределяет метод [**кбасепин:: Inactive**](cbasepin-inactive.md) . Если поток потоковой передачи активен, этот метод останавливает его и ждет выхода из потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




