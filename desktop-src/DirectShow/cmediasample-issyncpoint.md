---
description: 'Метод Иссинкпоинт определяет, является ли начало образца точкой синхронизации. Этот метод реализует метод Имедиасампле:: Иссинкпоинт.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Кмедиасампле. Иссинкпоинт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 00d238bb9289ba71237bfdf8e72acde384430f72470f16211093cb2ece8d68f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074008"
---
# <a name="cmediasampleissyncpoint-method"></a>Кмедиасампле. Иссинкпоинт, метод

`IsSyncPoint`Метод определяет, является ли начало образца точкой синхронизации. Этот метод реализует метод [**имедиасампле:: иссинкпоинт**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК, если образец является точкой синхронизации, или \_ false в противном случае.

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

 

 




