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
# <a name="authenticating-the-application"></a><span data-ttu-id="f424d-109">Проверка подлинности приложения</span><span class="sxs-lookup"><span data-stu-id="f424d-109">Authenticating the Application</span></span>

<span data-ttu-id="f424d-110">Первым шагом, который должен выполнить приложение, является проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="f424d-110">The first step your application must perform is authentication.</span></span> <span data-ttu-id="f424d-111">Проверка подлинности проверяет удостоверение приложения на диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f424d-111">Authentication verifies the application's identity to Windows Media Device Manager.</span></span> <span data-ttu-id="f424d-112">После проверки подлинности приложения можно вызвать **QueryInterface** , чтобы получить корневой интерфейс [**ивмдевицеманажер**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) , который может запрашивать другие необходимые интерфейсы, которые можно запрашивать для всех других интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f424d-112">Once you authenticate your application, you can call **QueryInterface** to get the root [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) interface, which can be queried for other required interfaces, which can themselves be queried for all other interfaces.</span></span> <span data-ttu-id="f424d-113">Проверка подлинности должна выполняться только один раз при запуске.</span><span class="sxs-lookup"><span data-stu-id="f424d-113">Authentication need only take place once, on startup.</span></span>

<span data-ttu-id="f424d-114">Чтобы проверить подлинность приложения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f424d-114">To authenticate your application, perform these steps:</span></span>

1.  <span data-ttu-id="f424d-115">Создайте объект **медиадевмгр** (идентификатор класса медиадевмгр) и запросите интерфейс [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="f424d-115">CoCreate the **MediaDevMgr** object (class ID MediaDevMgr), and request an [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>
2.  <span data-ttu-id="f424d-116">Создайте объект [ксекуречаннелклиент](csecurechannelclient-class.md) для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f424d-116">Create a [CSecureChannelClient](csecurechannelclient-class.md) object to handle the authentication.</span></span>
3.  <span data-ttu-id="f424d-117">Передайте ключ приложения и сертификат передачи в объект безопасного канала.</span><span class="sxs-lookup"><span data-stu-id="f424d-117">Pass your application key and transfer certificate to the secure channel object.</span></span> <span data-ttu-id="f424d-118">Для получения базовой функциональности из функций пакета SDK можно использовать фиктивный ключ или сертификат, показанный в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f424d-118">You can use the dummy key/certificate shown in the following example code to get basic functionality from SDK functions.</span></span> <span data-ttu-id="f424d-119">Однако для получения полной функциональности (важно для передачи файлов на устройство и обратно) необходимо запросить ключ и сертификат от Майкрософт, как описано в разделе [средства для разработки](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="f424d-119">However, to get full functionality (important for passing files to and from the device), you must request a key and certificate from Microsoft as described in [Tools for Development](tools-for-development.md).</span></span>
4.  <span data-ttu-id="f424d-120">Передайте интерфейс **икомпонентаусентикате** , созданный на шаге 1, в объект безопасного канала.</span><span class="sxs-lookup"><span data-stu-id="f424d-120">Pass the **IComponentAuthenticate** interface you created in step 1 to the secure channel object.</span></span>
5.  <span data-ttu-id="f424d-121">Вызовите [**ксекуречаннелклиент:: Authenticate**](/previous-versions/ms983906(v=msdn.10)) , чтобы проверить подлинность приложения.</span><span class="sxs-lookup"><span data-stu-id="f424d-121">Call [**CSecureChannelClient::Authenticate**](/previous-versions/ms983906(v=msdn.10)) to authenticate your application.</span></span>
6.  <span data-ttu-id="f424d-122">Запросите **икомпонентаусентикате** для интерфейса **ивмдевицеманажер** .</span><span class="sxs-lookup"><span data-stu-id="f424d-122">Query **IComponentAuthenticate** for the **IWMDeviceManager** interface.</span></span>

<span data-ttu-id="f424d-123">Эти шаги показаны в следующем коде C++.</span><span class="sxs-lookup"><span data-stu-id="f424d-123">These steps are shown in the following C++ code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f424d-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f424d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f424d-125">**Создание приложения диспетчер устройств Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f424d-125">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 