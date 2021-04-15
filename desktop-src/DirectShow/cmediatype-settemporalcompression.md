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
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675597"
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

## <a name="remarks"></a>Комментарии

Этот метод задает элемент **бтемпоралкомпрессион** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




