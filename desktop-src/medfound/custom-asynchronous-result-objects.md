---
description: Пользовательские объекты асинхронных результатов
ms.assetid: 78cef367-b007-46d5-bb7f-2b3f7eed9926
title: Пользовательские объекты асинхронных результатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5a0109b47255bc14fcccafbbb09c419848b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262808"
---
# <a name="custom-asynchronous-result-objects"></a>Пользовательские объекты асинхронных результатов

В этом разделе описывается, как реализовать интерфейс [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .

В редких случаях необходимо написать пользовательскую реализацию интерфейса [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Почти во всех случаях достаточно стандартной реализации Media Foundation. (Эта реализация возвращается функцией [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) .) Однако при написании пользовательской реализации необходимо учитывать некоторые моменты.

Во первых, ваша реализация должна наследовать структуру [**мфасинкресулт**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) . В Media Foundation рабочих очередях эта структура используется внутренним образом для отправки операции. Инициализируйте все члены структуры как ноль, за исключением элемента **пкаллбакк** , который содержит указатель на интерфейс обратного вызова вызывающего объекта.

Во вторых, объект должен вызвать [**мфлоккплатформ**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) в своем конструкторе, чтобы заблокировать Media Foundationную платформу. Вызовите [**мфунлоккплатформ**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) , чтобы разблокировать платформу. Эти функции помогают предотвратить завершение работы платформы перед уничтожением объекта. Дополнительные сведения см. в статье [рабочие очереди](work-queues.md).

В следующем коде показана базовая реализация интерфейса [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Как показано ниже, этот код не предоставляет дополнительных функций, Кроме стандартной реализации Media Foundation.


```C++
///////////////////////////////////////////////////////////////////////////////
//  CMyAsyncResult
//
//  Custom implementation of IMFAsyncResult. All implementations of this 
//  interface must inherit the MFASYNCRESULT structure.
// 
///////////////////////////////////////////////////////////////////////////////

class CMyAsyncResult : public MFASYNCRESULT
{
protected:
    LONG        m_cRef;             // Reference count.
    BOOL        m_bLockPlatform;    // Locked the Media Foundation platform?
    IUnknown*   m_pState;           // Caller's state object. 
    IUnknown*   m_pObject;  // Optional object. See IMFAsyncResult::GetObject.

    // Constructor. 
    CMyAsyncResult(IMFAsyncCallback *pCallback, IUnknown *pState, HRESULT *phr) :
        m_cRef(1),
        m_bLockPlatform(FALSE),
        m_pObject(NULL),
        m_pState(pState)
    {
        *phr = MFLockPlatform();

        m_bLockPlatform = TRUE;

        // Initialize the MFASYNCRESULT members.
        ZeroMemory(&this->overlapped, sizeof(OVERLAPPED));
        hrStatusResult = S_OK;
        dwBytesTransferred = 0;
        hEvent = NULL;

        this->pCallback = pCallback;
        if (pCallback)
        {
            this->pCallback->AddRef();
        }

        if (m_pState)
        {
            m_pState->AddRef();
        }
    }

    virtual ~CMyAsyncResult()
    {
        SafeRelease(&pCallback);
        SafeRelease(&m_pState);
        SafeRelease(&m_pObject);

        if (m_bLockPlatform)
        {
            MFUnlockPlatform();
        }
    }

public:
    // Static method to create an instance of this object.
    static HRESULT CreateInstance(
        IMFAsyncCallback *pCallback,    // Callback to invoke.
        IUnknown *pState,               // Optional state object.
        CMyAsyncResult **ppResult       // Receives a pointer to the object.
        )
    {
        HRESULT hr = S_OK;

        *ppResult = NULL;

        CMyAsyncResult *pResult = 
            new (std::nothrow) CMyAsyncResult(pCallback, pState, &hr);

        if (pResult == NULL)
        {
            return E_OUTOFMEMORY;
        }
        if (FAILED(hr))
        {
            delete pResult;
            return hr;
        }

        // If the callback is NULL, create an event that will be signaled.
        if (pCallback == NULL)
        {
            pResult->hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
            if (pResult->hEvent == NULL)
            {
                hr = HRESULT_FROM_WIN32(GetLastError());
            }
        }

        if (SUCCEEDED(hr))
        {
            *ppResult = pResult;  // Return the pointer to the caller.
        }
        else
        {
            pResult->Release();
        }
        return hr;
    }

    // SetObject: Sets the optional result object. 
    // (This method is not part of the interface.)
    HRESULT SetObject(IUnknown *pObject)
    {
        SafeRelease(&m_pObject);
        m_pObject = pObject;
        if (pObject)
        {
            m_pObject->AddRef();
        }
        return S_OK;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CMyAsyncResult, IMFAsyncResult),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
    
    // IMFAsyncResult methods.
    STDMETHODIMP GetState(IUnknown** ppunkState)
    {
        if (ppunkState == NULL)
        {
            return E_POINTER;
        }

        *ppunkState = m_pState;
        if (m_pState)
        {
            (*ppunkState)->AddRef();
        }

        return S_OK;
    }

    STDMETHODIMP GetStatus( void)
    {
        return hrStatusResult;
    }

    STDMETHODIMP STDMETHODCALLTYPE SetStatus(HRESULT hrStatus)
    {
        hrStatusResult = hrStatus;
        return S_OK;
    }

    STDMETHODIMP GetObject(IUnknown **ppObject)
    {
        if (ppObject == NULL)
        {
            return E_POINTER;
        }

        *ppObject = m_pObject;
        if (m_pObject)
        {
            (*ppObject)->AddRef();
        }
        return S_OK;
    }

    IUnknown* STDMETHODCALLTYPE GetStateNoAddRef()
    {
        return m_pState;  // Warning! Can be NULL. 
    }
};
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Рабочие очереди](work-queues.md)
</dt> <dt>

[Асинхронные методы обратного вызова](asynchronous-callback-methods.md)
</dt> </dl>

 

 



