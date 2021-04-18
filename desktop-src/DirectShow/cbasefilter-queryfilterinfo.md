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
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658091"
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

## <a name="remarks"></a>Комментарии

Этот метод копирует имя фильтра из переменной члена [**кбасефилтер:: m \_ pName**](cbasefilter-m-pname.md) в элемент **АЧНАМЕ** \_ структуры сведений о фильтре. Если **m \_ pname** имеет **значение NULL**, метод устанавливает **ачнаме** в L " \\ 0".

Метод задает элемент **пграф** \_ структуры сведений о фильтре, равный переменной члена [**кбасефилтер:: m \_ пграф**](cbasefilter-m-pgraph.md) , и увеличивает счетчик ссылок. Вызывающий объект должен освободить интерфейс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




