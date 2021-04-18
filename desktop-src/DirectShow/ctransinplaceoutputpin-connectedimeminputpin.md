---
description: 'Метод Коннектедимеминпутпин извлекает указатель на нисходящий входной ПИН-код. Этот метод возвращает переменную члена Кбасеаутпутпин:: m \_ пинпутпин.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Ктрансинплацеаутпутпин. Коннектедимеминпутпин, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657081"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>Ктрансинплацеаутпутпин. Коннектедимеминпутпин, метод

`ConnectedIMemInputPin`Метод получает указатель на нисходящий входной ПИН-код. Этот метод возвращает переменную члена [**кбасеаутпутпин:: m \_ пинпутпин**](cbaseoutputpin-m-pinputpin.md) .

## <a name="syntax"></a>Синтаксис


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) для входного контакта нисходящего входа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансинплацеаутпутпин**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




