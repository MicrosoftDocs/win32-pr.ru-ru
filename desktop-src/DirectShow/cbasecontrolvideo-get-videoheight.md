---
description: Метод Get \_ видеохеигхт извлекает высоту собственного видео.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: Метод CBaseControlVideo.get_VideoHeight (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a7ca4b87a9196a8b59ec00cdc0e458855fa1db4e1e8f7b5bfd233924475519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057084"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>Кбасеконтролвидео. Get \_ видеохеигхт, метод

`get_VideoHeight`Метод получает высоту собственного видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвидеохеигхт* 
</dt> <dd>

Указатель на высоту собственного видео в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если объем доступной памяти недостаточен.

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**ибасиквидео:: Get \_ видеохеигхт**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) . Он вызывает чисто виртуальный [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




