---
description: 'Метод Жоинфилтерграф уведомляет фильтр о соединении или на графе фильтра. Этот метод реализует метод Ибасефилтер:: Жоинфилтерграф.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Кбасефилтер. Жоинфилтерграф, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657798"
---
# <a name="cbasefilterjoinfiltergraph-method"></a>Кбасефилтер. Жоинфилтерграф, метод

`JoinFilterGraph`Метод уведомляет фильтр о соединении или влево граф фильтра. Этот метод реализует метод [**ибасефилтер:: жоинфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пграф* 
</dt> <dd>

Указатель на интерфейс [**ифилтерграф**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) диспетчера графа фильтров или **значение NULL** , если фильтр выходит из графа.

</dd> <dt>

*pName* \[ окне\]
</dt> <dd>

Указатель на строку в Юникоде, содержащую имя фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод задает переменную члена [**кбасефилтер:: m \_ пграф**](cbasefilter-m-pgraph.md) , равную параметру *пграф* . Он также запрашивает указатель интерфейса [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) и сохраняет его в переменной члена [**кбасефилтер:: m \_ псинк**](cbasefilter-m-psink.md) . Однако фильтр не сохраняет счетчик ссылок ни для одного из этих интерфейсов. Это приведет к созданию циклического счетчика ссылок, так как диспетчер графа фильтров сохранит счетчик ссылок на фильтре.

Метод копирует строку, указанную параметром *pName* , в переменную члена [**кбасефилтер:: m \_ pName**](cbasefilter-m-pname.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




