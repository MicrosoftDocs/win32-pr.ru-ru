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
# <a name="step-7-handle-window-messages"></a><span data-ttu-id="32ac7-104">Шаг 7.</span><span class="sxs-lookup"><span data-stu-id="32ac7-104">Step 7.</span></span> <span data-ttu-id="32ac7-105">Обработку сообщений окна</span><span class="sxs-lookup"><span data-stu-id="32ac7-105">Handle Window Messages</span></span>

<span data-ttu-id="32ac7-106">Переопределите метод [**кбасепропертипаже:: онрецеивемессаже**](cbasepropertypage-onreceivemessage.md) , чтобы обновить элементы управления диалогового окна в ответ на введенные пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="32ac7-106">Override the [**CBasePropertyPage::OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) method to update the dialog controls in response to user input.</span></span> <span data-ttu-id="32ac7-107">Если вы не обрабатываете конкретное сообщение, вызовите метод **онрецеивемессаже** для родительского класса.</span><span class="sxs-lookup"><span data-stu-id="32ac7-107">If you don't handle a particular message, call the **OnReceiveMessage** method on the parent class.</span></span> <span data-ttu-id="32ac7-108">Каждый раз, когда пользователь изменяет свойство, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="32ac7-108">Whenever the user changes a property, do the following:</span></span>

-   <span data-ttu-id="32ac7-109">Присвойте переменной **m \_ бдирти** страницы свойств **значение true**.</span><span class="sxs-lookup"><span data-stu-id="32ac7-109">Set the **m\_bDirty** variable of the property page to **TRUE**.</span></span>
-   <span data-ttu-id="32ac7-110">Вызовите метод **ипропертипажесите:: онстатусчанже** рамки свойства с \_ флагом проппажестатус Dirty.</span><span class="sxs-lookup"><span data-stu-id="32ac7-110">Call the **IPropertyPageSite::OnStatusChange** method of the property frame with the PROPPAGESTATUS\_DIRTY flag.</span></span> <span data-ttu-id="32ac7-111">Этот флаг информирует кадр свойств о том, что необходимо включить кнопку **Применить** .</span><span class="sxs-lookup"><span data-stu-id="32ac7-111">This flag informs the property frame that it should enable the **Apply** button.</span></span> <span data-ttu-id="32ac7-112">Элемент [**кбасепропертипаже:: m \_ ппажесите**](cbasepropertypage-m-ppagesite.md) содержит указатель на интерфейс **ипропертипажесите** .</span><span class="sxs-lookup"><span data-stu-id="32ac7-112">The [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member holds a pointer to the **IPropertyPageSite** interface.</span></span>

<span data-ttu-id="32ac7-113">Чтобы упростить этот шаг, можно добавить на страницу свойств следующую вспомогательную функцию.</span><span class="sxs-lookup"><span data-stu-id="32ac7-113">To simplify this step, you can add the following helper function to your property page:</span></span>


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



<span data-ttu-id="32ac7-114">Вызывайте этот частный метод внутри **онрецеивемессаже** каждый раз, когда действие пользователя изменяет свойство, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="32ac7-114">Call this private method inside **OnReceiveMessage** whenever a user action changes a property, as shown in the following example:</span></span>


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



<span data-ttu-id="32ac7-115">На странице свойств в этом примере есть два элемента управления: ползунок и кнопка **вернуться к использованию по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="32ac7-115">The property page in this example has two controls, a slider bar and a **Revert to Default** button.</span></span> <span data-ttu-id="32ac7-116">Если пользователь прокручивает ползунок, на странице свойств задается значение насыщенности фильтра.</span><span class="sxs-lookup"><span data-stu-id="32ac7-116">If the user scrolls the slider bar, the property page sets the saturation value on the filter.</span></span> <span data-ttu-id="32ac7-117">Если пользователь нажимает кнопку, страница свойств восстанавливает значение насыщенности по умолчанию для фильтра.</span><span class="sxs-lookup"><span data-stu-id="32ac7-117">If the user clicks the button, the property page restores the filter's default saturation value.</span></span> <span data-ttu-id="32ac7-118">В каждом случае m \_ лневвал содержит текущее значение, а m \_ лвал содержит исходное значение.</span><span class="sxs-lookup"><span data-stu-id="32ac7-118">In each case, m\_lNewVal holds the current value and m\_lVal holds the original value.</span></span> <span data-ttu-id="32ac7-119">Значение m \_ лвал не обновляется до тех пор, пока пользователь не зафиксирует изменение, что происходит, когда пользователь нажимает кнопку **ОК** или **Применить** в рамке свойства.</span><span class="sxs-lookup"><span data-stu-id="32ac7-119">The value of m\_lVal is not updated until the user commits the change, which happens when the user clicks the **OK** or **Apply** button on the property frame.</span></span>

<span data-ttu-id="32ac7-120">Далее. [Шаг 8. Применить изменения свойств](step-8--apply-property-changes.md).</span><span class="sxs-lookup"><span data-stu-id="32ac7-120">Next: [Step 8. Apply Property Changes](step-8--apply-property-changes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32ac7-121">См. также</span><span class="sxs-lookup"><span data-stu-id="32ac7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32ac7-122">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="32ac7-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



