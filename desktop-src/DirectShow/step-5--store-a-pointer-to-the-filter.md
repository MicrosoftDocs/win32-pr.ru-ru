---
description: Шаг 5.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Шаг 5. Сохранение указателя на фильтр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265960"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="54edb-104">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="54edb-104">Step 5.</span></span> <span data-ttu-id="54edb-105">Сохранение указателя на фильтр</span><span class="sxs-lookup"><span data-stu-id="54edb-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="54edb-106">Переопределите метод [**кбасепропертипаже:: OnConnect**](cbasepropertypage-onconnect.md) , чтобы сохранить указатель на фильтр.</span><span class="sxs-lookup"><span data-stu-id="54edb-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="54edb-107">В следующем примере запрашивается параметр *Punk* для пользовательского интерфейса исатуратион фильтра:</span><span class="sxs-lookup"><span data-stu-id="54edb-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


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



<span data-ttu-id="54edb-108">Далее. [Шаг 6. Инициализируйте диалоговое окно](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="54edb-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54edb-109">См. также</span><span class="sxs-lookup"><span data-stu-id="54edb-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54edb-110">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="54edb-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



