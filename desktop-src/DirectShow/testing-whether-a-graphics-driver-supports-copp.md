---
description: Проверка того, поддерживает ли графический драйвер Копп
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Проверка того, поддерживает ли графический драйвер Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22280f880ba01a8e51acda74a2a46dff595d5569f885ce1da3a3631bacd8db06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651834"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>Проверка того, поддерживает ли графический драйвер Копп

Протокол Копп позволяет приложению защищать содержимое видео по мере его передачи с видеоадаптера на устройство дисплея. Если графический драйвер поддерживает Копп, драйвер содержит цепочку сертификатов, подписанную корпорацией Майкрософт, которая проверяет подлинность драйвера. Приложения воспроизведения, использующие Копп для принудительной защиты содержимого, должны проверить цепочку сертификатов, чтобы убедиться, что драйвер не был изменен.

Однако может потребоваться проверить, поддерживает ли графический драйвер Копп, не проверяя сертификат. Например, если поставщик цифрового мультимедиа выдает лицензию на управление цифровыми правами (DRM), может потребоваться проверить, есть ли у пользователя драйвер графики с поддержкой Копп. Поставщику не требуется принудительно применять Копп на момент, когда он выдает лицензию; необходимо только проверить, поддерживает ли драйвер Копп.

В следующем коде показано, как проверить, поддерживает ли драйвер Копп. Приложение должно передать имя файла видео, который будет использоваться для проверки драйвера. это необходимо, поскольку фильтр модуля подготовки видео для микширования в Microsoft® DirectShow® не инициализирует сеанс копп, пока фильтр не будет подключен. Эта функция может быть включена в клиентское приложение, чтобы проверить, поддерживает ли драйвер запуск Копп.

> [!Note]  
> Если компьютер пользователя имеет две графические карты, эта функция проверяет наличие основного графического адаптера, но не дополнительного графического адаптера.

 


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование протокола сертифицированной выходной защиты](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



