---
description: Добавьте поддержку COM в процессе записи фильтра преобразования. Это заключительный шаг в этом руководстве.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Шаг 6. Добавление поддержки для COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d51fa440812311edde9ce448916c66721a507
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406777"
---
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="5965a-105">Шаг 6.</span><span class="sxs-lookup"><span data-stu-id="5965a-105">Step 6.</span></span> <span data-ttu-id="5965a-106">Добавление поддержки для COM</span><span class="sxs-lookup"><span data-stu-id="5965a-106">Add Support for COM</span></span>

<span data-ttu-id="5965a-107">Это шаг 6 учебника [Создание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5965a-107">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="5965a-108">Последним шагом является добавление поддержки COM.</span><span class="sxs-lookup"><span data-stu-id="5965a-108">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="5965a-109">Подсчет ссылок</span><span class="sxs-lookup"><span data-stu-id="5965a-109">Reference Counting</span></span>

<span data-ttu-id="5965a-110">Реализовывать [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) или [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)не требуется.</span><span class="sxs-lookup"><span data-stu-id="5965a-110">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="5965a-111">Все классы фильтров и закрепления являются производными от [**кункновн**](cunknown.md), который обрабатывает подсчет ссылок.</span><span class="sxs-lookup"><span data-stu-id="5965a-111">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="5965a-112">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="5965a-112">QueryInterface</span></span>

<span data-ttu-id="5965a-113">Все классы фильтров и закрепления реализуют [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для всех COM-интерфейсов, которые они наследуют.</span><span class="sxs-lookup"><span data-stu-id="5965a-113">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="5965a-114">Например, [**ктрансформфилтер**](ctransformfilter.md) наследует [**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (через [**кбасефилтер**](cbasefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="5965a-114">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="5965a-115">Если фильтр не предоставляет никаких дополнительных интерфейсов, никаких других действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="5965a-115">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="5965a-116">Чтобы предоставить дополнительные интерфейсы, переопределите метод [**кункновн:: нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="5965a-116">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="5965a-117">Например, предположим, что фильтр реализует пользовательский интерфейс с именем Имикустоминтерфаце.</span><span class="sxs-lookup"><span data-stu-id="5965a-117">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="5965a-118">Чтобы предоставить этот интерфейс клиентам, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5965a-118">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="5965a-119">Создайте производный класс фильтра от этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5965a-119">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="5965a-120">Вставьте макрос [**Declare \_ IUnknown**](declare-iunknown.md) в раздел объявления public.</span><span class="sxs-lookup"><span data-stu-id="5965a-120">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="5965a-121">Переопределите [**нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) , чтобы проверить идентификатор IID интерфейса и вернуть указатель на фильтр.</span><span class="sxs-lookup"><span data-stu-id="5965a-121">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="5965a-122">Следующий код показывает эти действия.</span><span class="sxs-lookup"><span data-stu-id="5965a-122">The following code shows these steps:</span></span>


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



<span data-ttu-id="5965a-123">Дополнительные сведения см. [в разделе Реализация IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="5965a-123">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="5965a-124">Создание объектов</span><span class="sxs-lookup"><span data-stu-id="5965a-124">Object Creation</span></span>

<span data-ttu-id="5965a-125">Если вы планируете упаковать фильтр в библиотеке DLL и сделаете его доступным для других клиентов, необходимо поддерживать [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и другие связанные функции COM.</span><span class="sxs-lookup"><span data-stu-id="5965a-125">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="5965a-126">Основная библиотека классов реализует большую часть этого. Вам нужно просто предоставить некоторую информацию о фильтре.</span><span class="sxs-lookup"><span data-stu-id="5965a-126">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="5965a-127">В этом разделе приводится краткий обзор действий.</span><span class="sxs-lookup"><span data-stu-id="5965a-127">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="5965a-128">Дополнительные сведения см. [в разделе Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="5965a-128">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="5965a-129">Сначала напишите статический метод класса, который возвращает новый экземпляр фильтра.</span><span class="sxs-lookup"><span data-stu-id="5965a-129">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="5965a-130">Этот метод можно назвать любым, но подпись должна соответствовать показанной в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="5965a-130">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



<span data-ttu-id="5965a-131">Затем объявите глобальный массив экземпляров класса [**кфакторитемплате**](cfactorytemplate.md) с именем *g \_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="5965a-131">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="5965a-132">Каждый класс **кфакторитемплате** содержит сведения о реестре для одного фильтра.</span><span class="sxs-lookup"><span data-stu-id="5965a-132">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="5965a-133">Несколько фильтров могут находиться в одной библиотеке DLL. просто включите дополнительные записи **кфакторитемплате** .</span><span class="sxs-lookup"><span data-stu-id="5965a-133">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="5965a-134">Можно также объявить другие COM-объекты, например страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5965a-134">You can also declare other COM objects, such as property pages.</span></span>


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



<span data-ttu-id="5965a-135">Определите глобальное целое число с именем *g \_ ктемплатес* , значение которого равно длине массива *\_ шаблонов g* :</span><span class="sxs-lookup"><span data-stu-id="5965a-135">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="5965a-136">Наконец, реализуйте функции регистрации DLL.</span><span class="sxs-lookup"><span data-stu-id="5965a-136">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="5965a-137">В следующем примере показана минимальная реализация для этих функций:</span><span class="sxs-lookup"><span data-stu-id="5965a-137">The following example shows the minimal implementation for these functions:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a><span data-ttu-id="5965a-138">Фильтрация записей реестра</span><span class="sxs-lookup"><span data-stu-id="5965a-138">Filter Registry Entries</span></span>

<span data-ttu-id="5965a-139">В предыдущих примерах показано, как зарегистрировать CLSID фильтра для COM.</span><span class="sxs-lookup"><span data-stu-id="5965a-139">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="5965a-140">Для многих фильтров это достаточно.</span><span class="sxs-lookup"><span data-stu-id="5965a-140">For many filters, this is sufficient.</span></span> <span data-ttu-id="5965a-141">Затем клиент должен создать фильтр с помощью [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и добавить его в граф фильтра, вызвав [**Ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span><span class="sxs-lookup"><span data-stu-id="5965a-141">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="5965a-142">Однако в некоторых случаях может потребоваться предоставить дополнительные сведения о фильтре в реестре.</span><span class="sxs-lookup"><span data-stu-id="5965a-142">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="5965a-143">Эта информация выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5965a-143">This information does the following:</span></span>

-   <span data-ttu-id="5965a-144">Позволяет клиентам обнаруживать фильтр с помощью модуля [сопоставления фильтров](filter-mapper.md) или [перечислителя системных устройств](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="5965a-144">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="5965a-145">Позволяет диспетчеру графа фильтров обнаруживать фильтр во время автоматического построения графа.</span><span class="sxs-lookup"><span data-stu-id="5965a-145">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="5965a-146">В следующем примере фильтр кодировщика RLE регистрируется в категории Video компрессор.</span><span class="sxs-lookup"><span data-stu-id="5965a-146">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="5965a-147">Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5965a-147">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="5965a-148">Обязательно ознакомьтесь с [рекомендациями](guidelines-for-registering-filters.md)по регистрации фильтров, которые описывают рекомендации по регистрации фильтров.</span><span class="sxs-lookup"><span data-stu-id="5965a-148">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



<span data-ttu-id="5965a-149">Кроме того, не обязательно упаковывать фильтры в библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="5965a-149">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="5965a-150">В некоторых случаях можно написать специальный фильтр, предназначенный только для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="5965a-150">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="5965a-151">В этом случае можно скомпилировать класс фильтра непосредственно в приложении и создать его с помощью `new` оператора, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="5965a-151">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="5965a-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5965a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5965a-153">Интеллектуальное подключение</span><span class="sxs-lookup"><span data-stu-id="5965a-153">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="5965a-154">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="5965a-154">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="5965a-155">Написание фильтров преобразования</span><span class="sxs-lookup"><span data-stu-id="5965a-155">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
