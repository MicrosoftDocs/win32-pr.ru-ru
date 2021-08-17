---
description: 'Метод Куерифилтеринфо извлекает сведения о фильтре. Этот метод реализует метод Ибасефилтер:: Куерифилтеринфо.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Кбасефилтер. Куерифилтеринфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31eb135a29a6e8e1c4f27c28d24b5cbf50eba3bb87b99ba9a1d3a5868c2fbc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341744"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>Кбасефилтер. Куерифилтеринфо, метод

`QueryFilterInfo`Метод получает сведения о фильтре. Этот метод реализует метод [**ибасефилтер:: куерифилтеринфо**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* 
</dt> <dd>

Указатель на структуру [**\_ сведений о фильтре**](/windows/win32/api/strmif/ns-strmif-filter_info) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="remarks"></a>Remarks

Этот метод копирует имя фильтра из переменной члена [**кбасефилтер:: m \_ pName**](cbasefilter-m-pname.md) в элемент **АЧНАМЕ** \_ структуры сведений о фильтре. Если **m \_ pname** имеет **значение NULL**, метод устанавливает **ачнаме** в L " \\ 0".

Метод задает элемент **пграф** \_ структуры сведений о фильтре, равный переменной члена [**кбасефилтер:: m \_ пграф**](cbasefilter-m-pgraph.md) , и увеличивает счетчик ссылок. Вызывающий объект должен освободить интерфейс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




