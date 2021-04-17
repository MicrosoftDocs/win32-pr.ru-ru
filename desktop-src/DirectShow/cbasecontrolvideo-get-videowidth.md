---
description: Метод Get \_ видеовидс извлекает ширину собственного видео.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: Метод CBaseControlVideo.get_VideoWidth (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658130"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a>Кбасеконтролвидео. Get \_ видеовидс, метод

`get_VideoWidth`Метод получает ширину собственного видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвидеовидс* 
</dt> <dd>

Указатель на ширину собственного видео в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если объем доступной памяти недостаточен.

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**ибасиквидео:: Get \_ видеовидс**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) . Он вызывает чисто виртуальный [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




