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
ms.openlocfilehash: b33e3584bb0460b798101d8062c3647b983841c77653adcffd18580eade25c6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057274"
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

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**ибасиквидео:: Get \_ скорость**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) . Он вызывает чисто виртуальный [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




