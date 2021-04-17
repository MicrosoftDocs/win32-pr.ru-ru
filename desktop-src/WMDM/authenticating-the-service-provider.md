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
# <a name="authenticating-the-service-provider"></a>Проверка подлинности поставщика услуг

Чтобы быть доступным из диспетчер устройств Windows Media, поставщик услуг должен наследовать и реализовывать интерфейс [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .

Для проверки подлинности поставщик услуг выполняет следующие действия:

1.  При создании экземпляра он создает новый глобальный объект [ксекуречаннелсервер](csecurechannelserver-class.md) и устанавливает значения сертификата и ключа из своего файла ключа.
2.  Он реализует методы [**икомпонентаусентикате:: сакаус**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) и [**Икомпонентаусентикате:: сакжетпротоколс**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) , просто передавая параметры в глобальный ксекуречаннелсервер член.
3.  Прежде чем обрабатывать все реализованные методы диспетчер устройств Windows Media, поставщик услуг должен проверить подлинность вызывающего объекта, вызвав Ксекуречаннелсервер:: Фисаусентикатед и отменив ошибку, если вызывающий объект не прошел проверку подлинности.

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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание поставщика услуг**](creating-a-service-provider.md)
</dt> </dl>

 

 




