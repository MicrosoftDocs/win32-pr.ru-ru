---
description: Проверка того, поддерживает ли графический драйвер Копп
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Проверка того, поддерживает ли графический драйвер Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f98a5bfc3f577d1acb45969ec5d10503ae87b27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684115"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a><span data-ttu-id="4d1db-103">Проверка того, поддерживает ли графический драйвер Копп</span><span class="sxs-lookup"><span data-stu-id="4d1db-103">Testing Whether a Graphics Driver Supports COPP</span></span>

<span data-ttu-id="4d1db-104">Протокол Копп позволяет приложению защищать содержимое видео по мере его передачи с видеоадаптера на устройство дисплея.</span><span class="sxs-lookup"><span data-stu-id="4d1db-104">Certified Output Protection Protocol (COPP) enables an application to protect video content as it travels from the video card to the display device.</span></span> <span data-ttu-id="4d1db-105">Если графический драйвер поддерживает Копп, драйвер содержит цепочку сертификатов, подписанную корпорацией Майкрософт, которая проверяет подлинность драйвера.</span><span class="sxs-lookup"><span data-stu-id="4d1db-105">If a graphics driver supports COPP, the driver holds a certificate chain, signed by Microsoft, authenticating the driver.</span></span> <span data-ttu-id="4d1db-106">Приложения воспроизведения, использующие Копп для принудительной защиты содержимого, должны проверить цепочку сертификатов, чтобы убедиться, что драйвер не был изменен.</span><span class="sxs-lookup"><span data-stu-id="4d1db-106">Playback applications that use COPP to enforce content protection must validate the certificate chain to ensure that the driver has not been tampered with.</span></span>

<span data-ttu-id="4d1db-107">Однако может потребоваться проверить, поддерживает ли графический драйвер Копп, не проверяя сертификат.</span><span class="sxs-lookup"><span data-stu-id="4d1db-107">However, you might want to check whether a graphics driver supports COPP, without validating the certificate.</span></span> <span data-ttu-id="4d1db-108">Например, если поставщик цифрового мультимедиа выдает лицензию на управление цифровыми правами (DRM), может потребоваться проверить, есть ли у пользователя драйвер графики с поддержкой Копп.</span><span class="sxs-lookup"><span data-stu-id="4d1db-108">For example, when a digital media provider issues a digital rights management (DRM) license, it might want to check whether the user has a COPP-enabled graphics driver.</span></span> <span data-ttu-id="4d1db-109">Поставщику не требуется принудительно применять Копп на момент, когда он выдает лицензию; необходимо только проверить, поддерживает ли драйвер Копп.</span><span class="sxs-lookup"><span data-stu-id="4d1db-109">The provider does not need to enforce COPP at the time it issues the license; it only needs to test whether the driver supports COPP.</span></span>

<span data-ttu-id="4d1db-110">В следующем коде показано, как проверить, поддерживает ли драйвер Копп.</span><span class="sxs-lookup"><span data-stu-id="4d1db-110">The following code shows how to test whether a driver supports COPP.</span></span> <span data-ttu-id="4d1db-111">Приложение должно передать имя файла видео, который будет использоваться для проверки драйвера.</span><span class="sxs-lookup"><span data-stu-id="4d1db-111">The application must pass in the name of a video file that will be used to test the driver.</span></span> <span data-ttu-id="4d1db-112">Это необходимо, поскольку фильтр модуля подготовки видео для микширования в Microsoft® DirectShow® не Инициализирует сеанс Копп, пока фильтр не будет подключен.</span><span class="sxs-lookup"><span data-stu-id="4d1db-112">This is required because the Video Mixing Renderer filter in Microsoft® DirectShow® does not initialize a COPP session until the filter is connected.</span></span> <span data-ttu-id="4d1db-113">Эта функция может быть включена в клиентское приложение, чтобы проверить, поддерживает ли драйвер запуск Копп.</span><span class="sxs-lookup"><span data-stu-id="4d1db-113">This function can be included in a client application to check if the driver is capable of running COPP.</span></span>

