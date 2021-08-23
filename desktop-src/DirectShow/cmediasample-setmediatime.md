---
description: 'Метод Сетмедиатиме задает время носителя для этого образца. Этот метод реализует метод Имедиасампле:: Сетмедиатиме.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Кмедиасампле. Сетмедиатиме, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3709a5f487855148b8ad4042f61b74fbe6029ef64e00b751672bf478f1da866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016372"
---
# <a name="cmediasamplesetmediatime-method"></a>Кмедиасампле. Сетмедиатиме, метод

`SetMediaTime`Метод задает время носителя для этого образца. Этот метод реализует метод [**имедиасампле:: сетмедиатиме**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстарт* 
</dt> <dd>

Указатель на время запуска носителя или **значение NULL**.

</dd> <dt>

*Ожидаем* 
</dt> <dd>

Указатель на время окончания воспроизведения или **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Время окончания работы с носителем должно быть больше времени начала носителя. Чтобы сделать носитель недействительным, используйте **значение NULL** .

Параметр *ожидания* задает абсолютное время носителя, но переменная-член [**кмедиасампле:: m \_ медиаенд**](cmediasample-m-mediaend.md) вычисляется как смещение от *пстарт*. Иными словами, **m \_ медиаенд**  =  \* *птиминд* \* *птиместарт*.  

Дополнительные сведения о времени мультимедиа см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




