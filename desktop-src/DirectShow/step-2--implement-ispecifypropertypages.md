---
description: Шаг 2.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Шаг 2. Реализация ИспеЦифипропертипажес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683990"
---
# <a name="step-2-implement-ispecifypropertypages"></a><span data-ttu-id="6e6ff-104">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-104">Step 2.</span></span> <span data-ttu-id="6e6ff-105">Реализация ИспеЦифипропертипажес</span><span class="sxs-lookup"><span data-stu-id="6e6ff-105">Implement ISpecifyPropertyPages</span></span>

<span data-ttu-id="6e6ff-106">Затем реализуйте интерфейс **испеЦифипропертипажес** в фильтре.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-106">Next, implement the **ISpecifyPropertyPages** interface in your filter.</span></span> <span data-ttu-id="6e6ff-107">Этот интерфейс содержит один метод, а **-страницы**, который ВОЗВРАЩАЕТ массив идентификаторов CLSID для страниц свойств, поддерживаемых фильтром.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-107">This interface has a single method, **GetPages**, which returns an array of CLSIDs for the property pages that the filter supports.</span></span> <span data-ttu-id="6e6ff-108">В этом примере фильтр содержит одну страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-108">In this example, the filter has a single property page.</span></span> <span data-ttu-id="6e6ff-109">Начните с создания идентификатора CLSID и объявления его в файле заголовка:</span><span class="sxs-lookup"><span data-stu-id="6e6ff-109">Start by generating the CLSID and declaring it in your header file:</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



<span data-ttu-id="6e6ff-110">Теперь реализуйте **метод WebMethod** :</span><span class="sxs-lookup"><span data-stu-id="6e6ff-110">Now implement the **GetPages** method:</span></span>


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



<span data-ttu-id="6e6ff-111">Выделите память для массива с помощью функции **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-111">Allocate memory for the array using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="6e6ff-112">Вызывающий объект выполнит освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-112">The caller will release the memory.</span></span>

<span data-ttu-id="6e6ff-113">Далее. [Шаг 3. Поддержка QueryInterface](step-3--support-queryinterface.md).</span><span class="sxs-lookup"><span data-stu-id="6e6ff-113">Next: [Step 3. Support QueryInterface](step-3--support-queryinterface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e6ff-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6e6ff-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e6ff-115">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="6e6ff-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



