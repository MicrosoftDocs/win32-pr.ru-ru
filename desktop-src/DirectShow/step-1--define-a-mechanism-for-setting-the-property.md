---
description: Шаг 1.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Шаг 1. Определение механизма установки свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a1845cfb3cdf5642378a2321e827e52720a83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673994"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="60ee4-104">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="60ee4-104">Step 1.</span></span> <span data-ttu-id="60ee4-105">Определение механизма установки свойства</span><span class="sxs-lookup"><span data-stu-id="60ee4-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="60ee4-106">Фильтр должен поддерживать связь со страницей свойств, чтобы страница свойств могла устанавливать и получать свойства фильтра.</span><span class="sxs-lookup"><span data-stu-id="60ee4-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="60ee4-107">К возможным механизмам относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="60ee4-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="60ee4-108">Предоставление пользовательского COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="60ee4-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="60ee4-109">Поддержка свойств автоматизации через **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="60ee4-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="60ee4-110">Предоставьте интерфейс **ипропертибаг** и определите набор именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="60ee4-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="60ee4-111">В этом примере используется пользовательский COM-интерфейс с именем Исатуратион.</span><span class="sxs-lookup"><span data-stu-id="60ee4-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="60ee4-112">Это не реальный интерфейс DirectShow. он определен только для этого примера.</span><span class="sxs-lookup"><span data-stu-id="60ee4-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="60ee4-113">Начните с объявления интерфейса в файле заголовка вместе с идентификатором интерфейса (IID):</span><span class="sxs-lookup"><span data-stu-id="60ee4-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



<span data-ttu-id="60ee4-114">Можно также определить интерфейс с помощью IDL и использовать компилятор MIDL для создания файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="60ee4-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="60ee4-115">Затем реализуйте пользовательский интерфейс в фильтре.</span><span class="sxs-lookup"><span data-stu-id="60ee4-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="60ee4-116">В этом примере для значения насыщенности фильтра используются методы get и Set.</span><span class="sxs-lookup"><span data-stu-id="60ee4-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="60ee4-117">Обратите внимание, что оба метода защищают \_ элемент m лсатуратион с помощью критической секции.</span><span class="sxs-lookup"><span data-stu-id="60ee4-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



<span data-ttu-id="60ee4-118">Разумеется, сведения о собственной реализации будут отличаться от приведенного здесь примера.</span><span class="sxs-lookup"><span data-stu-id="60ee4-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="60ee4-119">Далее. [Шаг 2. Реализуйте ИспеЦифипропертипажес](step-2--implement-ispecifypropertypages.md).</span><span class="sxs-lookup"><span data-stu-id="60ee4-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="60ee4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="60ee4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60ee4-121">**Класс Ккритсек**</span><span class="sxs-lookup"><span data-stu-id="60ee4-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="60ee4-122">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="60ee4-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



