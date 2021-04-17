---
description: Метод ondisconnect вызывается, когда страница свойств должна освободить связанный объект.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Метод Кбасепропертипаже. ondisconnect (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665250"
---
# <a name="cbasepropertypageondisconnect-method"></a>Кбасепропертипаже. ondisconnect, метод

`OnDisconnect`Метод вызывается, когда страница свойств должна освободить связанный объект.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Реализация базового класса возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Метод [**кбасепропертипаже:: сетобжектс**](cbasepropertypage-setobjects.md) вызывает `OnDisconnect` метод. Переопределите, `OnDisconnect` чтобы освободить все указатели, полученные в методе [**кбасепропертипаже:: OnConnect**](cbasepropertypage-onconnect.md) .

## <a name="examples"></a>Примеры


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




