---
description: 'Метод Stop останавливает фильтр. Этот метод реализует метод Имедиафилтер:: останавливаться.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Метод Кбасефилтер. останавливаться (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657331"
---
# <a name="cbasefilterstop-method"></a>Кбасефилтер. останавливаться, метод

`Stop`Метод останавливает фильтр. Этот метод реализует метод [**имедиафилтер:: останавливаться**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.

## <a name="remarks"></a>Комментарии

Этот метод вызывает метод [**кбасепин:: Inactive**](cbasepin-inactive.md) для каждого подключенного контакта фильтра. Он также устанавливает состояние фильтра в состояние \_ остановлено.

Когда фильтр останавливается, он должен отклонять выборки из вышестоящего, прекращать доставку образцов, завершать рабочие потоки и освобождать все ресурсы, используемые для потоковой передачи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




