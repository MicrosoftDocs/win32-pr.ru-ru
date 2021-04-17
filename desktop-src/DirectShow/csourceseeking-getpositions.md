---
description: 'Метод Disposition извлекает текущую и заданную позиции. Этот метод реализует метод Имедиасикинг:: Disposition.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Метод Ксаурцесикинг. Disposition (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657502"
---
# <a name="csourceseekinggetpositions-method"></a>Метод Ксаурцесикинг. Disposition

`GetPositions`Метод извлекает текущую и заданную позиции. Этот метод реализует метод [**имедиасикинг:: Disposition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкуррент* 
</dt> <dd>

Указатель на переменную, которая получает начальную точку.

</dd> <dt>

*пстоп* 
</dt> <dd>

Указатель на переменную, которая получает точку окончания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Для параметра *пкуррент* этот метод возвращает значение переменной члена [**ксаурцесикинг:: m \_ ртстарт**](csourceseeking-m-rtstart.md) , которая представляет последнее время поиска, а не текущее положение потоковой передачи. Однако когда приложение вызывает **имедиасикинг:: Disposition** через диспетчер графа фильтров, значения обычно берутся из фильтра модуля подготовки отчетов, а не из фильтра источника.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




