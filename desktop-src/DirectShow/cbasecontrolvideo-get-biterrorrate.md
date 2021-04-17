---
description: Метод Get \_ битерроррате извлекает приблизительную частоту ошибок в битах для видео.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Метод CBaseControlVideo.get_BitErrorRate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657249"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>Кбасеконтролвидео. Get \_ битерроррате, метод

`get_BitErrorRate`Метод извлекает приблизительную частоту ошибок в битах для видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбитерроррате* 
</dt> <dd>

Указатель на частоту битовых ошибок (одна ошибка для приблизительного числа битов).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если объем доступной памяти недостаточен.

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**ибасиквидео:: Get \_ битерроррате**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) . Он вызывает чистый виртуальный метод [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




