---
description: DirectShow реализует IUnknown в базовом классе с именем Кункновн.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Использование Кункновн
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663765"
---
# <a name="using-cunknown"></a><span data-ttu-id="3d89e-103">Использование Кункновн</span><span class="sxs-lookup"><span data-stu-id="3d89e-103">Using CUnknown</span></span>

<span data-ttu-id="3d89e-104">DirectShow реализует [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) в базовом классе с именем [**кункновн**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3d89e-104">DirectShow implements [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in a base class called [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="3d89e-105">**Кункновн** можно использовать для получения других классов, переопределяя только те методы, которые изменяются между компонентами.</span><span class="sxs-lookup"><span data-stu-id="3d89e-105">You can use **CUnknown** to derive other classes, overriding only the methods that change across components.</span></span> <span data-ttu-id="3d89e-106">Большинство других базовых классов в DirectShow являются производными от **кункновн**, поэтому компонент может наследовать непосредственно от **кункновн** или другого базового класса.</span><span class="sxs-lookup"><span data-stu-id="3d89e-106">Most of the other base classes in DirectShow derive from **CUnknown**, so your component can inherit directly from **CUnknown** or from another base class.</span></span>

## <a name="inondelegatingunknown"></a><span data-ttu-id="3d89e-107">инонделегатингункновн</span><span class="sxs-lookup"><span data-stu-id="3d89e-107">INonDelegatingUnknown</span></span>

<span data-ttu-id="3d89e-108">[**Кункновн**](cunknown.md) реализует [**инонделегатингункновн**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3d89e-108">[**CUnknown**](cunknown.md) implements [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="3d89e-109">Он управляет внутренними счетчиками ссылок, и в большинстве случаев производный класс может наследовать два метода подсчета ссылок без изменений.</span><span class="sxs-lookup"><span data-stu-id="3d89e-109">It manages reference counts internally, and in most situations your derived class can inherit the two reference-counting methods with no change.</span></span> <span data-ttu-id="3d89e-110">Имейте в виду, что **кункновн** удаляет себя, когда счетчик ссылок становится равным нулю.</span><span class="sxs-lookup"><span data-stu-id="3d89e-110">Be aware that **CUnknown** deletes itself when the reference count drops to zero.</span></span> <span data-ttu-id="3d89e-111">С другой стороны, необходимо переопределить [**кункновн:: нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md), так как метод в базовом классе возвращает E \_ без интерфейса, если он получает идентификатор IID, отличный от \_ IUnknown.</span><span class="sxs-lookup"><span data-stu-id="3d89e-111">On the other hand, you must override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), because the method in the base class returns E\_NOINTERFACE if it receives any IID other than IID\_IUnknown.</span></span> <span data-ttu-id="3d89e-112">В производном классе проверьте идентификаторов IID интерфейсов, которые поддерживаются, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="3d89e-112">In your derived class, test for the IIDs of interfaces that you support, as shown in the following example:</span></span>


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="3d89e-113">Служебная функция [**IsReference**](getinterface.md) (см. Дополнительные сведения о [**вспомогательных функциях com**](com-helper-functions.md)) задает указатель, увеличивает значение счетчика ссылок потокобезопасным способом и возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3d89e-113">The utility function [**GetInterface**](getinterface.md) (see [**COM Helper Functions**](com-helper-functions.md)) sets the pointer, increments the reference count in a thread-safe way, and returns S\_OK.</span></span> <span data-ttu-id="3d89e-114">В случае по умолчанию вызовите метод базового класса и возвратите результат.</span><span class="sxs-lookup"><span data-stu-id="3d89e-114">In the default case, call the base class method and return the result.</span></span> <span data-ttu-id="3d89e-115">Если вы наследуете от другого базового класса, вызовите его метод [**нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="3d89e-115">If you derive from another base class, call its [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method instead.</span></span> <span data-ttu-id="3d89e-116">Это позволяет поддерживать все интерфейсы, поддерживаемые родительским классом.</span><span class="sxs-lookup"><span data-stu-id="3d89e-116">This enables you to support all the interfaces that the parent class supports.</span></span>

## <a name="iunknown"></a><span data-ttu-id="3d89e-117">IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d89e-117">IUnknown</span></span>

<span data-ttu-id="3d89e-118">Как упоминалось ранее, делегированная версия [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) одинакова для каждого компонента, так как она ничего не вызывает правильного экземпляра неделегированной версии.</span><span class="sxs-lookup"><span data-stu-id="3d89e-118">As mentioned earlier, the delegating version of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is the same for every component, because it does nothing more than invoke the correct instance of the nondelegating version.</span></span> <span data-ttu-id="3d89e-119">Для удобства файл заголовка Комбасе. h содержит макрос, [**Declare \_ IUnknown**](declare-iunknown.md), который объявляет три делегированных метода как встроенные методы.</span><span class="sxs-lookup"><span data-stu-id="3d89e-119">For convenience, the header file Combase.h contains a macro, [**DECLARE\_IUNKNOWN**](declare-iunknown.md), which declares the three delegating methods as inline methods.</span></span> <span data-ttu-id="3d89e-120">Он расширяется до следующего кода:</span><span class="sxs-lookup"><span data-stu-id="3d89e-120">It expands to the following code:</span></span>


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



<span data-ttu-id="3d89e-121">Служебная функция [**кункновн::-owner**](cunknown-getowner.md) получает указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) компонента, которому принадлежит этот компонент.</span><span class="sxs-lookup"><span data-stu-id="3d89e-121">The utility function [**CUnknown::GetOwner**](cunknown-getowner.md) retrieves a pointer to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the component that owns this component.</span></span> <span data-ttu-id="3d89e-122">Для агрегированного компонента владельцем является внешний компонент.</span><span class="sxs-lookup"><span data-stu-id="3d89e-122">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="3d89e-123">В противном случае компонент владеет самим собой.</span><span class="sxs-lookup"><span data-stu-id="3d89e-123">Otherwise, the component owns itself.</span></span> <span data-ttu-id="3d89e-124">Включите макрос DECLARE \_ IUnknown в открытый раздел определения класса.</span><span class="sxs-lookup"><span data-stu-id="3d89e-124">Include the DECLARE\_IUNKNOWN macro in the public section of your class definition.</span></span>

## <a name="class-constructor"></a><span data-ttu-id="3d89e-125">Конструктор класса</span><span class="sxs-lookup"><span data-stu-id="3d89e-125">Class Constructor</span></span>

<span data-ttu-id="3d89e-126">Конструктор класса должен вызвать метод-конструктор для родительского класса, а также все, что он делает, относящийся к вашему классу.</span><span class="sxs-lookup"><span data-stu-id="3d89e-126">Your class constructor should invoke the constructor method for the parent class, in addition to anything it does that is specific to your class.</span></span> <span data-ttu-id="3d89e-127">Следующий пример является типичным методом конструктора:</span><span class="sxs-lookup"><span data-stu-id="3d89e-127">The following example is a typical constructor method:</span></span>


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



<span data-ttu-id="3d89e-128">Метод принимает следующие параметры, которые передаются непосредственно в метод конструктора [**кункновн**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="3d89e-128">The method takes the following parameters, which it passes directly to the [**CUnknown**](cunknown.md) constructor method.</span></span>

-   <span data-ttu-id="3d89e-129">*тсзнаме* указывает имя компонента.</span><span class="sxs-lookup"><span data-stu-id="3d89e-129">*tszName* specifies a name for the component.</span></span>
-   <span data-ttu-id="3d89e-130">*Punk* — это указатель на агрегатный [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="3d89e-130">*pUnk* is a pointer to the aggregating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="3d89e-131">*фр* — это указатель на значение HRESULT, указывающее на успешность или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="3d89e-131">*pHr* is a pointer to an HRESULT value, indicating the success or failure of the method.</span></span>

## <a name="summary"></a><span data-ttu-id="3d89e-132">Сводка</span><span class="sxs-lookup"><span data-stu-id="3d89e-132">Summary</span></span>

<span data-ttu-id="3d89e-133">В следующем примере показан производный класс, который поддерживает [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и гипотетический интерфейс с именем исомеинтерфаце:</span><span class="sxs-lookup"><span data-stu-id="3d89e-133">The following example shows a derived class that supports [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and a hypothetical interface named ISomeInterface:</span></span>


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



<span data-ttu-id="3d89e-134">В этом примере показаны следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="3d89e-134">This example illustrates the following points:</span></span>

-   <span data-ttu-id="3d89e-135">Класс [**кункновн**](cunknown.md) реализует интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3d89e-135">The [**CUnknown**](cunknown.md) class implements the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3d89e-136">Новый компонент наследует от **кункновн** и от всех интерфейсов, поддерживаемых компонентом.</span><span class="sxs-lookup"><span data-stu-id="3d89e-136">The new component inherits from **CUnknown** and from any interfaces that the component supports.</span></span> <span data-ttu-id="3d89e-137">Компонент может быть производным от другого базового класса, наследующего от **кункновн**.</span><span class="sxs-lookup"><span data-stu-id="3d89e-137">The component could derive instead from another base class that inherits from **CUnknown**.</span></span>
-   <span data-ttu-id="3d89e-138">Макрос [**Declare \_ IUnknown**](declare-iunknown.md) объявляет делегированные методы [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) как встроенные методы.</span><span class="sxs-lookup"><span data-stu-id="3d89e-138">The [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro declares the delegating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) methods as inline methods.</span></span>
-   <span data-ttu-id="3d89e-139">Класс [**кункновн**](cunknown.md) предоставляет реализацию для [**инонделегатингункновн**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3d89e-139">The [**CUnknown**](cunknown.md) class provides the implementation for [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>
-   <span data-ttu-id="3d89e-140">Для поддержки интерфейса, отличного от [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), производный класс должен переопределить метод [**нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) и проверить идентификатор IID нового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3d89e-140">To support an interface other than [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), the derived class must override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method and test for the IID of the new interface.</span></span>
-   <span data-ttu-id="3d89e-141">Конструктор класса вызывает метод конструктора для [**кункновн**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3d89e-141">The class constructor invokes the constructor method for [**CUnknown**](cunknown.md).</span></span>

<span data-ttu-id="3d89e-142">Следующим шагом при написании фильтра является предоставление приложению возможности создавать новые экземпляры компонента.</span><span class="sxs-lookup"><span data-stu-id="3d89e-142">The next step in writing a filter is to enable an application to create new instances of the component.</span></span> <span data-ttu-id="3d89e-143">Это требует понимания библиотек DLL и их связи с фабриками классов и методами конструктора классов.</span><span class="sxs-lookup"><span data-stu-id="3d89e-143">This requires an understanding of DLLs and their relation to class factories and class constructor methods.</span></span> <span data-ttu-id="3d89e-144">Дополнительные сведения см. [в разделе Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="3d89e-144">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d89e-145">См. также</span><span class="sxs-lookup"><span data-stu-id="3d89e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d89e-146">Реализация IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d89e-146">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 
