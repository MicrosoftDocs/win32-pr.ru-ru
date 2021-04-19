---
description: Является устаревшей. Вместо этого используйте AMovieSetupRegisterFilter2.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Функция Амовиесетупрегистерфилтер (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688940"
---
# <a name="amoviesetupregisterfilter-function"></a>Функция Амовиесетупрегистерфилтер

Является устаревшей. Вместо этого используйте [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псетупдата* 
</dt> <dd>

Зарезервировано.

</dd> <dt>

*пифм* 
</dt> <dd>

Зарезервировано.

</dd> <dt>

*брегистер* 
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дллсетуп. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции установки DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




