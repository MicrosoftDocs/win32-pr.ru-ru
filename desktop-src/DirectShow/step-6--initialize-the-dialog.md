---
description: Шаг 6.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Шаг 6. Инициализация диалогового окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282eb03db38c543678fb2c4ef1155e1150b419bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684126"
---
# <a name="step-6-initialize-the-dialog"></a><span data-ttu-id="56240-104">Шаг 6.</span><span class="sxs-lookup"><span data-stu-id="56240-104">Step 6.</span></span> <span data-ttu-id="56240-105">Инициализация диалогового окна</span><span class="sxs-lookup"><span data-stu-id="56240-105">Initialize the Dialog</span></span>

<span data-ttu-id="56240-106">Переопределите метод [**кбасепропертипаже:: OnActivate**](cbasepropertypage-onactivate.md) , чтобы инициализировать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="56240-106">Override the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method to initialize the dialog.</span></span> <span data-ttu-id="56240-107">В этом примере на странице свойств используется элемент управления "ползунок", поэтому первым шагом в **OnActivate** является инициализация общей библиотеки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="56240-107">In this example, the property page uses a slider control, so the first step in **OnActivate** is to initialize the common control library.</span></span> <span data-ttu-id="56240-108">Затем метод инициализирует элемент управления Slider, используя текущее значение свойства насыщенности фильтра:</span><span class="sxs-lookup"><span data-stu-id="56240-108">The method then initializes the slider control using the current value of the filter's saturation property:</span></span>


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



<span data-ttu-id="56240-109">Далее. [Шаг 7. Обработку сообщений окна](step-7--handle-window-messages.md)</span><span class="sxs-lookup"><span data-stu-id="56240-109">Next: [Step 7. Handle Window Messages](step-7--handle-window-messages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="56240-110">См. также</span><span class="sxs-lookup"><span data-stu-id="56240-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56240-111">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="56240-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



