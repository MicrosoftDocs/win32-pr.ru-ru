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
# <a name="implementing-imfnetcredentialmanager"></a><span data-ttu-id="cb170-103">Реализация Имфнеткредентиалманажер</span><span class="sxs-lookup"><span data-stu-id="cb170-103">Implementing IMFNetCredentialManager</span></span>

<span data-ttu-id="cb170-104">В методе [**имфнеткредентиалманажер:: бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cb170-104">In the [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method, do the following.</span></span>

1.  <span data-ttu-id="cb170-105">Если у вас еще нет указателя [**имфнеткредентиалкаче**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , вызовите [**мфкреатекредентиалкаче**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) , чтобы создать объект кэша учетных данных.</span><span class="sxs-lookup"><span data-stu-id="cb170-105">If you do not have an [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) pointer already, call [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) to create the credential cache object.</span></span> <span data-ttu-id="cb170-106">Сохранить этот указатель.</span><span class="sxs-lookup"><span data-stu-id="cb170-106">Store this pointer.</span></span>
2.  <span data-ttu-id="cb170-107">Вызовите [**имфнеткредентиалкаче:: Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="cb170-107">Call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span> <span data-ttu-id="cb170-108">Установите флаги в параметре *дваусентикатионфлагс* следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cb170-108">Set the flags in the *dwAuthenticationFlags* parameter as follows:</span></span>
    -   <span data-ttu-id="cb170-109">Если элемент **хроп** структуры [**мфнеткредентиалманажержетпарам**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) равен **NS \_ E \_ Proxy \_ ACCESSDENIED**, установите флаг **\_ \_ прокси-сервера проверки подлинности мфнет** .</span><span class="sxs-lookup"><span data-stu-id="cb170-109">If the **hrOp** member of the [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) structure equals **NS\_E\_PROXY\_ACCESSDENIED**, set the **MFNET\_AUTHENTICATION\_PROXY** flag.</span></span>
    -   <span data-ttu-id="cb170-110">Если **фклеартекстпаккаже** имеет **значение true**, установите **флаг \_ проверки подлинности в \_ виде открытого \_ текста мфнет Authentication** .</span><span class="sxs-lookup"><span data-stu-id="cb170-110">If **fClearTextPackage** is **TRUE**, set the **MFNET\_AUTHENTICATION\_CLEAR\_TEXT** flag.</span></span>
    -   <span data-ttu-id="cb170-111">Если **фалловлогжедонусер** имеет **значение true**, установите **флаг \_ проверки подлинности \_ вошедшего \_ в систему \_ пользователя мфнет** .</span><span class="sxs-lookup"><span data-stu-id="cb170-111">If **fAllowLoggedOnUser** is **TRUE**, set the **MFNET\_AUTHENTICATION\_LOGGED\_ON\_USER** flag.</span></span>
3.  <span data-ttu-id="cb170-112">Метод [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) возвращает указатель [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) и, возможно, флаг обязательного \_ запроса.</span><span class="sxs-lookup"><span data-stu-id="cb170-112">The [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) method returns an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer and possibly the REQUIRE\_PROMPT flag.</span></span> <span data-ttu-id="cb170-113">Сохраните указатель **имфнеткредентиал** .</span><span class="sxs-lookup"><span data-stu-id="cb170-113">Store the **IMFNetCredential** pointer.</span></span>
4.  <span data-ttu-id="cb170-114">Если параметр [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) не возвращает флаг " **требуется \_ запрос** ", то все готово.</span><span class="sxs-lookup"><span data-stu-id="cb170-114">If [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) does not return the **REQUIRE\_PROMPT** flag, you are done.</span></span> <span data-ttu-id="cb170-115">Перейдите к шагу 9.</span><span class="sxs-lookup"><span data-stu-id="cb170-115">Skip to step 9.</span></span>
5.  <span data-ttu-id="cb170-116">В противном случае, если функция [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) Возвращает флаг **обязательного \_ запроса** , необходимо запросить у пользователя имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="cb170-116">Otherwise, if [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) returns the **REQUIRE\_PROMPT** flag, you must prompt the user for his or her user name and password.</span></span>
6.  <span data-ttu-id="cb170-117">Если **фклеартекстпаккаже** имеет **значение false**, зашифруйте учетные данные.</span><span class="sxs-lookup"><span data-stu-id="cb170-117">If **fClearTextPackage** is **FALSE**, encrypt the credentials.</span></span>
7.  <span data-ttu-id="cb170-118">Вызовите [**имфнеткредентиал:: SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) и [**Имфнеткредентиал:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) , чтобы задать имя пользователя и пароль для объекта учетных данных.</span><span class="sxs-lookup"><span data-stu-id="cb170-118">Call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) to set the user's name and password on the credentials object.</span></span>
8.  <span data-ttu-id="cb170-119">При необходимости вызовите метод [**имфнеткредентиалкаче:: сетусероптионс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) , чтобы обновить объект кэша учетных данных с помощью настроек пользователя для хранения и отправки учетных данных.</span><span class="sxs-lookup"><span data-stu-id="cb170-119">Optionally, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) to update the credential cache object with the user's preferences for storing and sending credentials.</span></span>
9.  <span data-ttu-id="cb170-120">Вызовите обратный вызов [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , вызвав [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="cb170-120">Invoke the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>

<span data-ttu-id="cb170-121">В методе [**имфнеткредентиалманажер:: енджеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) верните указатель [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) , полученный в методе [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) .</span><span class="sxs-lookup"><span data-stu-id="cb170-121">In the [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method, return the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer obtained in the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span>

<span data-ttu-id="cb170-122">В методе [**имфнеткредентиалманажер:: сетгуд**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) передайте входные параметры непосредственно в метод [**Имфнеткредентиалкаче:: сетгуд**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) .</span><span class="sxs-lookup"><span data-stu-id="cb170-122">In the [**IMFNetCredentialManager::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) method, pass the input parameters directly to the [**IMFNetCredentialCache::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) method.</span></span> <span data-ttu-id="cb170-123">Он уведомляет кэш учетных данных о том, были ли учетные данные приняты сервером.</span><span class="sxs-lookup"><span data-stu-id="cb170-123">This notifies the credential cache whether the credentials were accepted by the server.</span></span>

<span data-ttu-id="cb170-124">Если вам нужно запросить пользователя (шаг 5) или зашифровать учетные данные (шаг 6), это следует сделать в потоке очереди работ, чтобы не блокировать конвейер Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cb170-124">If you need to prompt the user (step 5) or encrypt the credentials (step 6), you should do so on a work-queue thread, so that you do not block the Microsoft Media Foundation pipeline.</span></span> <span data-ttu-id="cb170-125">Вызовите [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , а затем выполните оставшиеся действия в обратном вызове очереди работ.</span><span class="sxs-lookup"><span data-stu-id="cb170-125">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) and then perform the remaining steps inside the work-queue callback.</span></span>

> [!Note]  
> <span data-ttu-id="cb170-126">Имейте в виду, что [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) может быть вызван во время создания сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="cb170-126">Be aware that [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) might be invoked while the network source is being created.</span></span> <span data-ttu-id="cb170-127">Поэтому при создании сетевого источника путем вызова синхронного метода [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) вызывающий поток может блокироваться, пока не будут получены учетные данные.</span><span class="sxs-lookup"><span data-stu-id="cb170-127">Therefore, if you create the network source by calling the synchronous [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method, your calling thread might block while the credentials are acquired.</span></span> <span data-ttu-id="cb170-128">Таким образом, вместо этого рекомендуется использовать асинхронный метод [**имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="cb170-128">Therefore, it is recommended to use the asynchronous [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method instead.</span></span>

 

## <a name="example"></a><span data-ttu-id="cb170-129">Пример</span><span class="sxs-lookup"><span data-stu-id="cb170-129">Example</span></span>

<span data-ttu-id="cb170-130">В этом примере показан один из типов поведения, которые может предоставить диспетчер учетных данных.</span><span class="sxs-lookup"><span data-stu-id="cb170-130">This example shows one type of behavior that a credential manager could provide.</span></span>

<span data-ttu-id="cb170-131">Ниже приведено объявление класса, реализующего [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span><span class="sxs-lookup"><span data-stu-id="cb170-131">Here is a declaration of the class that implements [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span></span>


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



<span data-ttu-id="cb170-132">Для отслеживания состояния операции [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) класс использует следующий вспомогательный объект:</span><span class="sxs-lookup"><span data-stu-id="cb170-132">To track the state of the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) operation, the class uses the following helper object:</span></span>


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



<span data-ttu-id="cb170-133">Метод [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) создает кэш учетных данных и получает указатель [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="cb170-133">The [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method creates the credential cache and gets an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer.</span></span> <span data-ttu-id="cb170-134">Если пользователь должен получить запрос (обозначен флагом **обязательного \_ запроса** ), метод вызывает [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , чтобы поставить новый рабочий элемент в очередь:</span><span class="sxs-lookup"><span data-stu-id="cb170-134">If the user must be prompted (indicated by the **REQUIRE\_PROMPT** flag), the method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item:</span></span>


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



<span data-ttu-id="cb170-135">Поток рабочей очереди вызывает [**метод Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), который предлагает пользователю, а затем вызывает [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) для вызова указателя обратного вызова, предоставленного в [**бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span><span class="sxs-lookup"><span data-stu-id="cb170-135">The work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), which prompts the user and then calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the callback pointer that was provided in [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span></span>


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



<span data-ttu-id="cb170-136">Метод [**енджеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) завершает операцию, возвращая указатель [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="cb170-136">The [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method completes the operation by returning the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer to the caller.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cb170-137">См. также</span><span class="sxs-lookup"><span data-stu-id="cb170-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb170-138">Проверка подлинности источника сети</span><span class="sxs-lookup"><span data-stu-id="cb170-138">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



