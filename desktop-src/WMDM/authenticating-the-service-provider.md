---
title: Проверка подлинности поставщика услуг
description: Проверка подлинности поставщика услуг
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Диспетчер устройств Windows Media, проверка подлинности
- Диспетчер устройств, проверка подлинности
- инструкции по программированию, проверка подлинности
- поставщики услуг, проверка подлинности
- Создание поставщиков услуг, проверка подлинности
- проверка подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271bf5594e4adaede01bb8e3795780f8f5c5177a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691324"
---
# <a name="authenticating-the-service-provider"></a><span data-ttu-id="bed1b-109">Проверка подлинности поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="bed1b-109">Authenticating the Service Provider</span></span>

<span data-ttu-id="bed1b-110">Чтобы быть доступным из диспетчер устройств Windows Media, поставщик услуг должен наследовать и реализовывать интерфейс [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="bed1b-110">To be accessible from Windows Media Device Manager, a service provider must inherit and implement the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>

<span data-ttu-id="bed1b-111">Для проверки подлинности поставщик услуг выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bed1b-111">To authenticate itself, a service provider performs the following steps:</span></span>

1.  <span data-ttu-id="bed1b-112">При создании экземпляра он создает новый глобальный объект [ксекуречаннелсервер](csecurechannelserver-class.md) и устанавливает значения сертификата и ключа из своего файла ключа.</span><span class="sxs-lookup"><span data-stu-id="bed1b-112">On instantiation, it creates a new global [CSecureChannelServer](csecurechannelserver-class.md) object and sets the certificate and key values from its key file.</span></span>
2.  <span data-ttu-id="bed1b-113">Он реализует методы [**икомпонентаусентикате:: сакаус**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) и [**Икомпонентаусентикате:: сакжетпротоколс**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) , просто передавая параметры в глобальный ксекуречаннелсервер член.</span><span class="sxs-lookup"><span data-stu-id="bed1b-113">It implements the [**IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) and [**IComponentAuthenticate::SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) methods by simply passing the parameters into its global CSecureChannelServer member.</span></span>
3.  <span data-ttu-id="bed1b-114">Прежде чем обрабатывать все реализованные методы диспетчер устройств Windows Media, поставщик услуг должен проверить подлинность вызывающего объекта, вызвав Ксекуречаннелсервер:: Фисаусентикатед и отменив ошибку, если вызывающий объект не прошел проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="bed1b-114">Before handling any implemented Windows Media Device Manager methods, the service provider must verify the caller's authentication by calling CSecureChannelServer::fIsAuthenticated, and failing if the caller is not authenticated.</span></span>

<span data-ttu-id="bed1b-115">Эти шаги показаны в следующих примерах C++.</span><span class="sxs-lookup"><span data-stu-id="bed1b-115">These steps are shown in the following C++ examples.</span></span>

<span data-ttu-id="bed1b-116">**Создание объекта Ксекуречаннелсервер**</span><span class="sxs-lookup"><span data-stu-id="bed1b-116">**Creating the CSecureChannelServer object**</span></span>


```C++
CMyServiceProvider::CMyServiceProvider()
{
    HRESULT hr = S_OK;

    // Create the persistent SAC object.
    g_pSAC = new CSecureChannelServer();

    // Set the SAC certificate.
    if (g_pSAC)
    {
        hr = g_pSAC->SetCertificate(
             SAC_CERT_V1,
            (BYTE*)abCert, sizeof(abCert), // SP's certificate.
            (BYTE*)abPVK, sizeof(abPVK)    // SP's key.
        );
    }   
    if (FAILED(hr)) return hr;

    //... Perform other class initialization here ...

    return hr;
}
```



<span data-ttu-id="bed1b-117">**Реализация методов Икомпонентаусентикате**</span><span class="sxs-lookup"><span data-stu-id="bed1b-117">**Implementing the IComponentAuthenticate methods**</span></span>


```C++
STDMETHODIMP CMDServiceProvider::SACAuth(
    DWORD   dwProtocolID,
    DWORD   dwPass,
    BYTE   *pbDataIn,
    DWORD   dwDataInLen,
    BYTE  **ppbDataOut,
    DWORD  *pdwDataOutLen)
{
    HRESULT hr = S_OK;

    // Verify that the global CSecureChannelServer member still exists.
    if (!g_pSAC)
        return E_FAIL;

    // Just pass the call to the global SAC member.
    hr = g_pSAC->SACAuth(
        dwProtocolID,
        dwPass,
        pbDataIn, dwDataInLen,
        ppbDataOut, pdwDataOutLen
    );
    return hr;
}

STDMETHODIMP CMDServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    if (!g_pSAC)
        return hr;

    hr = g_pSAC->SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );
    return hr;
}
```



<span data-ttu-id="bed1b-118">**Проверка проверки подлинности вызывающего объекта**</span><span class="sxs-lookup"><span data-stu-id="bed1b-118">**Verifying the caller's authentication**</span></span>

<span data-ttu-id="bed1b-119">В следующем примере кода показан поставщик услуг, который проверяет аутентификацию вызывающего объекта как часть его реализации интерфейса **имдсервицепровидер** .</span><span class="sxs-lookup"><span data-stu-id="bed1b-119">The following code example shows a service provider checking the caller's authentication as part of its implementation of the **IMDServiceProvider** interface.</span></span>


```C++
STDMETHODIMP CMyServiceProvider::GetDeviceCount(DWORD * pdwCount)
{
    HRESULT hr = S_OK;
    if (!g_pSAC)
        return E_FAIL;

    if (!(g_pSAC->fIsAuthenticated()))
        return WMDM_E_NOTCERTIFIED;

    *pdwCount = m_DeviceCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="bed1b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="bed1b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bed1b-121">**Создание поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="bed1b-121">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




