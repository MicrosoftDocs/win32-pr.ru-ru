---
description: Метод Регистермедиатиме кэширует метки времени из текущего образца.
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Крендерерпоспасссру. Регистермедиатиме, метод (Ктлутил. h)
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
ms.openlocfilehash: ff741e58f74770c8a97c13252302d4ef86868af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665470"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Крендерерпоспасссру. Регистермедиатиме, метод (Ктлутил. h)

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



 

## <a name="remarks"></a>Комментарии

Этот метод сохраняет значения меток времени, заданные в параметрах *StartTime* и *EndTime*. Метод [**крендерерпоспасссру:: жетмедиатиме**](crendererpospassthru-getmediatime.md) получает те же значения.

Фильтр должен вызывать этот метод для каждого получаемого примера. Метод перегружен, чтобы принять либо указатель на образец, либо сами значения меток времени.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




