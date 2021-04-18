---
description: Реализация Имфнеткредентиалманажер
ms.assetid: 3eb2afec-195c-4d8d-8e08-7e6ec7c572f8
title: Реализация Имфнеткредентиалманажер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c026f2c12b2ff248032a56d9c48a0e0e1576c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711158"
---
# <a name="implementing-imfnetcredentialmanager"></a>Реализация Имфнеткредентиалманажер

В методе [**имфнеткредентиалманажер:: бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) выполните следующие действия.

1.  Если у вас еще нет указателя [**имфнеткредентиалкаче**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , вызовите [**мфкреатекредентиалкаче**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) , чтобы создать объект кэша учетных данных. Сохранить этот указатель.
2.  Вызовите [**имфнеткредентиалкаче:: Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential). Установите флаги в параметре *дваусентикатионфлагс* следующим образом:
    -   Если элемент **хроп** структуры [**мфнеткредентиалманажержетпарам**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) равен **NS \_ E \_ Proxy \_ ACCESSDENIED**, установите флаг **\_ \_ прокси-сервера проверки подлинности мфнет** .
    -   Если **фклеартекстпаккаже** имеет **значение true**, установите **флаг \_ проверки подлинности в \_ виде открытого \_ текста мфнет Authentication** .
    -   Если **фалловлогжедонусер** имеет **значение true**, установите **флаг \_ проверки подлинности \_ вошедшего \_ в систему \_ пользователя мфнет** .
3.  Метод [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) возвращает указатель [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) и, возможно, флаг обязательного \_ запроса. Сохраните указатель **имфнеткредентиал** .
4.  Если параметр [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) не возвращает флаг " **требуется \_ запрос** ", то все готово. Перейдите к шагу 9.
5.  В противном случае, если функция [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) Возвращает флаг **обязательного \_ запроса** , необходимо запросить у пользователя имя пользователя и пароль.
6.  Если **фклеартекстпаккаже** имеет **значение false**, зашифруйте учетные данные.
7.  Вызовите [**имфнеткредентиал:: SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) и [**Имфнеткредентиал:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) , чтобы задать имя пользователя и пароль для объекта учетных данных.
8.  При необходимости вызовите метод [**имфнеткредентиалкаче:: сетусероптионс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) , чтобы обновить объект кэша учетных данных с помощью настроек пользователя для хранения и отправки учетных данных.
9.  Вызовите обратный вызов [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , вызвав [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).

В методе [**имфнеткредентиалманажер:: енджеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) верните указатель [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) , полученный в методе [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) .

В методе [**имфнеткредентиалманажер:: сетгуд**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) передайте входные параметры непосредственно в метод [**Имфнеткредентиалкаче:: сетгуд**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) . Он уведомляет кэш учетных данных о том, были ли учетные данные приняты сервером.

Если вам нужно запросить пользователя (шаг 5) или зашифровать учетные данные (шаг 6), это следует сделать в потоке очереди работ, чтобы не блокировать конвейер Microsoft Media Foundation. Вызовите [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , а затем выполните оставшиеся действия в обратном вызове очереди работ.

> [!Note]  
> Имейте в виду, что [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) может быть вызван во время создания сетевого источника. Поэтому при создании сетевого источника путем вызова синхронного метода [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) вызывающий поток может блокироваться, пока не будут получены учетные данные. Таким образом, вместо этого рекомендуется использовать асинхронный метод [**имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .

 

## <a name="example"></a>Пример

В этом примере показан один из типов поведения, которые может предоставить диспетчер учетных данных.

Ниже приведено объявление класса, реализующего [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).


```C++
class CCredentialManager : public IMFNetCredentialManager, IMFAsyncCallback 
{
    long                    m_cRef;
    IMFNetCredentialCache   *m_pCredentialCache;

public:
    CCredentialManager () : m_cRef(1), m_pCredentialCache(NULL)
    { 
    }
    ~CCredentialManager()
    {
        SafeRelease(&m_pCredentialCache);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCredentialManager, IMFNetCredentialManager),
            QITABENT(CCredentialManager, IMFAsyncCallback),
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

    STDMETHODIMP BeginGetCredentials(
        MFNetCredentialManagerGetParam* pParam,
        IMFAsyncCallback* pCallback,
        IUnknown* pState
        );

    STDMETHODIMP EndGetCredentials(
        IMFAsyncResult* pResult, 
        IMFNetCredential** ppCred);

    STDMETHODIMP SetGood(IMFNetCredential* pCred, BOOL fGood)
    {
        if (!pCred)
        {
            return E_POINTER;
        }

        return m_pCredentialCache->SetGood(pCred, fGood);
    }


    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



Для отслеживания состояния операции [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) класс использует следующий вспомогательный объект:


```C++
// Holds state information for the GetCredentials operation, so that work can 
// be moved to a work-queue thread.

struct CredentialOp : public IUnknown
{
    long                m_cRef;
    IMFNetCredential    *m_pCredential;
    DWORD               m_dwFlags;

    CredentialOp(IMFNetCredential *pCredential) 
        : m_cRef(1), m_dwFlags(0), m_pCredential(pCredential)
    {
        m_pCredential->AddRef();
    }

    ~CredentialOp()
    {
        SafeRelease(&m_pCredential);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CredentialOp, IUnknown),
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
};
```



Метод [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) создает кэш учетных данных и получает указатель [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) . Если пользователь должен получить запрос (обозначен флагом **обязательного \_ запроса** ), метод вызывает [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , чтобы поставить новый рабочий элемент в очередь:


```C++
STDMETHODIMP CCredentialManager::BeginGetCredentials(
    MFNetCredentialManagerGetParam* pParam,
    IMFAsyncCallback* pCallback,
    IUnknown* pState
    )
{
    if (!pParam || !pCallback)
    {
        return E_POINTER;
    }

    DWORD dwAuthenticationFlags = 0;
    DWORD dwRequirementFlags = 0;

    if (pParam->hrOp == NS_E_PROXY_ACCESSDENIED)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_PROXY;
    }

    if (pParam->fAllowLoggedOnUser)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_LOGGED_ON_USER;
    }

    if (pParam->fClearTextPackage)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_CLEAR_TEXT;
    }

    IMFNetCredential *pCredential =  NULL;
    IMFAsyncResult* pResult = NULL;

    HRESULT hr = S_OK;

    if (m_pCredentialCache == NULL)
    {
        hr = MFCreateCredentialCache(&m_pCredentialCache);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    hr = m_pCredentialCache->GetCredential(
        pParam->pszUrl, 
        pParam->pszRealm, 
        dwAuthenticationFlags, 
        &pCredential, 
        &dwRequirementFlags
        );

    if (FAILED(hr))
    {
        goto done;
    }

    if( ( dwRequirementFlags & REQUIRE_PROMPT ) == 0 )
    {
        // The credential is good to use. Prompting the user is not required.
        hr = S_OK;
        goto done;
    }

    // The credential requires prompting the user. 
    CredentialOp *pOp = new (std::nothrow) CredentialOp(pCredential);

    if (pOp == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Set flags. Use these to inform the user if the credentials will
    // be sent in plaintext or saved in the credential cache.

    if (pParam->fClearTextPackage)
    {
        // Notify the user that credentials will be sent in plaintext.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT;
    }

    if(dwRequirementFlags & REQUIRE_SAVE_SELECTED )
    {
        // Credentials will be saved in the cache by default.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_SAVE;
    }

    // NOTE: The application should enable to user to deselect these two flags;
    // for example, through check boxes in the prompt dialog.


    // Now queue the work item.

    hr = MFCreateAsyncResult(pOp, pCallback, pState, &pResult);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION, this, pResult);

done:
    SafeRelease(&pResult);
    SafeRelease(&pCredential);
    SafeRelease(&pOp);
    return hr;
}
```



Поток рабочей очереди вызывает [**метод Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), который предлагает пользователю, а затем вызывает [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) для вызова указателя обратного вызова, предоставленного в [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).


```C++
STDMETHODIMP CCredentialManager::Invoke(IMFAsyncResult* pResult)
{
    IUnknown *pState = NULL;
    IMFAsyncResult *pGetCredentialsResult = NULL;
    IUnknown *pOpState = NULL;

    CredentialOp *pOp = NULL;   // not AddRef'd

    HRESULT hr = pResult->GetState(&pState);

    if (SUCCEEDED(hr))
    {
        hr = pState->QueryInterface(IID_PPV_ARGS(&pGetCredentialsResult));
    }

    if (SUCCEEDED(hr))
    {
        hr = pGetCredentialsResult->GetObject(&pOpState);
    }

    if (SUCCEEDED(hr))
    {
        pOp = static_cast<CredentialOp*>(pOpState);

        // Display a dialog for the user to enter user name and password.
        hr = PromptUserCredentials(pOp);
    }

    if (SUCCEEDED(hr) && m_pCredentialCache)
    {
        // Update with options set by the user.
        hr = m_pCredentialCache->SetUserOptions(
            pOp->m_pCredential, 
            pOp->m_dwFlags
            );
    }

    if (pGetCredentialsResult)
    {
        pGetCredentialsResult->SetStatus(hr);
        MFInvokeCallback(pGetCredentialsResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pGetCredentialsResult);
    SafeRelease(&pOpState);
    return S_OK;
}
```



Метод [**енджеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) завершает операцию, возвращая указатель [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) вызывающему объекту.


```C++
STDMETHODIMP CCredentialManager::EndGetCredentials(
    IMFAsyncResult* pResult, 
    IMFNetCredential** ppCred
    )
{
    if (!pResult || !ppCred)
    {
        return E_POINTER;
    }

    *ppCred = NULL;

    IUnknown *pUnk = NULL;

    // Check the result of the asynchronous operation.
    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        // The operation failed.
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    CredentialOp *pOp = static_cast<CredentialOp*>(pUnk);

    *ppCred = pOp->m_pCredential;
    pOp->m_pCredential = NULL;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Проверка подлинности источника сети](network-source-authentication.md)
</dt> </dl>

 

 



