---
description: Метод конструктора.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Конструктор Кмедиасампле. Кмедиасампле (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675203"
---
# <a name="cmediasamplecmediasample-constructor"></a>Кмедиасампле. Кмедиасампле, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*паллокатор* 
</dt> <dd>

Указатель на объект [**кбасеаллокатор**](cbaseallocator.md) , который создал этот образец.

</dd> <dt>

*фр* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Указатель на буфер памяти, выделенный вызывающим объектом, *длиной* размера.

</dd> <dt>

*length* 
</dt> <dd>

Длина буфера памяти.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Базовый класс не изменяет значение **HRESULT** , передаваемое в параметре *фр* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




