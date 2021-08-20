---
description: Метод Сетсамплесизе задает фиксированный размер выборки или указывает, что выборки имеют переменный размер.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Кмедиатипе. Сетсамплесизе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a29393ed4c9251d1e12895ad57a61f96bdc80bb05757ce72fc9485bb42a1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954413"
---
# <a name="cmediatypesetsamplesize-method"></a>Кмедиатипе. Сетсамплесизе, метод

`SetSampleSize`Метод задает фиксированный размер выборки или указывает, что выборки имеют переменный размер.

## <a name="syntax"></a>Синтаксис


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SZ* 
</dt> <dd>

Размер выборки, в байтах или нуль.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Если значение *SZ* равно нулю, то тип носителя использует переменные выбор размера. В противном случае размер выборки зафиксирован на *SZ* байт.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




