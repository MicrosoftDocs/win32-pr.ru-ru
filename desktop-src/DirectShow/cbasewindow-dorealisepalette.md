---
description: Метод Дореалисепалетте реализует текущую палитру окна.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Кбасевиндов. Дореалисепалетте, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656951"
---
# <a name="cbasewindowdorealisepalette-method"></a>Кбасевиндов. Дореалисепалетте, метод

`DoRealisePalette`Метод реализует текущую палитру окна.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бфорцебаккграунд* 
</dt> <dd>

Логическое значение, указывающее, должна ли палитра быть палитрой фона. Дополнительные сведения см. в разделе **селектпалетте** в пакете Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                             | Описание                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Внутренний вызов **гдифлуш** вернул ошибку.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                                            |



 

## <a name="remarks"></a>Комментарии

Метод [**кбасевиндов:: онпалеттечанже**](cbasewindow-onpalettechange.md) вызывает этот метод. Чтобы задать новую палитру, вызовите метод [**кбасевиндов:: сетпалетте**](cbasewindow-setpalette.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




