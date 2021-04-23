---
description: В этом разделе описывается, как реализовать ведение журнала ошибок в службах редактирования DirectShow.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Создание класса ведения журнала ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655615"
---
# <a name="creating-an-error-logging-class"></a><span data-ttu-id="49e48-103">Создание класса ведения журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="49e48-103">Creating an Error Logging Class</span></span>

<span data-ttu-id="49e48-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="49e48-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="49e48-105">В этом разделе описывается, как реализовать ведение журнала ошибок в [службах редактирования DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="49e48-105">This topic describes how to implement error logging in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="49e48-106">Сначала объявите класс, который будет реализовывать ведение журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="49e48-106">First, declare a class that will implement error logging.</span></span> <span data-ttu-id="49e48-107">Класс наследует интерфейс [**иамеррорлог**](iamerrorlog.md) .</span><span class="sxs-lookup"><span data-stu-id="49e48-107">The class inherits the [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="49e48-108">Он содержит объявления для трех методов **IUnknown** и для одного метода в [иамеррорлог](implementing-iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="49e48-108">It contains declarations for the three **IUnknown** methods, and for the single method in [IAMErrorLog](implementing-iamerrorlog.md).</span></span> <span data-ttu-id="49e48-109">Объявление класса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49e48-109">The class declaration is as follows:</span></span>


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



<span data-ttu-id="49e48-110">Единственной переменной-членом в классе является m \_ лреф, которая содержит счетчик ссылок объекта.</span><span class="sxs-lookup"><span data-stu-id="49e48-110">The only member variable in the class is m\_lRef, which holds the object's reference count.</span></span>

<span data-ttu-id="49e48-111">Затем определите методы в **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="49e48-111">Next, define the methods in **IUnknown**.</span></span> <span data-ttu-id="49e48-112">В следующем примере показана стандартная реализация для этих методов:</span><span class="sxs-lookup"><span data-stu-id="49e48-112">The following example shows a standard implementation for these methods:</span></span>


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



<span data-ttu-id="49e48-113">После создания COM-инфраструктуры теперь можно реализовать интерфейс **иамеррорлог** .</span><span class="sxs-lookup"><span data-stu-id="49e48-113">With the COM framework in place, you can now implement the **IAMErrorLog** interface.</span></span> <span data-ttu-id="49e48-114">В следующем разделе описывается, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="49e48-114">The next section describes how to do this.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49e48-115">См. также</span><span class="sxs-lookup"><span data-stu-id="49e48-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49e48-116">Регистрация ошибок</span><span class="sxs-lookup"><span data-stu-id="49e48-116">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



