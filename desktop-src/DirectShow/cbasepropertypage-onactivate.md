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
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657486"
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

## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




