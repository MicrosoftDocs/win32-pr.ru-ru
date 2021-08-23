---
description: Метод Transform преобразует образец на месте.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Метод Ктрансинплацефилтер. Transform (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224052bc882792f57eedf9ea58842b953e5853012d3581ef14cad58467b614b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953403"
---
# <a name="ctransinplacefiltertransform-method"></a>Ктрансинплацефилтер. Transform, метод

`Transform`Метод преобразует образец на месте.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                             | Описание                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Не Доставьте этот пример.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                    |



 

## <a name="remarks"></a>Remarks

Производный класс должен реализовывать этот метод. Преобразуйте образец данных на месте. Если фильтр использует два распределителя, он копирует данные из входного примера в новый пример и передает копию в этот метод.

Если фильтр не должен доставлять этот пример (например, для поддержки контроля качества), метод должен вернуть \_ значение false.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансип. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансинплацефилтер**](ctransinplacefilter.md)
</dt> </dl>

 

 




