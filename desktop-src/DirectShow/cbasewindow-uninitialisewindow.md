---
description: Метод Унинитиалисевиндов освобождает ресурсы окна.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Кбасевиндов. Унинитиалисевиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c275e4d683bcc698c8f04c5a85017b081b6aad17f93c91d66e0a75f2da88692e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657496"
---
# <a name="cbasewindowuninitialisewindow-method"></a>Кбасевиндов. Унинитиалисевиндов, метод

`UninitialiseWindow`Метод освобождает ресурсы окна.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод освобождает ресурсы, которые были получены методом [**кбасевиндов:: инитиалисевиндов**](cbasewindow-initialisewindow.md) . Метод [**кбасевиндов::D оневисвиндов**](cbasewindow-donewithwindow.md) вызывает этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




