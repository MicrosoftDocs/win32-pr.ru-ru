---
title: Пример шифрования мультимедиа
description: Пример шифрования мультимедиа
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- Windows Media Format SDK, пример шифрования мультимедиа
- Windows Media Format SDK, пример кода
- Windows Media Format SDK, примеры кода
- Управление цифровыми правами (DRM), пример шифрования мультимедиа
- DRM (Управление цифровыми правами), пример шифрования мультимедиа
- Управление цифровыми правами (DRM), пример кода
- DRM (Управление цифровыми правами), пример кода
- Управление цифровыми правами (DRM), примеры кода
- DRM (Управление цифровыми правами), примеры кода
- Расширенные API клиента DRM, пример шифрования мультимедиа
- Расширенные API клиента, пример шифрования мультимедиа
- Расширенные API клиента DRM, пример кода
- Расширенные API клиента, пример кода
- Расширенные API клиента DRM, примеры кода
- Расширенные API клиента, примеры кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a669ab957aa7510cdd57daca798ec3e3ac3bf73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068570"
---
# <a name="media-sample-encryption-example"></a><span data-ttu-id="28051-118">Пример шифрования мультимедиа</span><span class="sxs-lookup"><span data-stu-id="28051-118">Media Sample Encryption Example</span></span>

<span data-ttu-id="28051-119">В следующем неполном примере показано, как зашифровать пример носителя с помощью шифрования DRM.</span><span class="sxs-lookup"><span data-stu-id="28051-119">The following incomplete example demonstrates how to encrypt a media sample using DRM encryption.</span></span> <span data-ttu-id="28051-120">Алгоритм шифрования RC4 был оставлен в этом примере из-за ограничений на пространство.</span><span class="sxs-lookup"><span data-stu-id="28051-120">The RC4 encryption algorithm has been left out of the example due to space restrictions.</span></span>


```C++
QWORD GetNextSalt(QWORD qwSalt)
{
   return InterlockedIncrement64( (volatile LONGLONG*)&qwSalt );
}

HRESULT EncryptSample( INSSBuffer *pSample )
{
    HRESULT hr = S_OK;
    INSSBuffer3 *pNSSBuffer3 = NULL;
    QWORD qwSalt = 0;
    BYTE *pbData = NULL;
    DWORD cbData = 0;

    hr = pSample->QueryInterface( IID_INSSBuffer3, (void**)&pNSSBuffer3 );
    if( FAILED( hr ) ) goto EXIT;

    hr = pSample->GetBufferAndLength( &pbData, &cbData );
    if( FAILED( hr ) ) goto EXIT;

    qwSalt = GetNextSalt(qwSalt);

    // TODO: Encrypt the sample by concatenating the initialization vector
    //   and using RC4 encryption.

    hr = pNSSBuffer3->SetProperty( 
        WM_SampleExtensionGUID_SampleProtectionSalt, 
        &qwSalt, sizeof( qwSalt ) );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pNSSBuffer3 );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="28051-121">См. также</span><span class="sxs-lookup"><span data-stu-id="28051-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28051-122">**Примеры импорта DRM**</span><span class="sxs-lookup"><span data-stu-id="28051-122">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