> [!Note]  
> <span data-ttu-id="4d1db-114">Если компьютер пользователя имеет две графические карты, эта функция проверяет наличие основного графического адаптера, но не дополнительного графического адаптера.</span><span class="sxs-lookup"><span data-stu-id="4d1db-114">If the user's computer has two graphics cards, this function tests the driver for the primary graphics card, but not the secondary graphics card.</span></span>

 


```C++
#include <dshow.h>
// Link to strmiids.lib

#define SAFE_RELEASE(p) if (NULL != (p)) { (p)->Release(); (p) = NULL; }
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }

enum COPPSupport 
{
    SUPPORTS_COPP,
    DOES_NOT_SUPPORT_COPP,
    CANNOT_DETERMINE_COPP_SUPPORT
};

//------------------------------------------------------------------------
// Name:        IsDriverCoppEnabled
// Description: Test whether the user's graphics driver supports
//              COPP.
// wszTestFile: Name of a video file to use for testing.
//
// If this method returns the value SUPPORTS_COPP, it does *not* guarantee 
// that the driver is a valid COPP-enabled driver. If you want to use COPP 
// to enforce video output protection, the application *must* validate 
// the certificate returned by the KeyExchange method. 
// 
// The purpose of this function is only to test whether the driver 
// claims to support COPP. 
//------------------------------------------------------------------------

COPPSupport IsDriverCoppEnabled(const WCHAR *wszTestFile)
{
    COPPSupport SupportResult = CANNOT_DETERMINE_COPP_SUPPORT; 

    IGraphBuilder *pGB = NULL;
    IBaseFilter *pRenderer = NULL;
    IAMCertifiedOutputProtection  *pCOPPDevice = NULL;
    BYTE *pbCertificate = NULL;
    GUID  RandomValue = GUID_NULL;
    ULONG cbCertificateLength = NULL;
    
    HRESULT hr = S_OK;

    CHECK_HR(hr = CoInitializeEx(NULL, COINIT_MULTITHREADED));
   
    // Create the Filter Graph Manager.
    CHECK_HR(hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void**)&pGB));

    // Create the VMR-9. 
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9,
        NULL, CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
        (void**)&pRenderer
        ));

    if (FAILED(hr))
    {
        // Try the VMR-7 instead.
        CHECK_HR(hr = CoCreateInstance(CLSID_VideoMixingRenderer,
                NULL, CLSCTX_INPROC, IID_IBaseFilter, 
                (void**)&pRenderer
                ));
    }

    // Add the VMR to the filter graph.
    CHECK_HR(hr = pGB->AddFilter(pRenderer, L"Video Renderer"));

    // Build a default playback graph.
    CHECK_HR(hr = pGB->RenderFile(wszTestFile, NULL));

    // Query for IAMCertifiedOutputProtection.
    CHECK_HR(hr = pRenderer->QueryInterface(IID_IAMCertifiedOutputProtection,
            (void**)&pCOPPDevice));

    // Get the driver's COPP certificate.
    hr = pCOPPDevice->KeyExchange(&RandomValue, &pbCertificate,
        &cbCertificateLength);

    if (SUCCEEDED(hr))
    {
        SupportResult = SUPPORTS_COPP;
    }
    else
    {
        SupportResult = DOES_NOT_SUPPORT_COPP;
    }

done:
    // Clean up.
    CoTaskMemFree(pbCertificate);
    SAFE_RELEASE(pCOPPDevice);
    SAFE_RELEASE(pRenderer);
    SAFE_RELEASE(pGB);
    CoUninitialize();

    return SupportResult;
} 

```



## <a name="related-topics"></a><span data-ttu-id="4d1db-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4d1db-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d1db-116">Использование протокола сертифицированной выходной защиты</span><span class="sxs-lookup"><span data-stu-id="4d1db-116">Using Certified Output Protection Protocol</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



