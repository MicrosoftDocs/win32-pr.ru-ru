---
description: Метод конструктора Цимажесампле. Цимажесампле.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Конструктор Цимажесампле. Цимажесампле (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecab52e347e03b698adccb79b77da879d26612b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095612"
---
# <a name="cimagesamplecimagesample-constructor"></a>Цимажесампле. Цимажесампле, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паллокатор* 
</dt> <dd>

Указатель на распределитель, создавший этот образец.

</dd> <dt>

*pName* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*фр* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Указатель на буфер памяти, выделенный вызывающим объектом, *длиной* размера. Буфер должен содержать аппаратно-независимый точечный рисунок GDI (DIB).

</dd> <dt>

*length* 
</dt> <dd>

Длина буфера.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс [**Цимажеаллокатор**](cimageallocator.md) создает DIB с помощью объекта сопоставления файлов, поддерживаемого файлом подкачки операционной системы. Маркер объекта сопоставления файлов хранится в элементе **хмаппинг** структуры **\_ дибдата m** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажесампле**](cimagesample.md)
</dt> </dl>

 

 




