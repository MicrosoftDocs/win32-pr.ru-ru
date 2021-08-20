---
description: Метод Аллокформатбуффер выделяет память для блока Format.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Кмедиатипе. Аллокформатбуффер, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c53e739237f2d61a6c59c7fac96e1b97e6343fa6dd209bcf72700cefab7d599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073988"
---
# <a name="cmediatypeallocformatbuffer-method"></a>Кмедиатипе. Аллокформатбуффер, метод

`AllocFormatBuffer`Метод выделяет память для блока Format.

## <a name="syntax"></a>Синтаксис


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*length* 
</dt> <dd>

Требуемый размер блока формата в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на новый блок в случае успеха. В противном случае возвращает **значение NULL**.

## <a name="remarks"></a>Remarks

Если метод успешно выделяет новый блок формата, он освобождает существующий блок формата. Если выделение завершается неудачей, метод оставляет существующий блок формата.

Метод обновляет члены **кбформат** и **пбформат** структуры **\_ \_ типа мультимедиа AM** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




