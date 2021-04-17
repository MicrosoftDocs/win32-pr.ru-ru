---
description: 'Метод Ендфлуш завершает операцию очистки. Этот метод реализует метод Ипин:: Ендфлуш.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Ктрансформинпутпин. Ендфлуш, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0fe6afeaa0ca3d47b278987af494221e8f50340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657405"
---
# <a name="ctransforminputpinendflush-method"></a>Ктрансформинпутпин. Ендфлуш, метод

`EndFlush`Метод завершает операцию очистки. Этот метод реализует метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                                           | Описание                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                  | Успешно.<br/>                     |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | Выходной ПИН-код не подключен.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод вызывает метод [**ктрансформфилтер:: ендфлуш**](ctransformfilter-endflush.md) фильтра для доставки вызова в нисходящем направлении. Затем вызывается метод [**кбасеинпутпин:: ендфлуш**](cbaseinputpin-endflush.md) ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




