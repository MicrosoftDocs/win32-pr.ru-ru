---
description: Метод OnActivate вызывается при активации страницы свойств.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Метод Кбасепропертипаже. OnActivate (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f779f5bc6c33f15b5e2b1da83a72d38b91c1785564e9cace99b91469e9fdfc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052574"
---
# <a name="cbasepropertypageonactivate-method"></a>Кбасепропертипаже. OnActivate, метод

`OnActivate`Метод вызывается при активации страницы свойств.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Реализация базового класса возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Метод [**кбасепропертипаже:: Activate**](cbasepropertypage-activate.md) вызывает `OnActivate` метод. В производном классе Переопределите, `OnActivate` чтобы инициализировать диалоговое окно.

## <a name="examples"></a>Примеры

В следующем примере инициализируется элемент управления TrackBar. В этом примере предполагается, что **m \_ повнингфилтер** является указателем на пользовательский интерфейс в фильтре, связанном со страницей свойств. (Для инициализации таких указателей используйте метод [**кбасепропертипаже:: OnConnect**](cbasepropertypage-onconnect.md) .)


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
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

 

 




