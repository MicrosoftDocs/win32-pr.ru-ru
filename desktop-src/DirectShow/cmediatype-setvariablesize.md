---
description: Метод Сетвариаблесизе указывает, что выборки не имеют фиксированного размера.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Кмедиатипе. Сетвариаблесизе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 118167d0068c058c925e5b63e2e951ff860917c40a5c3533daf9f02e6927649a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073968"
---
# <a name="cmediatypesetvariablesize-method"></a>Кмедиатипе. Сетвариаблесизе, метод

`SetVariableSize`Метод указывает, что выборки не имеют фиксированного размера.

## <a name="syntax"></a>Синтаксис


```C++
void SetVariableSize();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод задает для элемента **Бфикседсизесамплес** **значение false**. Последующие вызовы метода [**кмедиатипе:: жетсамплесизе**](cmediatype-getsamplesize.md) возвращают ноль.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




