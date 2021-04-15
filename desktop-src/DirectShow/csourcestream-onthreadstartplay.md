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
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689014"
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

## <a name="remarks"></a>Комментарии

Этот метод не выполняет никаких действий в базовом классе. Он доступен для переопределения производного класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




