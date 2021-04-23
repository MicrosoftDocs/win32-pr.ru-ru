---
description: Принцип работы IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Принцип работы IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139290"
---
# <a name="how-iunknown-works"></a><span data-ttu-id="2b37d-103">Принцип работы IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b37d-103">How IUnknown Works</span></span>

<span data-ttu-id="2b37d-104">Методы в **IUnknown** позволяют приложению запрашивать интерфейсы в компоненте и управлять счетчиком ссылок компонента.</span><span class="sxs-lookup"><span data-stu-id="2b37d-104">The methods in **IUnknown** enable an application to query for interfaces on the component and manage the component's reference count.</span></span>

<span data-ttu-id="2b37d-105">**Количество ссылок**</span><span class="sxs-lookup"><span data-stu-id="2b37d-105">**Reference Count**</span></span>

<span data-ttu-id="2b37d-106">Счетчик ссылок — это внутренняя переменная, которая увеличивается в методе **AddRef** и уменьшается в методе **Release** .</span><span class="sxs-lookup"><span data-stu-id="2b37d-106">The reference count is an internal variable, incremented in the **AddRef** method and decremented in the **Release** method.</span></span> <span data-ttu-id="2b37d-107">Базовые классы управляют счетчиком ссылок и синхронизируют доступ к счетчику ссылок между несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="2b37d-107">The base classes manage the reference count and synchronize access to the reference count among multiple threads.</span></span>

<span data-ttu-id="2b37d-108">**Запросы интерфейса**</span><span class="sxs-lookup"><span data-stu-id="2b37d-108">**Interface Queries**</span></span>

<span data-ttu-id="2b37d-109">Запросы к интерфейсу также просты.</span><span class="sxs-lookup"><span data-stu-id="2b37d-109">Querying for an interface is also straightforward.</span></span> <span data-ttu-id="2b37d-110">Вызывающий объект передает два параметра: идентификатор интерфейса (IID) и адрес указателя.</span><span class="sxs-lookup"><span data-stu-id="2b37d-110">The caller passes two parameters: an interface identifier (IID), and the address of a pointer.</span></span> <span data-ttu-id="2b37d-111">Если компонент поддерживает запрошенный интерфейс, он устанавливает указатель на интерфейс, увеличивает значение счетчика ссылок и возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2b37d-111">If the component supports the requested interface, it sets the pointer to the interface, increments its own reference count, and returns S\_OK.</span></span> <span data-ttu-id="2b37d-112">В противном случае он устанавливает указатель на **null** и ВОЗВРАЩАЕТ E \_ Interface.</span><span class="sxs-lookup"><span data-stu-id="2b37d-112">Otherwise, it sets the pointer to **NULL** and returns E\_NOINTERFACE.</span></span> <span data-ttu-id="2b37d-113">В следующем псевдокоде показана общая структура метода **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="2b37d-113">The following pseudocode shows the general outline of the **QueryInterface** method.</span></span> <span data-ttu-id="2b37d-114">Статистическая обработка компонентов, описанная в следующем разделе, содержит некоторую дополнительную сложность.</span><span class="sxs-lookup"><span data-stu-id="2b37d-114">Component aggregation, described in the next section, introduces some additional complexity.</span></span>


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



<span data-ttu-id="2b37d-115">Единственным различием между методом **QueryInterface** одного компонента и методом **QueryInterface** другого является список идентификаторов IID, которые проверяет каждый компонент.</span><span class="sxs-lookup"><span data-stu-id="2b37d-115">The only difference between the **QueryInterface** method of one component and the **QueryInterface** method of another is the list of IIDs that each component tests.</span></span> <span data-ttu-id="2b37d-116">Для каждого интерфейса, поддерживаемого компонентом, компонент должен проверить идентификатор IID этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b37d-116">For every interface that the component supports, the component must test for the IID of that interface.</span></span>

<span data-ttu-id="2b37d-117">**Агрегирование и делегирование**</span><span class="sxs-lookup"><span data-stu-id="2b37d-117">**Aggregation and Delegation**</span></span>

