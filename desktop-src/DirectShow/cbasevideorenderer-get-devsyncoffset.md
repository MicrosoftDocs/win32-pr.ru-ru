---
description: Метод Get \_ девсинкоффсет извлекает стандартное отклонение времени в миллисекундах между временем выполнения каждого кадра и моментом его отрисовки для всех кадров с момента запуска потоковой передачи.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Метод CBaseVideoRenderer.get_DevSyncOffset (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657104"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a>Кбасевидеорендерер. Get \_ девсинкоффсет, метод

`get_DevSyncOffset`Метод получает стандартное отклонение времени в миллисекундах между временем выполнения каждого кадра и моментом его отрисовки для всех кадров с момента запуска потоковой передачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пидев* 
</dt> <dd>

Указатель на стандартное отклонение времени, описанное ранее.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**икуалпроп:: Get \_ девсинкоффсет**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




