---
description: Метод Get \_ WindowStyle извлекает стандартные стили окна.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: Метод CBaseControlWindow.get_WindowStyle (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9356b449adbb4ee760ec70990c4db0b6703c16e9d0970f2756bac23907b1bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660263"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a>Кбасеконтролвиндов. Get \_ WindowStyle, метод

`get_WindowStyle`Метод получает стандартные стили окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвиндовстиле* 
</dt> <dd>

Указатель на стили окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция – член возвращает стандартные стили окон, такие как WS \_ Child и WS \_ Visible. Он вызывает функцию члена [**кбасеконтролвиндов::D ожетвиндовстиле**](cbasecontrolwindow-dogetwindowstyle.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




