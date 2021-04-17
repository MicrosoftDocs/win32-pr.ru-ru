---
title: Проверка подлинности приложения
description: Проверка подлинности приложения
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Диспетчер устройств Windows Media, проверка подлинности
- Диспетчер устройств, проверка подлинности
- инструкции по программированию, проверка подлинности
- Классические приложения, проверка подлинности
- Создание приложений диспетчер устройств Windows Media, проверка подлинности
- проверка подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7779cdbb874278e6b62517cc2c1983dd2ce8fa1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691529"
---
# <a name="authenticating-the-application"></a>Проверка подлинности приложения

Первым шагом, который должен выполнить приложение, является проверка подлинности. Проверка подлинности проверяет удостоверение приложения на диспетчер устройств Windows Media. После проверки подлинности приложения можно вызвать **QueryInterface** , чтобы получить корневой интерфейс [**ивмдевицеманажер**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) , который может запрашивать другие необходимые интерфейсы, которые можно запрашивать для всех других интерфейсов. Проверка подлинности должна выполняться только один раз при запуске.

Чтобы проверить подлинность приложения, выполните следующие действия.

1.  Создайте объект **медиадевмгр** (идентификатор класса медиадевмгр) и запросите интерфейс [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .
2.  Создайте объект [ксекуречаннелклиент](csecurechannelclient-class.md) для проверки подлинности.
3.  Передайте ключ приложения и сертификат передачи в объект безопасного канала. Для получения базовой функциональности из функций пакета SDK можно использовать фиктивный ключ или сертификат, показанный в следующем примере кода. Однако для получения полной функциональности (важно для передачи файлов на устройство и обратно) необходимо запросить ключ и сертификат от Майкрософт, как описано в разделе [средства для разработки](tools-for-development.md).
4.  Передайте интерфейс **икомпонентаусентикате** , созданный на шаге 1, в объект безопасного канала.
5.  Вызовите [**ксекуречаннелклиент:: Authenticate**](/previous-versions/ms983906(v=msdn.10)) , чтобы проверить подлинность приложения.
6.  Запросите **икомпонентаусентикате** для интерфейса **ивмдевицеманажер** .

Эти шаги показаны в следующем коде C++.


```C++
HRESULT CWMDMController::Authenticate()
{
    // Use a dummy key/certificate pair to allow basic functionality.
    // An authentic keypair is required for full SDK functionality.
    BYTE abPVK[] = {0x00};
    BYTE abCert[] = {0x00};
    HRESULT hr;
    CComPtr<IComponentAuthenticate> pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&pAuth);

    if (FAILED(hr)) return hr;

    // Create the secure channel client class needed to authenticate the application.
    // We'll use a global member variable to hold the secure channel client
    // in case we need to handle encryption, decryption, or MAC verification
    // during this session.
    m_pSAC = new CSecureChannelClient;
    if (m_pSAC == NULL) return E_FAIL;

    // Send the application's transfer certificate and the associated 
    // private key to the secure channel client.
    hr = m_pSAC->SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (FAILED(hr)) return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and authenticate the application with the V1 protocol.
    // (This is the only protocol currently supported.)
    m_pSAC->SetInterface(pAuth);
    hr = m_pSAC->Authenticate(SAC_PROTOCOL_V1);
    if (FAILED(hr)) return hr;

    // Authentication succeeded, so we can use WMDM.
    // Query for the root WMDM interface.
    hr = pAuth->QueryInterface( __uuidof(IWMDeviceManager), (void**)&m_IWMDMDeviceMgr);

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание приложения диспетчер устройств Windows Media**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 