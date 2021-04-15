---
description: Метод Disconnect прерывает соединение с выходным закреплением.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Метод Кпуллпин. Disconnect (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669061"
---
# <a name="cpullpindisconnect-method"></a>Кпуллпин. Disconnect, метод

`Disconnect`Метод прерывает соединение с выходным закреплением.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод прерывает все соединения, сделанные в методе [**кпуллпин:: Connect**](cpullpin-connect.md) . Вызовите этот метод внутри метода [**Ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) . (Если ПИН-код является производным от [**кбасепин**](cbasepin.md), переопределите [**Кбасепин:: бреакконнект**](cbasepin-breakconnect.md) , чтобы вызвать этот метод.)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




