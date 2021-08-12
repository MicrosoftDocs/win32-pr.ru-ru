---
title: Проверка подлинности поставщика услуг
description: Проверка подлинности поставщика услуг
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Диспетчер устройств носителя, проверка подлинности
- Диспетчер устройств, проверка подлинности
- инструкции по программированию, проверка подлинности
- поставщики услуг, проверка подлинности
- Создание поставщиков услуг, проверка подлинности
- проверка подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d6931acb4644d4222659d428be10877deb164a184c95609663a915c12b95d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586490"
---
# <a name="authenticating-the-service-provider"></a>Проверка подлинности поставщика услуг

для доступа к Windows Media диспетчер устройств поставщик услуг должен наследовать и реализовывать интерфейс [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .

Для проверки подлинности поставщик услуг выполняет следующие действия:

1.  При создании экземпляра он создает новый глобальный объект [ксекуречаннелсервер](csecurechannelserver-class.md) и устанавливает значения сертификата и ключа из своего файла ключа.
2.  Он реализует методы [**икомпонентаусентикате:: сакаус**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) и [**Икомпонентаусентикате:: сакжетпротоколс**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) , просто передавая параметры в глобальный ксекуречаннелсервер член.
3.  прежде чем обрабатывать все реализованные Windows методы диспетчер устройств мультимедиа, поставщик услуг должен проверить аутентификацию вызывающего объекта, вызвав ксекуречаннелсервер:: фисаусентикатед и отменив ошибку, если вызывающий объект не прошел проверку подлинности.

Эти шаги показаны в следующих примерах C++.

**Создание объекта Ксекуречаннелсервер**


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



**Реализация методов Икомпонентаусентикате**


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



**Проверка проверки подлинности вызывающего объекта**

В следующем примере кода показан поставщик услуг, который проверяет аутентификацию вызывающего объекта как часть его реализации интерфейса **имдсервицепровидер** .


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Создание поставщика услуг**](creating-a-service-provider.md)
</dt> </dl>

 

 




