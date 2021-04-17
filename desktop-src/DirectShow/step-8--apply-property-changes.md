---
description: Шаг 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Шаг 8. Применить изменения свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674170"
---
# <a name="step-8-apply-property-changes"></a><span data-ttu-id="88e0c-104">Шаг 8.</span><span class="sxs-lookup"><span data-stu-id="88e0c-104">Step 8.</span></span> <span data-ttu-id="88e0c-105">Применить изменения свойств</span><span class="sxs-lookup"><span data-stu-id="88e0c-105">Apply Property Changes</span></span>

<span data-ttu-id="88e0c-106">Переопределите метод [**кбасепропертипаже:: онаппличанжес**](cbasepropertypage-onapplychanges.md) , чтобы зафиксировать изменения свойств.</span><span class="sxs-lookup"><span data-stu-id="88e0c-106">Override the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method to commit any property changes.</span></span> <span data-ttu-id="88e0c-107">В этом примере \_ переменная m лневвал обновляется всякий раз, когда пользователь прокручивает ползунок.</span><span class="sxs-lookup"><span data-stu-id="88e0c-107">In this example, the m\_lNewVal variable is updated whenever the user scrolls the slider bar.</span></span> <span data-ttu-id="88e0c-108">Метод **онаппличанжес** копирует это значение в \_ переменную m лвал, перезаписывая исходное значение:</span><span class="sxs-lookup"><span data-stu-id="88e0c-108">The **OnApplyChanges** method copies this value into the m\_lVal variable, overwriting the original value:</span></span>


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



<span data-ttu-id="88e0c-109">Далее. [Шаг 9. Отключение страницы свойств](step-9--disconnect-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="88e0c-109">Next: [Step 9. Disconnect the Property Page](step-9--disconnect-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88e0c-110">См. также</span><span class="sxs-lookup"><span data-stu-id="88e0c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88e0c-111">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="88e0c-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



