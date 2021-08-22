---
description: Метод Онсреадстартплай вызывается в начале метода Ксаурцестреам::D Обуфферпроцессинглуп.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Метод Ксаурцестреам. Онсреадстартплай (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcd1ccf4b507570e0219854d1f5044c1d95db63d04b8f9049449beb3941e95d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073178"
---
# <a name="csourcestreamonthreadstartplay-method"></a>Ксаурцестреам. Онсреадстартплай, метод

`OnThreadStartPlay`Метод вызывается в начале метода [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод не выполняет никаких действий в базовом классе. Он доступен для переопределения производного класса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




