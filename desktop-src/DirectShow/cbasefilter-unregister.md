---
description: Метод Unregister удаляет фильтр из реестра.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Метод Кбасефилтер. Unregister (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c57d08c77c9c420cdc45b158a19fa610231f53f6b409d8b650953de0de8381a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317904"
---
# <a name="cbasefilterunregister-method"></a>Кбасефилтер. Unregister, метод

`Unregister`Метод удаляет фильтр из реестра.

> [!Note]  
> Этот метод устарел. Регистрация новых фильтров должна быть отменена с помощью функции [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) . дополнительные сведения см. [в статье регистрация DirectShow фильтров](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




