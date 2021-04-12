---
description: Предоставление пользовательского распределителя
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Предоставление пользовательского распределителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416604"
---
# <a name="providing-a-custom-allocator"></a><span data-ttu-id="e31d3-103">Предоставление пользовательского распределителя</span><span class="sxs-lookup"><span data-stu-id="e31d3-103">Providing a Custom Allocator</span></span>

<span data-ttu-id="e31d3-104">В этом разделе описывается, как предоставить пользовательский распределитель для фильтра.</span><span class="sxs-lookup"><span data-stu-id="e31d3-104">This section describes how to provide a custom allocator for a filter.</span></span> <span data-ttu-id="e31d3-105">Описываются только соединения [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , но шаги для соединения [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) похожи.</span><span class="sxs-lookup"><span data-stu-id="e31d3-105">Only [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) connections are described, but the steps for an [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connection are similar.</span></span>

<span data-ttu-id="e31d3-106">Сначала определите класс C++ для распределителя.</span><span class="sxs-lookup"><span data-stu-id="e31d3-106">First, define a C++ class for the allocator.</span></span> <span data-ttu-id="e31d3-107">Распределитель может быть производным от одного из стандартных классов распределителя, [**кбасеаллокатор**](cbaseallocator.md) или [**кмемаллокатор**](cmemallocator.md), или можно создать совершенно новый класс распределителя.</span><span class="sxs-lookup"><span data-stu-id="e31d3-107">Your allocator can derive from one of the standard allocator classes, [**CBaseAllocator**](cbaseallocator.md) or [**CMemAllocator**](cmemallocator.md), or you can create an entirely new allocator class.</span></span> <span data-ttu-id="e31d3-108">При создании нового класса он должен предоставлять интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="e31d3-108">If you create a new class, it must expose the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="e31d3-109">Оставшиеся действия зависят от того, принадлежит ли распределитель к входному заводу или выходному закрепления фильтра.</span><span class="sxs-lookup"><span data-stu-id="e31d3-109">The remaining steps depend on whether your allocator belongs to an input pin or an output pin on your filter.</span></span> <span data-ttu-id="e31d3-110">Входные ПИН-коды играют роль, отличную от закрепления вывода на этапе согласования распределителя, так как в конечном итоге выделяется распределитель.</span><span class="sxs-lookup"><span data-stu-id="e31d3-110">Input pins play a different role than output pins during the allocator negotiation phase, because the output pin ultimately selects the allocator.</span></span>

<span data-ttu-id="e31d3-111">**Предоставление пользовательского распределителя для входного ПИН-кода**</span><span class="sxs-lookup"><span data-stu-id="e31d3-111">**Providing a Custom Allocator for an Input Pin**</span></span>

<span data-ttu-id="e31d3-112">Чтобы предоставить распределитель для входного ПИН-кода, переопределите метод [**кбасеинпутпин::-распределителя**](cbaseinputpin-getallocator.md) входного контакта.</span><span class="sxs-lookup"><span data-stu-id="e31d3-112">To provide an allocator for an input pin, override the input pin's [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) method.</span></span> <span data-ttu-id="e31d3-113">В этом методе проверьте переменную члена **m \_ паллокатор** .</span><span class="sxs-lookup"><span data-stu-id="e31d3-113">Within this method, check the **m\_pAllocator** member variable.</span></span> <span data-ttu-id="e31d3-114">Если эта переменная не имеет **значение NULL**, это означает, что распределитель уже выбран для этого соединения, поэтому метод методаического **распределителя** должен возвращать указатель на этот распределитель.</span><span class="sxs-lookup"><span data-stu-id="e31d3-114">If this variable is non-**NULL**, it means the allocator has already been selected for this connection, so the **GetAllocator** method must return a pointer to that allocator.</span></span> <span data-ttu-id="e31d3-115">Если значение **m \_ Паллокатор** равно **null**, это означает, что распределитель не выбран, **поэтому метод метода** должен возвращать указатель на предпочтительный распределитель ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="e31d3-115">If **m\_pAllocator** is **NULL**, it means the allocator has not been selected, so the **GetAllocator** method should return a pointer to the input pin's preferred allocator.</span></span> <span data-ttu-id="e31d3-116">В этом случае создайте экземпляр пользовательского распределителя и возвратите его указатель [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="e31d3-116">In that case, create an instance of your custom allocator and return its [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) pointer.</span></span> <span data-ttu-id="e31d3-117">В следующем коде показано, как реализовать метод методаического **распределителя** :</span><span class="sxs-lookup"><span data-stu-id="e31d3-117">The following code shows how to implement the **GetAllocator** method:</span></span>


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="e31d3-118">Когда вышестоящий фильтр выбирает распределитель, он вызывает метод [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) входного контакта.</span><span class="sxs-lookup"><span data-stu-id="e31d3-118">When the upstream filter selects an allocator, it calls the input pin's [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span> <span data-ttu-id="e31d3-119">Переопределите метод [**кбасеинпутпин:: нотифяллокатор**](cbaseinputpin-notifyallocator.md) , чтобы проверить свойства распределителя.</span><span class="sxs-lookup"><span data-stu-id="e31d3-119">Override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method to check the allocator properties.</span></span> <span data-ttu-id="e31d3-120">В некоторых случаях входной ПИН-код может отклонить распределитель, если он не является пользовательским распределителем, хотя это может привести к сбою всего соединения с ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="e31d3-120">In some cases, the input pin might reject the allocator if it is not your custom allocator, although this may cause the entire pin connection to fail.</span></span>

<span data-ttu-id="e31d3-121">**Предоставление пользовательского распределителя для выходного ПИН-кода**</span><span class="sxs-lookup"><span data-stu-id="e31d3-121">**Providing a Custom Allocator for an Output Pin**</span></span>

<span data-ttu-id="e31d3-122">Чтобы предоставить распределитель для выходного ПИН-кода, переопределите метод [**кбасеаутпутпин:: иниталлокатор**](cbaseoutputpin-initallocator.md) , чтобы создать экземпляр распределителя:</span><span class="sxs-lookup"><span data-stu-id="e31d3-122">To provide an allocator for an output pin, override the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) method to create an instance of your allocator:</span></span>


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="e31d3-123">По умолчанию класс [**кбасеаутпутпин**](cbaseoutputpin.md) запрашивает распределитель из входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="e31d3-123">By default, the [**CBaseOutputPin**](cbaseoutputpin.md) class requests an allocator from the input pin first.</span></span> <span data-ttu-id="e31d3-124">Если распределитель не подходит, закрепление вывода создает собственный распределитель.</span><span class="sxs-lookup"><span data-stu-id="e31d3-124">If that allocator is not suitable, the output pin creates its own allocator.</span></span> <span data-ttu-id="e31d3-125">Чтобы принудительно установить соединение для использования пользовательского распределителя, переопределите метод [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="e31d3-125">To force the connection to use your custom allocator, override the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method.</span></span> <span data-ttu-id="e31d3-126">Однако имейте в виду, что это может препятствовать подключению выходного контакта с определенными фильтрами, так как другой фильтр может также требовать собственный пользовательский распределитель.</span><span class="sxs-lookup"><span data-stu-id="e31d3-126">However, be aware that this can prevent your output pin from connecting with certain filters, because the other filter may also require its own custom allocator.</span></span> <span data-ttu-id="e31d3-127">Третий вариант — переключить порядок: сначала попробуйте выбрать пользовательский распределитель, а затем вернитесь к распределителю другого фильтра.</span><span class="sxs-lookup"><span data-stu-id="e31d3-127">A third option is to switch the order: Try your custom allocator first, and then fall back to the other filter's allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e31d3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e31d3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e31d3-129">Согласование распределителя</span><span class="sxs-lookup"><span data-stu-id="e31d3-129">Negotiating Allocators</span></span>](negotiating-allocators.md)
</dt> </dl>

 

 



