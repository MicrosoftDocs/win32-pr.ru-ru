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
# <a name="supporting-multiple-callbacks"></a>Поддержка нескольких обратных вызовов

При вызове более одного асинхронного метода для каждого из них требуется отдельная реализация [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Однако может возникнуть необходимость реализовать обратные вызовы внутри одного класса C++. Класс может иметь только один метод **Invoke** , поэтому одно решение заключается в предоставлении вспомогательного класса, который делегирует вызовы **вызова** другому методу класса контейнера.

В следующем коде показан шаблон класса с именем `AsyncCallback` , демонстрирующий этот подход.


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



Параметр шаблона — это имя класса контейнера. `AsyncCallback`Конструктор имеет два параметра: указатель на класс контейнера и адрес метода обратного вызова в классе контейнера. Класс контейнера может иметь несколько экземпляров `AsyncCallback` класса как переменные члена, по одному для каждого асинхронного метода. Когда класс контейнера вызывает асинхронный метод, он использует интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) соответствующего `AsyncCallback` объекта. Когда `AsyncCallback` вызывается метод [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) объекта, вызов делегируется правильному методу в классе контейнера.

`AsyncCallback`Объект также делегирует вызовы метода **AddRef** и **Release** классу контейнера, поэтому класс контейнера управляет временем существования `AsyncCallback` объекта. Это гарантирует, что `AsyncCallback` объект не будет удален до удаления самого объекта контейнера.

В следующем коде показано, как использовать этот шаблон:


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



В этом примере класс контейнера называется `CMyObject` . Переменная-член *m \_ CB* — это `AsyncCallback` объект. В `CMyObject` конструкторе переменная-член *m \_ CB* инициализируется с помощью адреса `CMyObject::OnInvoke` метода.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Асинхронные методы обратного вызова](asynchronous-callback-methods.md)
</dt> </dl>

 

 



