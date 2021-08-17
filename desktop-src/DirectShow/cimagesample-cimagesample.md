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
ms.openlocfilehash: 4eeb15ec42daed1fa835eff28a4953b223d9782859bfcc23b174dee8fee65019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402534"
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
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажесампле**](cimagesample.md)
</dt> </dl>

 

 