<span data-ttu-id="2b37d-118">Агрегирование компонентов должно быть прозрачным для вызывающего.</span><span class="sxs-lookup"><span data-stu-id="2b37d-118">Component aggregation must be transparent to the caller.</span></span> <span data-ttu-id="2b37d-119">Таким образом, агрегатная функция должна предоставлять один интерфейс **IUnknown** , а агрегированный компонент отменяет реализацию внешнего компонента.</span><span class="sxs-lookup"><span data-stu-id="2b37d-119">Therefore, the aggregate must expose a single **IUnknown** interface, with the aggregated component deferring to the outer component's implementation.</span></span> <span data-ttu-id="2b37d-120">В противном случае вызывающий объект будет видеть два разных интерфейса **IUnknown** в одной статистической функции.</span><span class="sxs-lookup"><span data-stu-id="2b37d-120">Otherwise, the caller would see two different **IUnknown** interfaces in the same aggregate.</span></span> <span data-ttu-id="2b37d-121">Если компонент не является агрегированным, он использует собственную реализацию.</span><span class="sxs-lookup"><span data-stu-id="2b37d-121">If the component is not aggregated, it uses its own implementation.</span></span>

<span data-ttu-id="2b37d-122">Для поддержки такого поведения компонент должен добавить уровень косвенного обращения.</span><span class="sxs-lookup"><span data-stu-id="2b37d-122">To support this behavior, the component must add a level of indirection.</span></span> <span data-ttu-id="2b37d-123">*Делегированный IUnknown* делегирует работу в соответствующее место: внешнему компоненту, если таковой имеется, или к внутренней версии компонента.</span><span class="sxs-lookup"><span data-stu-id="2b37d-123">A *delegating IUnknown* delegates the work to the appropriate place: to the outer component, if there is one, or to the component's internal version.</span></span> <span data-ttu-id="2b37d-124">*Неделегированный IUnknown* выполняет работу, как описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="2b37d-124">A *nondelegating IUnknown* does the work, as described in the previous section.</span></span>

<span data-ttu-id="2b37d-125">Делегированная версия является общедоступной и хранит имя **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="2b37d-125">The delegating version is public and keeps the name **IUnknown**.</span></span> <span data-ttu-id="2b37d-126">Неделегированная версия переименовывается в [**инонделегатингункновн**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="2b37d-126">The nondelegating version is renamed [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="2b37d-127">Это имя не является частью спецификации COM, поскольку оно не является общедоступным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="2b37d-127">This name is not part of the COM specification, because it is not a public interface.</span></span>

<span data-ttu-id="2b37d-128">Когда клиент создает экземпляр компонента, он вызывает метод **IClassFactory:: CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="2b37d-128">When the client creates an instance of the component, it calls the **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="2b37d-129">Один параметр является указателем на интерфейс **IUnknown** компонента агрегирования или **null** , если новый экземпляр не является агрегатом.</span><span class="sxs-lookup"><span data-stu-id="2b37d-129">One parameter is a pointer to the aggregating component's **IUnknown** interface, or **NULL** if the new instance is not aggregated.</span></span> <span data-ttu-id="2b37d-130">Компонент использует этот параметр для хранения переменной-члена, указывающей, какой интерфейс **IUnknown** следует использовать, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="2b37d-130">The component uses this parameter to store a member variable indicating which **IUnknown** interface to use, as shown in the following example:</span></span>


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



<span data-ttu-id="2b37d-131">Каждый метод в делегированном **интерфейсе IUnknown** вызывает его неделегированный аналог, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="2b37d-131">Each method in the delegating **IUnknown** calls its nondelegating counterpart, as shown in the following example:</span></span>


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



<span data-ttu-id="2b37d-132">По природе делегирования методы делегирования выглядят одинаково в каждом компоненте.</span><span class="sxs-lookup"><span data-stu-id="2b37d-132">By the nature of delegation, the delegating methods look identical in every component.</span></span> <span data-ttu-id="2b37d-133">Изменяются только неделегированные версии.</span><span class="sxs-lookup"><span data-stu-id="2b37d-133">Only the nondelegating versions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b37d-134">См. также</span><span class="sxs-lookup"><span data-stu-id="2b37d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b37d-135">Реализация IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b37d-135">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



