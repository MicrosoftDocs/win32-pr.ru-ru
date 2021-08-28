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
ms.openlocfilehash: 1df087e71ba03ef67ea250235a4ef8a9ef5e6623efe67594381111de6088cf7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074378"
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
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдеферредкомманд**](cdeferredcommand.md)
</dt> </dl>

 

 




