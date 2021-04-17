---
description: Метод Чанжестоп вызывается при изменении позиции окончания.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Ксаурцесикинг. Чанжестоп, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688762"
---
# <a name="csourceseekingchangestop-method"></a>Ксаурцесикинг. Чанжестоп, метод

`ChangeStop`Метод вызывается при изменении позиции окончания.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Метод [**ксаурцесикинг:: сетпоситионс**](csourceseeking-setpositions.md) вызывает этот метод, если позиция окончания изменяется. Этот метод является чисто виртуальным; производный класс должен реализовать его. В следующем примере показана возможная реализация:


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




