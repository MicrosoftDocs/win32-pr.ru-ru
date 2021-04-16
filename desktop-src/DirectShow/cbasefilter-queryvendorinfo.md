---
description: 'Метод Куеривендоринфо извлекает строку, содержащую сведения о поставщике. Этот метод реализует метод Ибасефилтер:: Куеривендоринфо.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Кбасефилтер. Куеривендоринфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658090"
---
# <a name="cbasefilterqueryvendorinfo-method"></a>Кбасефилтер. Куеривендоринфо, метод

`QueryVendorInfo`Метод извлекает строку, содержащую сведения о поставщике. Этот метод реализует метод [**ибасефилтер:: куеривендоринфо**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвендоринфо* 
</dt> <dd>

Адрес переменной, которая получает указатель на строку расширенных символов, содержащую сведения о поставщике.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает E \_ нотимпл.

## <a name="remarks"></a>Комментарии

Чтобы предоставить сведения о поставщике для фильтра, Переопределите этот метод. При реализации этого метода используйте функцию **CoTaskMemAlloc** , чтобы выделить память для строки. Вызывающий объект отвечает за вызов функции **CoTaskMemFree** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




