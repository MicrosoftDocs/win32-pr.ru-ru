---
description: Метод получения \_ колебаний получает стандартное отклонение времени в миллисекундах между кадром и следующим для всех кадров с момента запуска потоковой передачи.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Метод CBaseVideoRenderer.get_Jitter (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675209"
---
# <a name="cbasevideorendererget_jitter-method"></a>Кбасевидеорендерер. получение \_ метода противосинхронизации

`get_Jitter`Метод получает стандартное отклонение времени в миллисекундах между каждым кадром и следующим для всех кадров с момента запуска потоковой передачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пижиттер* 
</dt> <dd>

Указатель на стандартное отклонение времени между кадрами в миллисекундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**\_ колебаний икуалпроп:: Get**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




