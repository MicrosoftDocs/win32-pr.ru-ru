---
description: Метод конструктора.
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
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665230"
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

## <a name="remarks"></a>Комментарии

Класс [**Цимажеаллокатор**](cimageallocator.md) создает DIB с помощью объекта сопоставления файлов, поддерживаемого файлом подкачки операционной системы. Маркер объекта сопоставления файлов хранится в элементе **хмаппинг** структуры **\_ дибдата m** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажесампле**](cimagesample.md)
</dt> </dl>

 

 




