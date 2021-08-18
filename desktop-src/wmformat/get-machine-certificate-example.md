---
title: Пример получения сертификата компьютера
description: Пример получения сертификата компьютера
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows Пакет SDK для формата мультимедиа, сертификаты компьютеров
- Windows Пакет SDK для формата мультимедиа, сертификаты
- Windows Пакет SDK для формата мультимедиа, пример кода
- Windows Пакет SDK для формата мультимедиа, примеры кода
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
ms.openlocfilehash: 855479e90095f204a3ba7abafadcb4a31bbcaeaf7c592221ab0d5906cb1d8b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964013"
---
# <a name="get-machine-certificate-example"></a>Пример получения сертификата компьютера

В следующем примере показано, как получить коллекцию сертификатов компьютера:


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Примеры импорта DRM**](drm-import-examples.md)
</dt> </dl>

 

 




