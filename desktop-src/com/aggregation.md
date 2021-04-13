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
# <a name="aggregation"></a>Агрегирование

Агрегирование — это механизм повторного использования объектов, при котором внешний объект предоставляет интерфейсы из внутреннего объекта, как если бы они были реализованы в самом внешнем объекте. Это полезно, когда внешний объект делегирует каждый вызов к одному из своих интерфейсов во внутреннем объекте. Агрегирование доступно для удобства, чтобы избежать дополнительных затрат на реализацию во внешнем объекте в данном случае. В действительности агрегирование является специализированным вариантом [включения или делегирования](containment-delegation.md).

Статистическая обработка практически проста в реализации как вложенность, за исключением трех функций [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Перехват заключается в том, что с точки зрения клиента любая функция **IUnknown** во внешнем объекте должна влиять на внешний объект. То есть, **AddRef** и **Release** влияют на внешний объект, а **QueryInterface** — на доступ ко всем интерфейсам, доступным на внешнем объекте. Однако если внешний объект просто предоставляет интерфейс внутреннего объекта как собственный, то члены **IUnknown** этого внутреннего объекта, вызываемые через этот интерфейс, будут вести себя иначе, чем эти члены **IUnknown** в интерфейсах внешнего объекта, абсолютное нарушение правил и свойств, управляющих **IUnknown**.

Решение состоит в том, что для агрегирования требуется явная реализация [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) для внутреннего объекта и делегирование методов **IUnknown** любого другого интерфейса в методы **IUnknown** внешнего объекта.

## <a name="creating-aggregable-objects"></a>Создание объектов Аггрегабле

Создание объектов, которые могут быть агрегированными, является необязательным; Однако это просто и предоставляет значительные преимущества. Для создания объекта аггрегабле применяются следующие правила.

-   Реализация аггрегабле (или внутреннего) объекта [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для своего интерфейса [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) определяет счетчик ссылок внутреннего объекта, и эта реализация не должна делегироваться неизвестному внешнему объекту (управляющий **IUnknown**).
-   Реализация аггрегабле (или внутреннего) объекта [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для других интерфейсов должна быть делегирована управляющему [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) и не должна напрямую влиять на счетчик ссылок внутреннего объекта.
-   Внутренний [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) должен реализовывать [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) только для внутреннего объекта.
-   Объект аггрегабле не должен вызывать [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) при удержании ссылки на управляющий указатель [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .
-   При создании объекта, если запрашивается какой-либо интерфейс, отличный от [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , создание завершится ошибкой с помощью \_ интерфейса E.

В следующем фрагменте кода показана правильная реализация объекта аггрегабле с помощью метода вложенного класса реализации интерфейсов:


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



## <a name="aggregating-objects"></a>Статистическая обработка объектов

При разработке объекта аггрегабле применяются следующие правила.

-   При создании внутреннего объекта внешний объект должен явно запрашивать его [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).
-   Внешний объект должен защищать свою реализацию [**выпуска**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) от повторного входа со искусственным счетчиком ссылок вокруг кода уничтожения.
-   Внешний объект должен вызвать свой метод управления  [**выпуском**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) IUnknown, если он запрашивает указатель на любой из интерфейсов внутреннего объекта. Чтобы освободить этот указатель, внешний объект вызывает свой управляющий метод  [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) для **IUnknown**, за которым следует **выпуск** на указателе внутреннего объекта.
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   Внешний объект не должен явным образом делегировать запрос для любого неопознанного интерфейса внутреннему объекту, если это поведение не является особенно намерением внешнего объекта.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Включение и делегирование](containment-delegation.md)
</dt> </dl>

 

 