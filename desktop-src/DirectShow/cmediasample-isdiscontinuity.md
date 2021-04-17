---
description: 'Метод Исдисконтинуити определяет, представляет ли этот образец разрыв в потоке данных. Этот метод реализует метод Имедиасампле:: Исдисконтинуити.'
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Кмедиасампле. Исдисконтинуити, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665214"
---
# <a name="cmediasampleisdiscontinuity-method"></a>Кмедиасампле. Исдисконтинуити, метод

`IsDiscontinuity`Метод определяет, представляет ли этот образец разрыв в потоке данных. Этот метод реализует метод [**имедиасампле:: исдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК, если образец является перерывом в потоке данных, и \_ false в противном случае.

## <a name="remarks"></a>Комментарии

Значение этого свойства указывается в переменной члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




