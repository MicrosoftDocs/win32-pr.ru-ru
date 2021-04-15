---
description: Метод "получить \_ скорость" получает приблизительную скорость потока для видео.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Метод CBaseControlVideo.get_BitRate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688769"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a>Метод Кбасеконтролвидео. Get \_ скорость

`get_BitRate`Метод извлекает приблизительную скорость потока для видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбитрате* 
</dt> <dd>

Указатель на скорость потока в битах в секунду.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если недостаточный объем памяти недоступен.

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**ибасиквидео:: Get \_ скорость**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) . Он вызывает чисто виртуальный [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




