---
description: Метод Онпалеттечанже обрабатывает сообщения изменения палитры.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Кбасевиндов. Онпалеттечанже, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c881c519706ca0288847a7dc603cf513a99cdd76e4c83f0e53bec16df840e509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657957"
---
# <a name="cbasewindowonpalettechange-method"></a>Кбасевиндов. Онпалеттечанже, метод

`OnPaletteChange`Метод обрабатывает сообщения изменения палитры.

## <a name="syntax"></a>Синтаксис


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Дескриптор для окна.

</dd> <dt>

*Message* 
</dt> <dd>

Идентификатор сообщения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0, если сообщение было обработано, или значение 1, если сообщение не было обработано.

## <a name="remarks"></a>Remarks

Этот метод обрабатывает \_ сообщения WM палеттечанжед и WM \_ куериневпалетте. Он вызывает метод [**кбасевиндов::D ореалисепалетте**](cbasewindow-dorealisepalette.md) для реализации новой палитры.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




