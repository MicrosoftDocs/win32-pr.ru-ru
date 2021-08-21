---
description: Метод Сеттемпоралкомпрессион указывает, сжимаются ли образцы с использованием временного (упакованного) сжатия.
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Кмедиатипе. Сеттемпоралкомпрессион, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29efb0ec16f99c7354621bc49bd36c4e367375d5eb68a2d94a69c27bfdce2f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954403"
---
# <a name="cmediatypesettemporalcompression-method"></a>Кмедиатипе. Сеттемпоралкомпрессион, метод

`SetTemporalCompression`Метод указывает, сжимаются ли образцы с использованием временного (упакованного) сжатия.

## <a name="syntax"></a>Синтаксис


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бкомпрессед* 
</dt> <dd>

Логическое значение, указывающее, использует ли поток временное сжатие. Если поток использует временное сжатие, установите значение **true**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод задает элемент **бтемпоралкомпрессион** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




