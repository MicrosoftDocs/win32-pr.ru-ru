---
description: Метод OnConnect предоставляет указатель IUnknown на объект, связанный со страницей свойств.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Метод Кбасепропертипаже. OnConnect (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657962"
---
# <a name="cbasepropertypageonconnect-method"></a>Метод Кбасепропертипаже. OnConnect

`OnConnect`Метод предоставляет указатель **IUnknown** на объект, связанный со страницей свойств.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pUnknown* 
</dt> <dd>

Указатель на интерфейс **IUnknown** объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Реализация базового класса возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Метод [**кбасепропертипаже:: сетобжектс**](cbasepropertypage-setobjects.md) вызывает `OnConnect` метод. Переопределите этот метод, чтобы сохранить указатель на объект, указанный параметром *pUnknown*. Можно либо сохранить сам указатель *pUnknown* , либо запросить этот указатель для других интерфейсов. Если вы сохраняете указатель *pUnknown* , вызывайте **AddRef** перед `OnConnect` возвратом.

В методе [**кбасепропертипаже:: OnActivate**](cbasepropertypage-onactivate.md) используйте сохраненный указатель (или указатели) для получения начальных значений для свойств диалогового окна. В методе [**кбасепропертипаже:: онаппличанжес**](cbasepropertypage-onapplychanges.md) примените любые изменения к объекту. Освободите все указатели в методе [**кбасепропертипаже:: ondisconnect**](cbasepropertypage-ondisconnect.md) .

## <a name="examples"></a>Примеры


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
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

 

 




