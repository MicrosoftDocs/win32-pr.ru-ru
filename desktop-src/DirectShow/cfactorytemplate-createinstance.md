---
description: Метод CreateInstance вызывает функцию создания объекта для класса.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Метод Кфакторитемплате. CreateInstance (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 816d690a7e57df83b3f521f4591c3334269d0fccebbaeac480e7aacb46253273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074208"
---
# <a name="cfactorytemplatecreateinstance-method"></a>Кфакторитемплате. CreateInstance, метод

`CreateInstance`Метод вызывает функцию создания объекта для класса.

## <a name="syntax"></a>Синтаксис


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pUnk* 
</dt> <dd>

Указатель на агрегированный интерфейс **IUnknown** .

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает экземпляр объекта класса.

## <a name="remarks"></a>Remarks

Метод **IClassFactory:: CreateInstance** вызывает этот метод класса. Этот метод вызывает функцию, на которую указывает переменная члена [**кфакторитемплате:: m \_ лпфннев**](cfactorytemplate-m-lpfnnew.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>комбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кфакторитемплате**](cfactorytemplate.md)
</dt> </dl>

 

 




