---
description: Поддержка нескольких обратных вызовов
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: Поддержка нескольких обратных вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77a15899488e44ea3c1499b11af65894d47483c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812598"
---
# <a name="supporting-multiple-callbacks"></a><span data-ttu-id="65ce7-103">Поддержка нескольких обратных вызовов</span><span class="sxs-lookup"><span data-stu-id="65ce7-103">Supporting Multiple Callbacks</span></span>

<span data-ttu-id="65ce7-104">При вызове более одного асинхронного метода для каждого из них требуется отдельная реализация [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="65ce7-104">If you call more than one asynchronous method, each one requires a separate implementation of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="65ce7-105">Однако может возникнуть необходимость реализовать обратные вызовы внутри одного класса C++.</span><span class="sxs-lookup"><span data-stu-id="65ce7-105">However, you might want to implement the callbacks inside a single C++ class.</span></span> <span data-ttu-id="65ce7-106">Класс может иметь только один метод **Invoke** , поэтому одно решение заключается в предоставлении вспомогательного класса, который делегирует вызовы **вызова** другому методу класса контейнера.</span><span class="sxs-lookup"><span data-stu-id="65ce7-106">The class can have only one **Invoke** method, so one solution is to provide a helper class that delegates **Invoke** calls to another method on a container class.</span></span>

<span data-ttu-id="65ce7-107">В следующем коде показан шаблон класса с именем `AsyncCallback` , демонстрирующий этот подход.</span><span class="sxs-lookup"><span data-stu-id="65ce7-107">The following code shows a class template named `AsyncCallback`, which demonstrates this approach.</span></span>


```C++
//////////////////////////////////////////////////////////////////////////
//  AsyncCallback [template]
//
//  Description:
//  Helper class that routes IMFAsyncCallback::Invoke calls to a class
//  method on the parent class.
//
//  Usage:
//  Add this class as a member variable. In the parent class constructor,
//  initialize the AsyncCallback class like this:
//      m_cb(this, &CYourClass::OnInvoke)
//  where
//      m_cb       = AsyncCallback object
//      CYourClass = parent class
//      OnInvoke   = Method in the parent class to receive Invoke calls.
//
//  The parent's OnInvoke method (you can name it anything you like) must
//  have a signature that matches the InvokeFn typedef below.
//////////////////////////////////////////////////////////////////////////

// T: Type of the parent object
template<class T>
class AsyncCallback : public IMFAsyncCallback
{
public:
    typedef HRESULT (T::*InvokeFn)(IMFAsyncResult *pAsyncResult);

    AsyncCallback(T *pParent, InvokeFn fn) : m_pParent(pParent), m_pInvokeFn(fn)
    {
    }

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(AsyncCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef() {
        // Delegate to parent class.
        return m_pParent->AddRef();
    }
    STDMETHODIMP_(ULONG) Release() {
        // Delegate to parent class.
        return m_pParent->Release();
    }

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult)
    {
        return (m_pParent->*m_pInvokeFn)(pAsyncResult);
    }

    T *m_pParent;
    InvokeFn m_pInvokeFn;
};
```



<span data-ttu-id="65ce7-108">Параметр шаблона — это имя класса контейнера.</span><span class="sxs-lookup"><span data-stu-id="65ce7-108">The template parameter is the name of container class.</span></span> <span data-ttu-id="65ce7-109">`AsyncCallback`Конструктор имеет два параметра: указатель на класс контейнера и адрес метода обратного вызова в классе контейнера.</span><span class="sxs-lookup"><span data-stu-id="65ce7-109">The `AsyncCallback` constructor has two parameters: a pointer to the container class, and the address of a callback method on the container class.</span></span> <span data-ttu-id="65ce7-110">Класс контейнера может иметь несколько экземпляров `AsyncCallback` класса как переменные члена, по одному для каждого асинхронного метода.</span><span class="sxs-lookup"><span data-stu-id="65ce7-110">The container class can have multiple instances of the `AsyncCallback` class as member variables, one for each asynchronous method.</span></span> <span data-ttu-id="65ce7-111">Когда класс контейнера вызывает асинхронный метод, он использует интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) соответствующего `AsyncCallback` объекта.</span><span class="sxs-lookup"><span data-stu-id="65ce7-111">When the container class calls an asynchronous method, it use the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface of the appropriate `AsyncCallback` object.</span></span> <span data-ttu-id="65ce7-112">Когда `AsyncCallback` вызывается метод [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) объекта, вызов делегируется правильному методу в классе контейнера.</span><span class="sxs-lookup"><span data-stu-id="65ce7-112">When the `AsyncCallback` object's [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called, the call is delegated to the correct method on the container class.</span></span>

<span data-ttu-id="65ce7-113">`AsyncCallback`Объект также делегирует вызовы метода **AddRef** и **Release** классу контейнера, поэтому класс контейнера управляет временем существования `AsyncCallback` объекта.</span><span class="sxs-lookup"><span data-stu-id="65ce7-113">The `AsyncCallback` object also delegates **AddRef** and **Release** calls to the container class, so the container class manages the lifetime of the `AsyncCallback` object.</span></span> <span data-ttu-id="65ce7-114">Это гарантирует, что `AsyncCallback` объект не будет удален до удаления самого объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="65ce7-114">This guarantees that the `AsyncCallback` object will not be deleted until the container object itself is deleted.</span></span>

<span data-ttu-id="65ce7-115">В следующем коде показано, как использовать этот шаблон:</span><span class="sxs-lookup"><span data-stu-id="65ce7-115">The following code shows how to use this template:</span></span>


```C++
#pragma warning( push )
#pragma warning( disable : 4355 )  // 'this' used in base member initializer list

class CMyObject : public IUnknown
{
public:

    CMyObject() : m_CB(this, &CMyObject::OnInvoke)
    {
        // Other initialization here.
    }

    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);


private:

    AsyncCallback<CMyObject>   m_CB;

    HRESULT OnInvoke(IMFAsyncResult *pAsyncResult);
};

#pragma warning( pop )
```



<span data-ttu-id="65ce7-116">В этом примере класс контейнера называется `CMyObject` .</span><span class="sxs-lookup"><span data-stu-id="65ce7-116">In this example, the container class is named `CMyObject`.</span></span> <span data-ttu-id="65ce7-117">Переменная-член *m \_ CB* — это `AsyncCallback` объект.</span><span class="sxs-lookup"><span data-stu-id="65ce7-117">The *m\_CB* member variable is a `AsyncCallback` object.</span></span> <span data-ttu-id="65ce7-118">В `CMyObject` конструкторе переменная-член *m \_ CB* инициализируется с помощью адреса `CMyObject::OnInvoke` метода.</span><span class="sxs-lookup"><span data-stu-id="65ce7-118">In the `CMyObject` constructor, the *m\_CB* member variable is initialized with the address of the `CMyObject::OnInvoke` method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65ce7-119">См. также</span><span class="sxs-lookup"><span data-stu-id="65ce7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65ce7-120">Асинхронные методы обратного вызова</span><span class="sxs-lookup"><span data-stu-id="65ce7-120">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



