---
description: Шаг 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Шаг 9. Отключение страницы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684125"
---
# <a name="step-9-disconnect-the-property-page"></a><span data-ttu-id="e6795-104">Шаг 9.</span><span class="sxs-lookup"><span data-stu-id="e6795-104">Step 9.</span></span> <span data-ttu-id="e6795-105">Отключение страницы свойств</span><span class="sxs-lookup"><span data-stu-id="e6795-105">Disconnect the Property Page</span></span>

<span data-ttu-id="e6795-106">Переопределите метод [**кбасепропертипаже:: ondisconnect**](cbasepropertypage-ondisconnect.md) , чтобы освободить все интерфейсы, полученные в методе **ondisconnect** .</span><span class="sxs-lookup"><span data-stu-id="e6795-106">Override the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method to release any interfaces that you obtained in the **OnConnect** method.</span></span> <span data-ttu-id="e6795-107">Кроме того, если пользователь закрывает страницу свойств без фиксации изменений, следует восстановить исходные значения, если они были изменены.</span><span class="sxs-lookup"><span data-stu-id="e6795-107">Also, if the user dismisses the property sheet without committing the changes, you should restore the original values if they have changed.</span></span> <span data-ttu-id="e6795-108">Нет метода "OnCancel", который вызывается при отмене пользователем, поэтому необходимо отследить, что пользователь вызвал **онаппличанжес**.</span><span class="sxs-lookup"><span data-stu-id="e6795-108">There is no "OnCancel" method that gets called when the user cancels, so you need to keep track of whether the user has called **OnApplyChanges**.</span></span> <span data-ttu-id="e6795-109">В этом примере используется \_ переменная m лвал, описанная выше.</span><span class="sxs-lookup"><span data-stu-id="e6795-109">This example uses the m\_lVal variable, described earlier:</span></span>


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



<span data-ttu-id="e6795-110">Далее. [Шаг 10. Поддержка регистрации COM](step-10--support-com-registration.md)</span><span class="sxs-lookup"><span data-stu-id="e6795-110">Next: [Step 10. Support COM Registration](step-10--support-com-registration.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6795-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e6795-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6795-112">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="e6795-112">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



