---
description: Метод Онрецеивемессаже вызывается, когда диалоговое окно получает сообщение.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Кбасепропертипаже. Онрецеивемессаже, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833f0f7ab9192d88440afff75a36fee744ac2fe053c6fe99d1940686c452799a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158136"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>Кбасепропертипаже. Онрецеивемессаже, метод

`OnReceiveMessage`Метод вызывается, когда диалоговое окно получает сообщение.

## <a name="syntax"></a>Синтаксис


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Дескриптор для окна.

</dd> <dt>

*Uiacp* 
</dt> <dd>

Message.

</dd> <dt>

*wParam* 
</dt> <dd>

Первый параметр сообщения.

</dd> <dt>

*lParam* 
</dt> <dd>

Второй параметр сообщения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает логическое значение. Процедура диалогового окна возвращает это значение. Дополнительные сведения см. в документации по пакету Platform SDK.

## <a name="remarks"></a>Remarks

Реализация базового класса вызывает **дефвиндовпрок**. Переопределите этот метод, чтобы он обрабатывал сообщения, связанные с элементами управления диалогового окна. Если переопределяющий метод не обрабатывает конкретное сообщение, он должен вызвать метод базового класса.

Если пользователь изменяет свойства через диалоговые элементы управления, установите для флага [**кбасепропертипаже:: m \_ Бдирти**](cbasepropertypage-m-bdirty.md) **значение true**. Затем вызовите метод **ипропертипажесите:: онстатусчанже** в указателе [**кбасепропертипаже:: m \_ ппажесите**](cbasepropertypage-m-ppagesite.md) , чтобы проинформировать кадр.

## <a name="examples"></a>Примеры

Следующий пример реагирует на нажатие кнопки, обновляя переменную-член, которая предполагается определить в производном классе. В этом примере также показана вспомогательная функция для задания состояния "грязной" страницы свойств.


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
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

 

 




