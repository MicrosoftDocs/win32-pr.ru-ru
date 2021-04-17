---
description: Шаг 7.
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: Шаг 7. Обработку сообщений окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd1c44dd65a4f9f430b4223f0a5a0e4763af981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674171"
---
# <a name="step-7-handle-window-messages"></a>Шаг 7. Обработку сообщений окна

Переопределите метод [**кбасепропертипаже:: онрецеивемессаже**](cbasepropertypage-onreceivemessage.md) , чтобы обновить элементы управления диалогового окна в ответ на введенные пользователем данные. Если вы не обрабатываете конкретное сообщение, вызовите метод **онрецеивемессаже** для родительского класса. Каждый раз, когда пользователь изменяет свойство, выполните следующие действия.

-   Присвойте переменной **m \_ бдирти** страницы свойств **значение true**.
-   Вызовите метод **ипропертипажесите:: онстатусчанже** рамки свойства с \_ флагом проппажестатус Dirty. Этот флаг информирует кадр свойств о том, что необходимо включить кнопку **Применить** . Элемент [**кбасепропертипаже:: m \_ ппажесите**](cbasepropertypage-m-ppagesite.md) содержит указатель на интерфейс **ипропертипажесите** .

Чтобы упростить этот шаг, можно добавить на страницу свойств следующую вспомогательную функцию.


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



Вызывайте этот частный метод внутри **онрецеивемессаже** каждый раз, когда действие пользователя изменяет свойство, как показано в следующем примере:


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



На странице свойств в этом примере есть два элемента управления: ползунок и кнопка **вернуться к использованию по умолчанию** . Если пользователь прокручивает ползунок, на странице свойств задается значение насыщенности фильтра. Если пользователь нажимает кнопку, страница свойств восстанавливает значение насыщенности по умолчанию для фильтра. В каждом случае m \_ лневвал содержит текущее значение, а m \_ лвал содержит исходное значение. Значение m \_ лвал не обновляется до тех пор, пока пользователь не зафиксирует изменение, что происходит, когда пользователь нажимает кнопку **ОК** или **Применить** в рамке свойства.

Далее. [Шаг 8. Применить изменения свойств](step-8--apply-property-changes.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



