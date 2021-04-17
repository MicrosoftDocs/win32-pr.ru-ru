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
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669236"
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

## <a name="remarks"></a>Комментарии

Эта функция – член возвращает значение 1, если окно имеет \_ стиль WS Visible; в противном случае — 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




