---
description: 'переопределите метод кбасепропертипаже:: onactivate, чтобы инициализировать диалоговое окно в процессе создания страницы свойств фильтра для настраиваемого фильтра DirectShow.'
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Шаг 6. Инициализация диалогового окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2ac2dbc4e8ed59317db3db46079b087e4afcf0fa8dce315aa2a0cbd45d502a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102314"
---
# <a name="step-6-initialize-the-dialog"></a>Шаг 6. Инициализация диалогового окна

Переопределите метод [**кбасепропертипаже:: OnActivate**](cbasepropertypage-onactivate.md) , чтобы инициализировать диалоговое окно. В этом примере на странице свойств используется элемент управления "ползунок", поэтому первым шагом в **OnActivate** является инициализация общей библиотеки элементов управления. Затем метод инициализирует элемент управления Slider, используя текущее значение свойства насыщенности фильтра:


```C++
HRESULT CGrayProp::OnActivate(void)
{
    INITCOMMONCONTROLSEX icc;
    icc.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icc.dwICC = ICC_BAR_CLASSES;
    if (InitCommonControlsEx(&icc) == FALSE)
    {
        return E_FAIL;
    }

    ASSERT(m_pGray != NULL);
    HRESULT hr = m_pGray->GetSaturation(&m_lVal);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0,
            MAKELONG(SATURATION_MIN, SATURATION_MAX));

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 
            (SATURATION_MAX - SATURATION_MIN) / 10, 0);

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lVal);
    }
    return hr;
}
```



Далее. [Шаг 7. Обработку сообщений окна](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



