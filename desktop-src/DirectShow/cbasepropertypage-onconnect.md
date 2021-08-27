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
ms.openlocfilehash: edc5448a20320e9bf74da7511bf6ae9fb9d95facc9b7973bbcd688127b495fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056104"
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

## <a name="remarks"></a>Remarks

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>кпроп. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




