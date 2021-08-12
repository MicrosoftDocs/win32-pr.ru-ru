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
ms.openlocfilehash: ff1cd8b966456df631a573ab2e8691b3be5d8bda47b21b042986204144e639b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659807"
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

## <a name="remarks"></a>Remarks

Чтобы предоставить сведения о поставщике для фильтра, Переопределите этот метод. При реализации этого метода используйте функцию **CoTaskMemAlloc** , чтобы выделить память для строки. Вызывающий объект отвечает за вызов функции **CoTaskMemFree** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




