---
description: 'Метод Испреролл определяет, является ли этот пример примером предобразца. Образец не должен отображаться. Этот метод реализует метод Имедиасампле:: Испреролл.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Кмедиасампле. Испреролл, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f4c4b192d72c5edcfdb9c318f7420ca6ae5797446ec4f99cb6871aad2abd241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634644"
---
# <a name="cmediasampleispreroll-method"></a>Кмедиасампле. Испреролл, метод

`IsPreroll`Метод определяет, является ли этот пример примером предобразца. Образец не должен отображаться. Этот метод реализует метод [**имедиасампле:: испреролл**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение \_ ОК, если образец является примером, и \_ false в противном случае.

## <a name="remarks"></a>Remarks

Значение этого свойства указывается в переменной члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




