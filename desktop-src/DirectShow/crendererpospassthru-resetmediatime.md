---
description: Метод Ресетмедиатиме Сбрасывает кэшированные отметки времени в ноль.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Крендерерпоспасссру. Ресетмедиатиме, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657172"
---
# <a name="crendererpospassthruresetmediatime-method"></a>Крендерерпоспасссру. Ресетмедиатиме, метод

`ResetMediaTime`Метод сбрасывает кэшированные отметки времени в ноль.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Фильтр должен вызывать этот метод всякий раз, когда отметки времени, кэшированные методом [**крендерерпоспасссру:: регистермедиатиме**](crendererpospassthru-registermediatime.md) , становятся недействительными. В частности, он должен вызывать этот метод в ответ на методы [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) и [**Имедиафилтер:: останавливаться**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

После вызова этого метода метод [**крендерерпоспасссру:: жетмедиатиме**](crendererpospassthru-getmediatime.md) возвращает ноль для времени начала и окончания.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




