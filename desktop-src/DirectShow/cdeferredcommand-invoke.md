---
description: Метод Invoke предоставляет доступ к методам и свойствам, предоставляемым объектом.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Метод Кдеферредкомманд. Invoke (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675813"
---
# <a name="cdeferredcommandinvoke-method"></a>Кдеферредкомманд. Invoke, метод

`Invoke`Метод предоставляет доступ к методам и свойствам, предоставляемым объектом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает VFW \_ E \_ уже \_ отменено, если **m \_ пкуеуе** имеет **значение NULL**. В противном случае возвращает **значение HRESULT** , полученное в результате вызова **IDispatch:: GetTypeInfo** или **IUnknown:: QueryInterface**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдеферредкомманд**](cdeferredcommand.md)
</dt> </dl>

 

 




