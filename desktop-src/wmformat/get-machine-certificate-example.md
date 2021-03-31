---
title: Пример получения сертификата компьютера
description: Пример получения сертификата компьютера
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows Media Format SDK, сертификаты компьютеров
- Windows Media Format SDK, сертификаты
- Windows Media Format SDK, пример кода
- Windows Media Format SDK, примеры кода
- Управление цифровыми правами (DRM), сертификаты компьютеров
- DRM (Управление цифровыми правами), сертификаты компьютеров
- Управление цифровыми правами (DRM), сертификаты
- DRM (Управление цифровыми правами), сертификаты
- Управление цифровыми правами (DRM), пример кода
- DRM (Управление цифровыми правами), пример кода
- Управление цифровыми правами (DRM), примеры кода
- DRM (Управление цифровыми правами), примеры кода
- Расширенные API клиента DRM, сертификаты компьютеров
- Расширенные API клиента, сертификаты компьютеров
- Расширенные API клиента DRM, сертификаты
- Расширенные API клиента, сертификаты
- Расширенные API клиента DRM, пример кода
- Расширенные API клиента, пример кода
- Расширенные API клиента DRM, примеры кода
- Расширенные API клиента, примеры кода
- сертификаты, примеры кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68a8ecbaf3e3c0ba8001a7a2094ab2b4a7e09a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411263"
---
# <a name="get-machine-certificate-example"></a><span data-ttu-id="1e7e0-124">Пример получения сертификата компьютера</span><span class="sxs-lookup"><span data-stu-id="1e7e0-124">Get Machine Certificate Example</span></span>

<span data-ttu-id="1e7e0-125">В следующем примере показано, как получить коллекцию сертификатов компьютера:</span><span class="sxs-lookup"><span data-stu-id="1e7e0-125">The following example shows how to retrieve the machine certificate collection:</span></span>


```C++
HRESULT GetMachineCert( BYTE **ppbCert, DWORD *pcbCert )
{
    HRESULT hr = S_OK;
    IWMDRMProvider *pProvider = NULL;
    IWMDRMSecurity *pSecurity = NULL;
    BYTE rgbVersion[4];

    // Create a provider object.
    hr = WMDRMCreateProvider( &pProvider );
    if( FAILED( hr ) ) goto EXIT;

    // Create a security object from a provider object.
    hr = pProvider->CreateObject( IID_IWMDRMSecurity, (void**) &pSecurity );
    if( FAILED( hr ) ) goto EXIT;

    // Query the security to get the machine certificate.
    hr = pSecurity->GetMachineCertificate( WMDRM_CERTIFICATE_TYPE_V2,
        rgbVersion, ppbCert, pcbCert );

    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pSecurity );
    SAFE_RELEASE( pProvider );

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1e7e0-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1e7e0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e7e0-127">**Примеры импорта DRM**</span><span class="sxs-lookup"><span data-stu-id="1e7e0-127">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




