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
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675088"
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

Обработчик для окна.

</dd> <dt>

*Message* 
</dt> <dd>

Идентификатор сообщения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0, если сообщение было обработано, или значение 1, если сообщение не было обработано.

## <a name="remarks"></a>Комментарии

Этот метод обрабатывает \_ сообщения WM палеттечанжед и WM \_ куериневпалетте. Он вызывает метод [**кбасевиндов::D ореалисепалетте**](cbasewindow-dorealisepalette.md) для реализации новой палитры.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




