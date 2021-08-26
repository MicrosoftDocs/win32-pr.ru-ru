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
ms.openlocfilehash: 2602d203ca5a418dcc889d26932cd28be78d984390e71cff996e6fd3938030a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057294"
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

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**ибасиквидео:: Get \_ битерроррате**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) . Он вызывает чистый виртуальный метод [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




