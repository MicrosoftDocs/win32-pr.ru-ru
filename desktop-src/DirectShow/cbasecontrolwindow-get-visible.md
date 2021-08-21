---
description: Метод Get \_ Visible извлекает текущую видимость окна.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Метод CBaseControlWindow.get_Visible (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef75aaf396e8677e9c470239d5dfca747729b534b67f8fef53a065280175f017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017382"
---
# <a name="cbasecontrolwindowget_visible-method"></a>Кбасеконтролвиндов. получить \_ видимый метод

`get_Visible`Метод получает текущую видимость окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвисибле* 
</dt> <dd>

Указатель на логический флаг автоматизации (0 — Off, 1 — включено).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция – член возвращает значение 1, если окно имеет \_ стиль WS Visible; в противном случае — 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




