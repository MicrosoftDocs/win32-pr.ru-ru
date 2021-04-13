---
title: Агрегирование
description: Агрегирование — это механизм повторного использования объектов, при котором внешний объект предоставляет интерфейсы из внутреннего объекта, как если бы они были реализованы в самом внешнем объекте.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4f11f69f5d7b14047a8138cba93bd503b645a3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339340"
---
# <a name="aggregation"></a><span data-ttu-id="dd362-103">Агрегирование</span><span class="sxs-lookup"><span data-stu-id="dd362-103">Aggregation</span></span>

<span data-ttu-id="dd362-104">Агрегирование — это механизм повторного использования объектов, при котором внешний объект предоставляет интерфейсы из внутреннего объекта, как если бы они были реализованы в самом внешнем объекте.</span><span class="sxs-lookup"><span data-stu-id="dd362-104">Aggregation is the object reuse mechanism in which the outer object exposes interfaces from the inner object as if they were implemented on the outer object itself.</span></span> <span data-ttu-id="dd362-105">Это полезно, когда внешний объект делегирует каждый вызов к одному из своих интерфейсов во внутреннем объекте.</span><span class="sxs-lookup"><span data-stu-id="dd362-105">This is useful when the outer object delegates every call to one of its interfaces to the same interface in the inner object.</span></span> <span data-ttu-id="dd362-106">Агрегирование доступно для удобства, чтобы избежать дополнительных затрат на реализацию во внешнем объекте в данном случае.</span><span class="sxs-lookup"><span data-stu-id="dd362-106">Aggregation is available as a convenience to avoid extra implementation overhead in the outer object in this case.</span></span> <span data-ttu-id="dd362-107">В действительности агрегирование является специализированным вариантом [включения или делегирования](containment-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="dd362-107">Aggregation is actually a specialized case of [containment/delegation](containment-delegation.md).</span></span>

<span data-ttu-id="dd362-108">Статистическая обработка практически проста в реализации как вложенность, за исключением трех функций [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="dd362-108">Aggregation is almost as simple to implement as containment is, except for the three [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) functions: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="dd362-109">Перехват заключается в том, что с точки зрения клиента любая функция **IUnknown** во внешнем объекте должна влиять на внешний объект.</span><span class="sxs-lookup"><span data-stu-id="dd362-109">The catch is that from the client's perspective, any **IUnknown** function on the outer object must affect the outer object.</span></span> <span data-ttu-id="dd362-110">То есть, **AddRef** и **Release** влияют на внешний объект, а **QueryInterface** — на доступ ко всем интерфейсам, доступным на внешнем объекте.</span><span class="sxs-lookup"><span data-stu-id="dd362-110">That is, **AddRef** and **Release** affect the outer object and **QueryInterface** exposes all the interfaces available on the outer object.</span></span> <span data-ttu-id="dd362-111">Однако если внешний объект просто предоставляет интерфейс внутреннего объекта как собственный, то члены **IUnknown** этого внутреннего объекта, вызываемые через этот интерфейс, будут вести себя иначе, чем эти члены **IUnknown** в интерфейсах внешнего объекта, абсолютное нарушение правил и свойств, управляющих **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="dd362-111">However, if the outer object simply exposes an inner object's interface as its own, that inner object's **IUnknown** members called through that interface will behave differently than those **IUnknown** members on the outer object's interfaces, an absolute violation of the rules and properties governing **IUnknown**.</span></span>

<span data-ttu-id="dd362-112">Решение состоит в том, что для агрегирования требуется явная реализация [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) для внутреннего объекта и делегирование методов **IUnknown** любого другого интерфейса в методы **IUnknown** внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="dd362-112">The solution is that aggregation requires an explicit implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) on the inner object and delegation of the **IUnknown** methods of any other interface to the outer object's **IUnknown** methods.</span></span>

## <a name="creating-aggregable-objects"></a><span data-ttu-id="dd362-113">Создание объектов Аггрегабле</span><span class="sxs-lookup"><span data-stu-id="dd362-113">Creating Aggregable Objects</span></span>

<span data-ttu-id="dd362-114">Создание объектов, которые могут быть агрегированными, является необязательным; Однако это просто и предоставляет значительные преимущества.</span><span class="sxs-lookup"><span data-stu-id="dd362-114">Creating objects that can be aggregated is optional; however, it is simple to do and provides significant benefits.</span></span> <span data-ttu-id="dd362-115">Для создания объекта аггрегабле применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="dd362-115">The following rules apply to creating an aggregable object:</span></span>

-   <span data-ttu-id="dd362-116">Реализация аггрегабле (или внутреннего) объекта [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для своего интерфейса [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) определяет счетчик ссылок внутреннего объекта, и эта реализация не должна делегироваться неизвестному внешнему объекту (управляющий **IUnknown**).</span><span class="sxs-lookup"><span data-stu-id="dd362-116">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface controls the inner object's reference count, and this implementation must not delegate to the outer object's unknown (the controlling **IUnknown**).</span></span>
-   <span data-ttu-id="dd362-117">Реализация аггрегабле (или внутреннего) объекта [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для других интерфейсов должна быть делегирована управляющему [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) и не должна напрямую влиять на счетчик ссылок внутреннего объекта.</span><span class="sxs-lookup"><span data-stu-id="dd362-117">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its other interfaces must delegate to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and must not directly affect the inner object's reference count.</span></span>
-   <span data-ttu-id="dd362-118">Внутренний [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) должен реализовывать [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) только для внутреннего объекта.</span><span class="sxs-lookup"><span data-stu-id="dd362-118">The inner [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) must implement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) only for the inner object.</span></span>
-   <span data-ttu-id="dd362-119">Объект аггрегабле не должен вызывать [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) при удержании ссылки на управляющий указатель [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dd362-119">The aggregable object must not call [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) when holding a reference to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="dd362-120">При создании объекта, если запрашивается какой-либо интерфейс, отличный от [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , создание завершится ошибкой с помощью \_ интерфейса E.</span><span class="sxs-lookup"><span data-stu-id="dd362-120">When the object is created, if any interface other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) is requested, the creation must fail with E\_NOINTERFACE.</span></span>

<span data-ttu-id="dd362-121">В следующем фрагменте кода показана правильная реализация объекта аггрегабле с помощью метода вложенного класса реализации интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="dd362-121">The following code fragment illustrates a correct implementation of an aggregable object by using the nested class method of implementing interfaces:</span></span>


```C++
// CSomeObject is an aggregable object that implements 
// IUnknown and ISomeInterface 
class CSomeObject : public IUnknown 
{ 
    private: 
        DWORD        m_cRef;         // Object reference count 
        IUnknown*    m_pUnkOuter;    // Controlling IUnknown, no AddRef 
 
        // Nested class to implement the ISomeInterface interface 
        class CImpSomeInterface : public ISomeInterface 
        { 
            friend class CSomeObject ; 
            private: 
                DWORD    m_cRef;    // Interface ref-count, for debugging 
                IUnknown*    m_pUnkOuter;    // Controlling IUnknown 
            public: 
                CImpSomeInterface() { m_cRef = 0;   }; 
                ~ CImpSomeInterface(void) {}; 
 
                // IUnknown members delegate to the outer unknown 
                // IUnknown members do not control lifetime of object 
                STDMETHODIMP     QueryInterface(REFIID riid, void** ppv) 
                {    return m_pUnkOuter->QueryInterface(riid,ppv);   }; 
 
                STDMETHODIMP_(DWORD) AddRef(void) 
                {    return m_pUnkOuter->AddRef();   }; 
 
                STDMETHODIMP_(DWORD) Release(void) 
                {    return m_pUnkOuter->Release();   }; 
 
                // ISomeInterface members 
                STDMETHODIMP SomeMethod(void) 
                {    return S_OK;   }; 
        } ; 
        CImpSomeInterface m_ImpSomeInterface ; 
    public: 
        CSomeObject(IUnknown * pUnkOuter) 
        { 
            m_cRef=0; 
            // No AddRef necessary if non-NULL as we're aggregated. 
            m_pUnkOuter=pUnkOuter; 
            m_ImpSomeInterface.m_pUnkOuter=pUnkOuter; 
        } ; 
        ~CSomeObject(void) {} ; 
 
        // Static member function for creating new instances (don't use 
        // new directly). Protects against outer objects asking for 
        // interfaces other than Iunknown. 
        static HRESULT Create(IUnknown* pUnkOuter, REFIID riid, void **ppv) 
        { 
            CSomeObject*        pObj; 
            if (pUnkOuter != NULL && riid != IID_IUnknown) 
                return CLASS_E_NOAGGREGATION; 
            pObj = new CSomeObject(pUnkOuter); 
            if (pObj == NULL) 
                return E_OUTOFMEMORY; 
            // Set up the right unknown for delegation (the non-
            // aggregation case) 
            if (pUnkOuter == NULL) 
            {
                pObj->m_pUnkOuter = (IUnknown*)pObj ; 
                pObj->m_ImpSomeInterface.m_pUnkOuter = (IUnknown*)pObj;
            }
            HRESULT hr; 
            if (FAILED(hr = pObj->QueryInterface(riid, (void**)ppv))) 
                delete pObj ; 
            return hr; 
        } 
 
        // Inner IUnknown members, non-delegating 
        // Inner QueryInterface only controls inner object 
        STDMETHODIMP QueryInterface(REFIID riid, void** ppv) 
        { 
            *ppv=NULL; 
            if (riid == IID_IUnknown) 
                *ppv=this; 
            if (riid == IID_ISomeInterface) 
                *ppv=&m_ImpSomeInterface; 
            if (NULL==*ppv) 
                return ResultFromScode(E_NOINTERFACE); 
            ((IUnknown*)*ppv)->AddRef(); 
            return NOERROR; 
        } ; 
        STDMETHODIMP_(DWORD) AddRef(void) 
        {    return ++m_cRef; }; 
        STDMETHODIMP_(DWORD) Release(void) 
        { 
            if (--m_cRef != 0) 
                return m_cRef; 
            delete this; 
            return 0; 
        }; 
}; 
 
```



## <a name="aggregating-objects"></a><span data-ttu-id="dd362-122">Статистическая обработка объектов</span><span class="sxs-lookup"><span data-stu-id="dd362-122">Aggregating Objects</span></span>

<span data-ttu-id="dd362-123">При разработке объекта аггрегабле применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="dd362-123">When developing an aggregable object, the following rules apply:</span></span>

-   <span data-ttu-id="dd362-124">При создании внутреннего объекта внешний объект должен явно запрашивать его [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="dd362-124">When creating the inner object, the outer object must explicitly ask for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="dd362-125">Внешний объект должен защищать свою реализацию [**выпуска**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) от повторного входа со искусственным счетчиком ссылок вокруг кода уничтожения.</span><span class="sxs-lookup"><span data-stu-id="dd362-125">The outer object must protect its implementation of [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) from reentrancy with an artificial reference count around its destruction code.</span></span>
-   <span data-ttu-id="dd362-126">Внешний объект должен вызвать свой метод управления  [**выпуском**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) IUnknown, если он запрашивает указатель на любой из интерфейсов внутреннего объекта.</span><span class="sxs-lookup"><span data-stu-id="dd362-126">The outer object must call its controlling **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method if it queries for a pointer to any of the inner object's interfaces.</span></span> <span data-ttu-id="dd362-127">Чтобы освободить этот указатель, внешний объект вызывает свой управляющий метод  [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) для **IUnknown**, за которым следует **выпуск** на указателе внутреннего объекта.</span><span class="sxs-lookup"><span data-stu-id="dd362-127">To free this pointer, the outer object calls its controlling **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method, followed by **Release** on the inner object's pointer.</span></span>
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   <span data-ttu-id="dd362-128">Внешний объект не должен явным образом делегировать запрос для любого неопознанного интерфейса внутреннему объекту, если это поведение не является особенно намерением внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="dd362-128">The outer object must not blindly delegate a query for any unrecognized interface to the inner object, unless that behavior is specifically the intention of the outer object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd362-129">См. также</span><span class="sxs-lookup"><span data-stu-id="dd362-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd362-130">Включение и делегирование</span><span class="sxs-lookup"><span data-stu-id="dd362-130">Containment/Delegation</span></span>](containment-delegation.md)
</dt> </dl>

 

 