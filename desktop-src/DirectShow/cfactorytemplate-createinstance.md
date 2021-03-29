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
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657577"
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

## <a name="remarks"></a>Комментарии

Метод **IClassFactory:: CreateInstance** вызывает этот метод класса. Этот метод вызывает функцию, на которую указывает переменная члена [**кфакторитемплате:: m \_ лпфннев**](cfactorytemplate-m-lpfnnew.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кфакторитемплате**](cfactorytemplate.md)
</dt> </dl>

 

 




