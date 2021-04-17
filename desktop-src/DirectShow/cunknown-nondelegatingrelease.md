---
description: 'Уменьшает значение счетчика ссылок на объект. Этот метод реализует метод Инонделегатингункновн:: Нонделегатингрелеасе.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Кункновн. Нонделегатингрелеасе, метод (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679692"
---
# <a name="cunknownnondelegatingrelease-method"></a>Кункновн. Нонделегатингрелеасе, метод

Уменьшает значение счетчика ссылок на объект. Этот метод реализует метод **инонделегатингункновн:: нонделегатингрелеасе** .

## <a name="syntax"></a>Синтаксис


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает счетчик ссылок.

## <a name="remarks"></a>Комментарии

Когда счетчик ссылок достигает нуля, объект удаляет себя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




