---
description: Сохранение указателя на фильтр в рамках создания страницы свойств фильтра для настраиваемого фильтра DirectShow.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Шаг 5. Сохранение указателя на фильтр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406797"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="ac4b0-104">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="ac4b0-104">Step 5.</span></span> <span data-ttu-id="ac4b0-105">Сохранение указателя на фильтр</span><span class="sxs-lookup"><span data-stu-id="ac4b0-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="ac4b0-106">Переопределите метод [**кбасепропертипаже:: OnConnect**](cbasepropertypage-onconnect.md) , чтобы сохранить указатель на фильтр.</span><span class="sxs-lookup"><span data-stu-id="ac4b0-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="ac4b0-107">В следующем примере запрашивается параметр *Punk* для пользовательского интерфейса исатуратион фильтра:</span><span class="sxs-lookup"><span data-stu-id="ac4b0-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



<span data-ttu-id="ac4b0-108">Далее. [Шаг 6. Инициализируйте диалоговое окно](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="ac4b0-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac4b0-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ac4b0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac4b0-110">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="ac4b0-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



