---
description: Метод Регистермедиатиме кэширует метки времени из текущего образца. Этот метод использует параметры *StartTime* и *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Метод Крендерерпоспасссру. Регистермедиатиме (Ктлутил. h) — параметры StartTime и EndTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187829"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>Метод Крендерерпоспасссру. Регистермедиатиме (Ктлутил. h) — параметры StartTime и EndTime

Метод [**регистермедиатиме**](crendererpospassthru-registermediatime.md) кэширует метки времени из текущего образца.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*StartTime* 
</dt> <dd>

Время начала примера в единицах измерения 100-наносекундных.

</dd> <dt>

*EndTime* 
</dt> <dd>

Время окончания примера в единицах измерения 100-наносекундных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                          | Описание         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод сохраняет значения меток времени, заданные в параметрах *StartTime* и *EndTime*. Метод [**крендерерпоспасссру:: жетмедиатиме**](crendererpospassthru-getmediatime.md) получает те же значения.

Фильтр должен вызывать этот метод для каждого получаемого примера. Метод перегружен, чтобы принять либо указатель на образец, либо сами значения меток времени.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок  | Ктлутил. h (включение Streams. h)                                                                                   |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |



 

 




