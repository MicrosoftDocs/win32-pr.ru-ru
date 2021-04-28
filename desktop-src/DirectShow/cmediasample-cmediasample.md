---
description: Метод конструктора Кмедиасампле. Кмедиасампле.
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
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095442"
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

## <a name="remarks"></a>Remarks

Базовый класс не изменяет значение **HRESULT** , передаваемое в параметре *фр* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




