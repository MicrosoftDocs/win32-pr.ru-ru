---
description: Метод Онаппличанжес вызывается, когда пользователь применяет изменения к странице свойств.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Кбасепропертипаже. Онаппличанжес, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f822bed433af6e3fab0250e06a04911ee10187039036211974b046b32df6b7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823110"
---
# <a name="cbasepropertypageonapplychanges-method"></a>Кбасепропертипаже. Онаппличанжес, метод

`OnApplyChanges`Метод вызывается, когда пользователь применяет изменения к странице свойств.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Реализация базового класса возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Метод [**кбасепропертипаже:: Apply**](cbasepropertypage-apply.md) вызывает, `OnApplyChanges` Если флаг [**кбасепропертипаже:: m \_ бдирти**](cbasepropertypage-m-bdirty.md) имеет **значение true**. Переопределите `OnApplyChanges` для обработки изменений и сбросьте **m \_ Бдирти** в **значение false**.

## <a name="examples"></a>Примеры


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>кпроп. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




