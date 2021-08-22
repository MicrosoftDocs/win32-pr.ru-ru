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
ms.openlocfilehash: 268316dd9b7f37894f60ed45878c7de9bbc8d379301daa7bbefedcadd0b8e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661381"
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

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**ибасиквидео:: Get \_ видеовидс**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) . Он вызывает чисто виртуальный [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




